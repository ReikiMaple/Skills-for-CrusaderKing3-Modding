# CK3 Mod 脚本语言编写指南

> 本文档基于Paradox官方Wiki的Scripting页面整理，介绍CK3脚本语言（Jomini Script）的完整编写结构。

---

## 目录

1. [语言概述](#1-语言概述)
2. [基础语法](#2-基础语法)
3. [作用域系统](#3-作用域系统)
4. [关键字与变量](#4-关键字与变量)
5. [运算符](#5-运算符)
6. [条件语句](#6-条件语句)
7. [列表与数组](#7-列表与数组)
8. [迭代器](#8-迭代器)
9. [模板与复用](#9-模板与复用)
10. [调试与测试](#10-调试与测试)

---

## 1. 语言概述

### 1.1 什么是Jomini Script

CK3使用**Paradox Scripting Language**（开发者称为**Jomini Script**）作为Mod脚本语言，游戏引擎为**Clausewitz**。

脚本主要用于：
- `common/` 文件夹：定义决议、事件、宗教、文化等
- `events/` 文件夹：编写事件逻辑

### 1.2 硬编码限制

以下功能**无法**通过脚本修改：
- AI行为逻辑
- 军队行为逻辑
- UI系统（除Scripted GUI外）
- 核心游戏机制算法

### 1.3 三种核心函数类型

| 类型 | 作用 | 使用位置 |
|------|------|----------|
| **Effects（效果）** | 执行操作，修改游戏状态 | `immediate = {}`, `effect = {}`, `on_accept = {}` |
| **Triggers（触发器）** | 检查条件，返回true/false | `limit = {}`, `trigger = {}` |
| **Event Targets（事件目标）** | 切换作用域 | 任何需要切换对象的地方 |

---

## 2. 基础语法

### 2.1 基本结构

```
# 简单赋值
key = value

# 代码块
key = {
    sub_key = sub_value
}

# 嵌套代码块
key = {
    a = b
    e = {
        f = g
    }
}
```

### 2.2 实际示例

```
is_alive = yes                    # 布尔值
add_gold = 100                    # 整数
debug_log = "hello world"         # 字符串
player_heir = { marry = root }    # 嵌套效果
```

### 2.3 语法规则

| 规则 | 说明 | 示例 |
|------|------|------|
| 等号 | 用于赋值和比较 | `key = value` |
| 花括号 | 定义代码块 | `{ ... }` |
| 注释 | 使用 `#` | `# 这是注释` |
| 引号 | 字符串需要引号 | `"hello"` |
| 缩进 | 不影响执行，仅提高可读性 | 推荐使用Tab或4空格 |

### 2.4 特殊语法：带target的触发器

```
# 使用引号包裹复杂表达式
add_gold = "opinion(liege)"
```

---

## 3. 作用域系统

### 3.1 什么是作用域（Scopes）

作用域是游戏中的实体对象，如角色、领地、信仰等。效果和触发器必须在正确的作用域上使用。

### 3.2 常用作用域

| 作用域 | 说明 | 示例触发器 |
|--------|------|-----------|
| `character` | 角色 | `age`, `is_alive` |
| `title` | 头衔 | `tier`, `is_landed` |
| `county` | 伯爵领 | `development`, `culture` |
| `faith` | 信仰 | `religious_head`, `fervor` |
| `culture` | 文化 | `traditions`, `era` |

### 3.3 事件目标（Event Targets）

事件目标用于在不同作用域之间切换，称为**scoping**。

**常用事件目标：**
```
primary_heir          # 主要继承人
spouse               # 配偶
liege                # 领主
realm_capital        # 领地首都
title_holder         # 头衔持有者
de_jure_liege        # 法理领主
faith                # 信仰
religious_head       # 宗教领袖
culture              # 文化
```

### 3.4 链式调用

```
# 方法1：点号链式
primary_heir.faith.religious_head

# 方法2：代码块嵌套（等效）
primary_heir = {
    faith = {
        religious_head = { }
    }
}
```

### 3.5 前缀引用

使用特殊前缀直接引用特定对象：

```
# 引用文化
set_culture = culture:english
set_culture = culture:chinese

# 引用信仰
set_character_faith = faith:orthodox
set_character_faith = faith:catholic

# 引用头衔
capital_county = title:c_byzantion
holder = title:k_england

# 引用角色（使用角色ID）
marry = character:123456
kill = character:789012
```

---

## 4. 关键字与变量

### 4.1 核心关键字

| 关键字 | 作用 | 示例 |
|--------|------|------|
| `root` | 脚本的根对象 | `primary_heir = { set_relation_grudge = root }` |
| `prev` | 上一个作用域 | 用于返回前一个对象 |
| `this` | 当前作用域 | `this = root` |

**prev使用示例：**
```
primary_heir = {
    primary_spouse = {
        set_relation_soulmate = prev    # prev指向primary_heir
    }
}
```

### 4.2 保存的作用域（Saved Scopes）

```
# 保存作用域
primary_heir = { save_scope_as = my_son }

# 使用保存的作用域
scope:my_son = { death = natural }
```

**保存数值：**
```
save_scope_value_as = {
    name = cost
    value = primary_heir.age
}
add_gold = scope:cost
```

**重要提示：**
- 在触发器中使用 `save_temporary_scope_as` 和 `save_temporary_scope_value_as`
- `scope:` 只用于保存的作用域，不用于事件目标或关键字

### 4.3 变量系统

#### 变量类型

| 类型 | 定义方式 | 访问方式 | 说明 |
|------|----------|----------|------|
| 普通变量 | `set_variable` | `var:` | 存储在作用域上，角色死亡会丢失 |
| 全局变量 | `set_global_variable` | `global_var:` | 全局可访问，唯一 |
| 局部变量 | `set_local_variable` | `local_var:` | 临时存在，脚本执行后消失 |
| 死亡角色变量 | `set_dead_character_variable` | `dead_var:` | 存储在死亡角色上，有过期时间 |

#### 变量操作

```
# 设置变量
set_variable = {
    name = test
    value = 10
}

# 简单设置（等效于value = yes）
set_variable = test

# 修改变量
change_variable = {
    name = test
    add = 1
}

# 复杂计算
set_variable = {
    name = test
    value = {
        add = 10
        divide = 5
        subtract = 1
    }
}

# 删除变量
remove_variable = test

# 检查变量存在
has_variable = test
```

#### 变量引用

```
# 在效果中引用
add_gold = var:test

# 链式引用
add_gold = player_heir.var:my_sons_birthday

# 在UI中显示
"[GetPlayer.MakeScope.Var('test').GetValue]"
"[GetGlobalVariable('test').GetValue]"
```

---

## 5. 运算符

### 5.1 逻辑运算符

| 运算符 | 说明 | 示例 |
|--------|------|------|
| `AND` | 所有条件为真 | `AND = { is_adult = yes has_trait = brave }` |
| `OR` | 任一条件为真 | `OR = { is_ai = yes gold > 100 }` |
| `NOT` | 条件为假 | `NOT = { has_trait = craven }` |
| `NOR` | 所有条件为假 | `NOR = { has_trait = lazy has_trait = craven }` |
| `NAND` | 任一条件为假 | `NAND = { is_ai = yes gold > 100 }` |

**注意：**
- 触发器块默认就是AND，可以直接写多个条件
- 运算符通常大写以提高可读性

### 5.2 关系运算符

| 运算符 | 说明 |
|--------|------|
| `=` | 等于 |
| `!=` | 不等于 |
| `<` | 小于 |
| `<=` | 小于等于 |
| `>` | 大于 |
| `>=` | 大于等于 |
| `?=` | 存在则比较（避免错误） |

**特殊运算符 `?=`：**
```
# 检查capital_county存在，且等于title:c_byzantion
capital_county ?= title:c_byzantion

# 等效于：
exists = capital_county
capital_county = title:c_byzantion
```

---

## 6. 条件语句

### 6.1 if / else / else_if

```
if = {
    limit = { is_ai = no }
    add_gold = 100
}
```

**完整结构：**
```
if = {
    limit = {
        # 条件
    }
    # 效果
}
else_if = {
    limit = {
        # 其他条件
    }
    # 其他效果
}
else = {
    # 默认效果
}
```

**注意事项：**
- `limit` 默认就是AND块，可以写多个条件
- 确保效果在 `if` 块内，但在 `limit` 块外

### 6.2 switch语句

当有很多 `else_if` 检查同一个触发器时，使用 `switch` 更简洁：

```
switch = {
    trigger = has_culture
    culture:english = { add_gold = 10 }
    culture:french = { add_gold = 20 }
    culture:italian = { add_gold = 30 }
}
```

### 6.3 while循环

```
# 固定次数
while = {
    count = 10
    add_gold = 100
}

# 条件循环
while = {
    limit = { gold > 0 }
    remove_short_term_gold = 50
}
```

**限制：**
- 默认最多1000次迭代
- 无法break跳出循环

### 6.4 trigger_if / trigger_else

用于触发器块中的条件检查：

```
trigger_if = {
    limit = { is_ai = no }
    is_independent_ruler = yes
}
```

**注意：**
- 使用 `trigger_else_if` 后必须用 `trigger_else` 结束
- 只能在触发器块中使用，不能在效果块中使用

---

## 7. 列表与数组

### 7.1 列表类型

| 类型 | 创建方式 | 说明 |
|------|----------|------|
| 临时列表 | `add_to_list` | 脚本执行期间存在 |
| 临时变量列表 | `add_to_local_variable_list` | 支持过期时间 |
| 临时触发器列表 | `add_to_temporary_list` | 可在触发器块中使用 |
| 永久变量列表 | `add_to_variable_list` | 存储在作用域上，支持过期时间 |
| 永久全局列表 | `add_to_global_variable_list` | 全局可访问，支持过期时间 |

### 7.2 列表操作

```
# 创建列表（如果不存在会自动创建）
every_ruler = {
    root = {
        add_to_variable_list = {
            name = rulers
            target = prev
        }
    }
}

# 检查元素是否在列表中
is_in_list = my_list
is_target_in_variable_list = {
    name = my_list
    target = scope:target
}

# 移除元素
remove_from_list = my_list
remove_list_variable = {
    name = my_list
    target = scope:target
}

# 清空列表
clear_variable_list = my_list
```

**重要提示：**
- 如果元素已在列表中，不会重复添加
- 重新创建列表前建议先 `clear_variable_list`
- 列表不能包含其他列表

---

## 8. 迭代器

### 8.1 效果迭代器（用于效果块）

| 迭代器 | 说明 |
|--------|------|
| `every_x` | 遍历所有项目（按添加顺序） |
| `ordered_x` | 按值排序后遍历 |
| `random_x` | 随机选择一个项目 |

**示例：**
```
every_ruler = {
    limit = { age > 20 }
    add_gold = 100
}
```

### 8.2 触发器迭代器（用于触发器块）

| 迭代器 | 说明 |
|--------|------|
| `any_x` | 遍历所有项目，返回true如果条件对所有项目都成立 |

**示例：**
```
any_living_character = {
    count > 10
    has_culture = culture:english
    is_adult = yes
}
```

**注意事项：**
- `any_x` 中不要使用 `limit`，它本身就是触发器
- 可以使用 `count` 和 `percent` 指定需要满足条件的项目数量

### 8.3 列表迭代器

```
# 遍历列表
every_in_list = {
    variable = my_list
    add_gold = 100
}

# 排序遍历
ordered_in_list = {
    variable = my_list
    order_by = age
    add_gold = 100
}

# 随机选择
random_in_list = {
    variable = my_list
    add_gold = 100
}

# 触发器检查
any_in_list = {
    variable = my_list
    has_trait = brave
}
```

---

## 9. 模板与复用

### 9.1 Scripted Effects（脚本化效果）

定义在 `common/scripted_effects` 或事件文件中：

```
# 定义
my_effect = {
    add_gold = 100
}

# 使用
my_effect = yes
```

**事件文件中定义（需要scripted_effect关键字）：**
```
scripted_effect convert_family = {
    every_close_family_member = {
        set_character_faith = faith:adamites
    }
}

# 使用
convert_family = yes
```

### 9.2 参数替换

使用 `$$` 标记参数位置：

```
# 定义带参数的效果
gift = {
    add_gold = $val$
}

# 使用并传入参数
gift = { val = 100 }
```

**替换部分效果：**
```
my_iterator = {
    every_$WHO$ = { add_gold = 10 }
}

# 使用
my_iterator = { WHO = child }    # 变成 every_child = { add_gold = 10 }
```

**插入整块脚本：**
```
do_anything = { $DO$ }

do_anything = { DO = "add_gold = 100" }
```

### 9.3 Scripted Triggers（脚本化触发器）

定义在 `common/scripted_triggers` 或事件文件中：

```
# 定义
my_trigger = {
    is_ai = yes
}

# 使用
my_trigger = yes

# 取反使用
my_trigger = no    # 等效于 NOT = { my_trigger = yes }
```

### 9.4 Script Values（脚本值）

定义在 `common/script_values`：

```
# 定义
my_value = {
    add = age
    add = 10
    divide = 5
}

# 使用
add_gold = my_value
```

**在UI中显示：**
```
"[GetPlayer.MakeScope.ScriptValue('my_value')]"
```

**性能注意：**
- 脚本值每次使用都会重新计算
- UI中每帧都会重新计算，复杂计算可能导致卡顿

---

**文档版本**：1.0  
**最后更新**：2026-03-27  
**基于**：CK3 Wiki Scripting页面
