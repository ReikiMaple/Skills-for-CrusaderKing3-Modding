# CK3 触发器（Triggers）系统详解

> 本文档基于Paradox官方Wiki的Triggers页面整理，介绍CK3脚本中触发器的概念、类型和使用方法。

---

## 目录

1. [触发器基础概念](#1-触发器基础概念)
2. [触发器块（Trigger Blocks）](#2-触发器块trigger-blocks)
3. [逻辑块](#3-逻辑块)
4. [Limit块](#4-limit块)
5. [触发器语法](#5-触发器语法)
6. [Scripted Triggers](#6-scripted-triggers)
7. [逻辑运算符](#7-逻辑运算符)

---

## 1. 触发器基础概念

### 1.1 什么是触发器

**触发器（Trigger）**是CK3脚本中用于检查条件的命令。触发器返回 **true** 或 **false**，用于控制脚本流程。

**示例：**
```
is_ai = yes    # 如果是AI角色返回true，玩家返回false
```

### 1.2 触发器与效果的区别

| 类型 | 作用 | 返回值 | 示例 |
|------|------|--------|------|
| **Triggers** | 检查条件 | true/false | `is_ai = yes` |
| **Effects** | 执行操作 | 无 | `add_gold = 100` |

### 1.3 返回值的使用

比较值的触发器可以返回该值本身，用于效果中：

```
# 添加与当前金币数量相同的金币
add_gold = gold

# 添加与年龄相同的威望
add_prestige = age
```

**完整列表**可在 `triggers.log` 中查看（运行 `script_docs` 控制台命令生成）。

---

## 2. 触发器块（Trigger Blocks）

### 2.1 什么是触发器块

触发器在**触发器块（Trigger Blocks）**中使用。触发器块可以是显式命名的，也可以是暗示其用途的。

### 2.2 常见触发器块

| 触发器块 | 说明 | 使用场景 |
|----------|------|----------|
| `trigger = {}` | 标准触发器块 | 事件、决议 |
| `is_shown = {}` | 是否显示 | 决议、互动选项 |
| `is_valid = {}` | 是否有效 | 决议、互动 |
| `limit = {}` | 限制条件 | if语句、列表构建器 |
| `filter = {}` | 过滤条件 | any_X列表构建器 |

### 2.3 混合块示例

```
modifier = {
    is_ai = yes      # 触发器
    factor = 0       # 运算符
}
```

### 2.4 提前退出（Early Out）

触发器块默认使用**提前退出**原则：
- 触发器块中的所有触发器都必须为true，整个块才为true
- 一旦某个触发器为false，后续触发器不再检查

**性能优化示例：**
```
trigger = {
    is_ai = no              # 先检查（大多数角色是AI，这里会提前退出）
    is_independent_ruler = yes
}
```

**避免错误示例：**
```
trigger = {
    exists = primary_spouse          # 先检查是否存在
    culture = primary_spouse.culture # 再使用
}
```

---

## 3. 逻辑块

### 3.1 AND（逻辑与）

默认逻辑，所有触发器都必须为true。

```
AND = {
    is_ai = no
    is_independent_ruler = yes
}
# 等同于：
is_ai = no
is_independent_ruler = yes
```

### 3.2 OR（逻辑或）

任一触发器为true，整个块为true。

```
OR = {
    is_ai = no
    is_independent_ruler = yes
}
# 玩家或独立统治者都返回true
```

### 3.3 NOT（逻辑非）

取反单个触发器。

```
NOT = { has_title = title:k_france }
# 不持有法兰西王国返回true
```

**注意：** NOT应只包含单个触发器。多个触发器使用NOR或NAND。

### 3.4 NOR（逻辑或非）

所有触发器都为false时返回true。

```
NOR = {
    has_title = title:k_france
    has_title = title:k_aquitaine
}
# 既不持有法兰西也不持有阿基坦返回true
```

### 3.5 NAND（逻辑与非）

任一触发器为false时返回true。

```
NAND = {
    has_title = title:k_france
    has_title = title:k_aquitaine
}
# 不同时持有两个王国返回true
```

---

## 4. Limit块

### 4.1 if/else_if中的limit

```
if = {
    limit = { is_ai = no }
    add_gold = 100
}
```

### 4.2 效果列表构建器中的limit

```
every_child = {
    limit = { is_male = yes }
    add_gold = 100
}
```

**注意：** `any_X` 列表构建器**不使用** limit块。

### 4.3 trigger_if / trigger_else_if / trigger_else

用于触发器块中的条件检查：

```
trigger_if = {
    limit = { exists = primary_spouse }
    culture = primary_spouse.culture
}
```

**用途：**
- 提高可读性
- 避免工具提示中的错误（工具提示时不使用early out）

---

## 5. 触发器语法

### 5.1 作用域比较

检查两个作用域是否相同。

```
# 检查法兰西国王是否是当前角色的父亲
title:k_france.holder = father
```

**安全比较（?=）：**
```
# 先检查存在性，再比较
title:k_france.holder ?= father
# 等效于：
exists = title:k_france.holder
title:k_france.holder = father
```

### 5.2 数值比较

| 运算符 | 说明 |
|--------|------|
| `=` | 等于 |
| `!=` | 不等于 |
| `>` | 大于 |
| `>=` | 大于等于 |
| `<` | 小于 |
| `<=` | 小于等于 |

```
gold > 1000           # 金币大于1000
age >= 18             # 年龄大于等于18
prestige < 100        # 威望小于100
```

**可比较的值：**
- 数字
- 命名值
- 脚本值（script_value）
- 保存的作用域值
- 存储数字的变量

### 5.3 基本触发器（Basic Triggers）

检查布尔值。

```
is_ai = no            # 不是AI
is_alive = yes        # 存活
is_adult = yes        # 成年
is_married = yes      # 已婚
is_at_war = no        # 不在战争中
```

### 5.4 简单触发器（Simple Triggers）

**作用域参数：**
```
is_vassal_of = scope:actor
is_liege_of = scope:target
is_allied_to = scope:ally
```

**数据库键参数：**
```
has_trait = infirm
has_trait = brave
has_culture = culture:english
has_faith = faith:catholic
```

### 5.5 复杂触发器（Complex Triggers）

使用多个参数。

```
is_scheming_against = {
    target = liege
    type = murder
}

has_opinion_modifier = {
    target = scope:other
    modifier = opinion_modifier_name
}

has_relation = {
    target = scope:friend
    relation = friend
}
```

---

## 6. Scripted Triggers

### 6.1 什么是Scripted Triggers

**Scripted Triggers**是宏，允许用单个语句替换一组触发器，使脚本更易读并避免重复。

定义在 `common/scripted_triggers/` 中，可以在任何允许触发器的地方使用。

### 6.2 基本形式

**定义：**
```
# common/scripted_triggers/my_triggers.txt
is_rich_adult_independent_ruler = {
    is_adult = yes
    is_independent_ruler = yes
    gold > 1000
}
```

**使用：**
```
trigger = {
    is_rich_adult_independent_ruler = yes
}

# 取反使用
trigger = {
    is_rich_adult_independent_ruler = no
}
# 等效于：
NOT = { is_rich_adult_independent_ruler = yes }
```

**注意：** 不建议在scripted triggers中使用 `root` 或 `prev` 等模糊的事件目标。

### 6.3 复杂形式（带参数）

使用 `$$` 标记参数位置。

**定义：**
```
is_related_vassal_of = {
    is_vassal_of = $TARGET$
    is_close_family_of = $TARGET$
}
```

**使用：**
```
is_related_vassal_of = {
    TARGET = title:k_france.holder
}
```

**文本替换说明：**
- 替换是**字面替换**，在scripted trigger求值之前发生
- 每个 `$TARGET$` 会被替换为提供的参数

---

## 7. 逻辑运算符

### 7.1 常用逻辑触发器

| 触发器 | 说明 | 示例 |
|--------|------|------|
| `always` | 总是返回指定值 | `always = yes` |
| `AND` | 所有子触发器为true | `AND = { ... }` |
| `OR` | 任一子触发器为true | `OR = { ... }` |
| `NOT` | 取反 | `NOT = { ... }` |
| `NOR` | 所有子触发器为false | `NOR = { ... }` |
| `NAND` | 任一子触发器为false | `NAND = { ... }` |
| `all_false` | 等效于NOR | `all_false = { ... }` |
| `any_false` | 等效于NAND | `any_false = { ... }` |

### 7.2 switch语句

```
switch = {
    trigger = has_culture
    culture:english = { is_ai = yes }
    culture:french = { gold > 1000 }
    fallback = { prestige > 500 }
}
```

---

## 附录：常用触发器速查表

### 角色状态触发器

```
is_ai = yes/no                    # 是否是AI
is_alive = yes/no                 # 是否存活
is_adult = yes/no                 # 是否成年
is_married = yes/no               # 是否已婚
is_betrothed = yes/no             # 是否订婚
is_pregnant = yes/no              # 是否怀孕
is_at_war = yes/no                # 是否在战争中
is_in_prison = yes/no             # 是否被监禁
is_independent_ruler = yes/no     # 是否独立统治者
is_landed = yes/no                # 是否有领地
```

### 数值比较触发器

```
age >= 18                         # 年龄
gold > 1000                       # 金币
prestige >= 1000                  # 威望
piety >= 500                      # 虔诚
dread >= 20                       # 恐惧
stress >= 50                      # 压力
tyranny >= 10                     # 暴政
```

### 特质触发器

```
has_trait = brave                 # 有特定特质
has_any_trait = yes               # 有任何特质
has_trait_with_flag = flag_name   # 有带特定标志的特质
```

### 头衔触发器

```
has_title = title:k_france        # 拥有头衔
holds_landed_title = yes          # 持有领地头衔
has_claim_on = scope:title        # 有宣称
tier = tier_kingdom               # 头衔等级
```

### 关系触发器

```
is_vassal_of = scope:liege        # 是封臣
is_liege_of = scope:vassal        # 是领主
is_allied_to = scope:ally         # 是盟友
is_at_war_with = scope:enemy      # 在战争中
has_opinion_modifier = {          # 有好感修正
    target = scope:other
    modifier = opinion_modifier
}
```

### 家族关系触发器

```
is_child_of = scope:parent        # 是子女
is_parent_of = scope:child        # 是父母
is_sibling_of = scope:sibling     # 是兄弟姐妹
is_spouse_of = scope:spouse       # 是配偶
is_concubine_of = scope:owner     # 是侍妾
```

### 存在性检查

```
exists = primary_spouse           # 存在配偶
exists = liege                    # 存在领主
exists = scope:saved_scope        # 存在保存的作用域
has_variable = my_var             # 有变量
```

---

**文档版本**：1.0  
**最后更新**：2026-03-27  
**基于**：CK3 Wiki Triggers页面
