# CK3 效果（Effects）系统详解

> 本文档基于Paradox官方Wiki的Effects页面整理，介绍CK3脚本中效果的概念、类型和使用方法。

---

## 目录

1. [效果基础概念](#1-效果基础概念)
2. [效果块（Effect Blocks）](#2-效果块effect-blocks)
3. [效果语法](#3-效果语法)
4. [条件效果](#4-条件效果)
5. [控制效果](#5-控制效果)
6. [常用效果分类](#6-常用效果分类)
7. [Scripted Effects](#7-scripted-effects)

---

## 1. 效果基础概念

### 1.1 什么是效果

**效果（Effect）**是CK3脚本中用于改变游戏状态的命令。与触发器（Triggers）只检查条件不同，效果会实际执行操作并修改游戏数据。

**完整列表**可在 `effects.log` 中查看（运行 `script_docs` 控制台命令生成）。

### 1.2 效果与触发器的区别

| 类型 | 作用 | 示例 |
|------|------|------|
| **Triggers** | 检查条件，返回true/false | `is_ai = yes` |
| **Effects** | 执行操作，修改游戏状态 | `add_gold = 100` |

---

## 2. 效果块（Effect Blocks）

### 2.1 什么是效果块

效果在**效果块（Effect Blocks）**中执行。效果块可以是显式命名的，也可以是暗示执行时机的。

### 2.2 常见效果块

| 效果块 | 说明 | 使用场景 |
|--------|------|----------|
| `immediate = {}` | 事件触发时立即执行 | 事件 |
| `effect = {}` | 标准效果块 | 决议、互动 |
| `on_accept = {}` | 接受时执行 | 角色互动 |
| `on_decline = {}` | 拒绝时执行 | 角色互动 |
| `after = {}` | 选择选项后执行 | 事件 |

### 2.3 混合块示例

```
option = {
    is_shown = { is_ai = yes }      # 触发器块
    ai_will_do = { base = 100 }      # AI逻辑块
    add_gold = 100                   # 效果（选择时执行）
}
```

---

## 3. 效果语法

### 3.1 布尔形式（Boolean Form）

最简单的形式，后面跟 `= yes`。

```
# 释放当前角色出狱
release_from_prison = yes

# 清除所有特质
clear_traits = yes

# 结束战争
end_war = white_peace
```

### 3.2 简单形式（Simple Form）

需要一个参数，可以是：

**作用域参数：**
```
# 让目标成为当前角色的配偶
marry = scope:bride

# 离婚
divorce = scope:spouse
```

**数据库键参数：**
```
# 改变监狱类型
change_prison_type = house_arrest

# 添加特质
add_trait = brave

# 移除特质
remove_trait = craven
```

**数值参数：**
```
# 添加金币
add_gold = 1000

# 添加威望
add_prestige = 500

# 添加虔诚
add_piety = 250
```

### 3.3 复杂形式（Complex Form）

使用多个参数的脚本块。

```
# 监禁角色
imprison = {
    target = scope:imprisoned_character
    type = house_arrest
}

# 添加好感
add_opinion = {
    target = scope:other_character
    modifier = opinion_modifier_name
    value = 20
    days = 365
}

# 添加钩子
add_hook = {
    type = favor_hook
    target = scope:target_character
    days = 1825
}
```

---

## 4. 条件效果

### 4.1 if / else_if / else

```
if = {
    limit = { is_ai = no }
    add_gold = 100
}
else_if = {
    limit = { prestige >= 1000 }
    add_prestige = -100
}
else = {
    add_piety = 50
}
```

### 4.2 while 循环

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

**限制：** 默认最多1000次迭代，无法break跳出。

### 4.3 switch 语句

```
switch = {
    trigger = has_culture
    culture:english = { add_gold = 10 }
    culture:french = { add_gold = 20 }
    culture:italian = { add_gold = 30 }
    fallback = { add_gold = 5 }
}
```

---

## 5. 控制效果

### 5.1 隐藏效果

```
# 效果执行但不显示在提示中
hidden_effect = {
    add_gold = 1000
    add_trait = secret_trait
}
```

### 5.2 仅提示效果

```
# 只在提示中显示，不实际执行
show_as_tooltip = {
    add_gold = 100
}
```

### 5.3 自定义描述

```
custom_description = {
    text = my_effect_description
    subject = scope:actor
    object = scope:recipient
    value = 100
    add_gold = 100
}
```

### 5.4 随机效果

```
# 简单随机
random = {
    chance = 50
    add_gold = 100
}

# 带权重的随机列表
random_list = {
    10 = { add_gold = 100 }
    20 = { add_prestige = 100 }
    30 = { add_piety = 100 }
}
```

### 5.5 发送消息

```
# 发送界面消息
send_interface_message = {
    type = message_type
    title = my_title_loc
    desc = my_desc_loc
    left_icon = scope:character
    right_icon = scope:title
    goto = scope:province
    add_dread = 5
}

# 发送Toast消息
send_interface_toast = {
    type = message_type
    title = my_title_loc
    add_gold = 100
}
```

---

## 6. 常用效果分类

### 6.1 角色资源效果

| 效果 | 说明 | 示例 |
|------|------|------|
| `add_gold` | 添加金币 | `add_gold = 100` |
| `add_prestige` | 添加威望 | `add_prestige = 50` |
| `add_piety` | 添加虔诚 | `add_piety = 25` |
| `add_dread` | 添加恐惧 | `add_dread = 10` |
| `remove_short_term_gold` | 移除短期金币 | `remove_short_term_gold = 50` |

### 6.2 特质效果

| 效果 | 说明 | 示例 |
|------|------|------|
| `add_trait` | 添加特质 | `add_trait = brave` |
| `remove_trait` | 移除特质 | `remove_trait = craven` |
| `clear_traits` | 清除所有特质 | `clear_traits = yes` |
| `copy_traits` | 复制特质 | `copy_traits = scope:target` |

### 6.3 关系效果

| 效果 | 说明 | 示例 |
|------|------|------|
| `add_opinion` | 添加好感 | `add_opinion = { target = X modifier = Y }` |
| `add_hook` | 添加钩子 | `add_hook = { type = X target = Y }` |
| `marry` | 结婚 | `marry = scope:spouse` |
| `divorce` | 离婚 | `divorce = scope:spouse` |
| `create_betrothal` | 订婚 | `create_betrothal = scope:target` |
| `break_betrothal` | 解除婚约 | `break_betrothal = scope:target` |

### 6.4 头衔效果

| 效果 | 说明 | 示例 |
|------|------|------|
| `create_title` | 创建头衔 | `create_title = { tier = kingdom }` |
| `destroy_title` | 销毁头衔 | `destroy_title = title:k_france` |
| `usurp_title` | 篡夺头衔 | `usurp_title = title:c_county` |
| `grant_title` | 授予头衔 | `grant_title = scope:recipient` |
| `revoke_title` | 撤销头衔 | `revoke_title = scope:target` |
| `change_title_holder` | 改变头衔持有者 | `change_title_holder = { holder = X }` |

### 6.5 战争效果

| 效果 | 说明 | 示例 |
|------|------|------|
| `declare_war` | 宣战 | `declare_war = { target = X casus_belli = Y }` |
| `end_war` | 结束战争 | `end_war = white_peace` |
| `add_attacker` | 添加攻击方 | `add_attacker = scope:character` |
| `add_defender` | 添加防守方 | `add_defender = scope:character` |

### 6.6 监禁效果

| 效果 | 说明 | 示例 |
|------|------|------|
| `imprison` | 监禁 | `imprison = { target = X type = Y }` |
| `release_from_prison` | 释放 | `release_from_prison = yes` |
| `execute` | 处决 | `execute = scope:prisoner` |
| `banish` | 放逐 | `banish = scope:target` |

### 6.7 角色创建效果

| 效果 | 说明 | 示例 |
|------|------|------|
| `create_character` | 创建角色 | `create_character = { age = 20 gender = male }` |
| `kill` | 杀死角色 | `kill = scope:target` |
| `death = natural` | 自然死亡 | `death = natural` |
| `death = murder` | 被谋杀 | `death = murder` |

### 6.8 变量效果

| 效果 | 说明 | 示例 |
|------|------|------|
| `set_variable` | 设置变量 | `set_variable = { name = X value = Y }` |
| `change_variable` | 修改变量 | `change_variable = { name = X add = Y }` |
| `remove_variable` | 移除变量 | `remove_variable = X` |
| `save_scope_as` | 保存作用域 | `save_scope_as = my_scope` |
| `save_scope_value_as` | 保存数值 | `save_scope_value_as = { name = X value = Y }` |

### 6.9 事件效果

| 效果 | 说明 | 示例 |
|------|------|------|
| `trigger_event` | 触发事件 | `trigger_event = { id = X days = Y }` |
| `trigger_event = { on_action = X }` | 触发on_action | `trigger_event = { on_action = my_on_action }` |

### 6.10 列表迭代效果

| 效果 | 说明 | 示例 |
|------|------|------|
| `every_child` | 遍历所有子女 | `every_child = { add_gold = 10 }` |
| `every_vassal` | 遍历所有封臣 | `every_vassal = { add_opinion = X }` |
| `every_courtier` | 遍历所有廷臣 | `every_courtier = { ... }` |
| `random_child` | 随机选择子女 | `random_child = { ... }` |
| `ordered_child` | 排序选择子女 | `ordered_child = { order_by = age }` |

---

## 7. Scripted Effects

### 7.1 什么是Scripted Effects

**Scripted Effects**是宏，允许用单个语句替换一组效果，使脚本更易读并避免重复。

定义在 `common/scripted_effects/` 中，可以在任何允许效果的地方使用。

### 7.2 简单形式

**定义：**
```
# common/scripted_effects/my_effects.txt
give_gold_prestige_piety = {
    add_gold = 1000
    add_prestige = 1000
    add_piety = 1000
}
```

**使用：**
```
immediate = {
    give_gold_prestige_piety = yes
}
```

**注意：** 不建议在scripted effects中使用 `root` 或 `prev` 等模糊的事件目标。

### 7.3 复杂形式（带参数）

使用 `$$` 标记参数位置。

**定义：**
```
give_resources = {
    add_gold = $GOLD$
    add_prestige = $PRESTIGE$
    add_piety = $PIETY$
}
```

**使用：**
```
give_resources = {
    GOLD = 1000
    PRESTIGE = 500
    PIETY = 250
}
```

### 7.4 参数替换注意事项

文本替换是**字面替换**，在scripted effect求值之前发生。

**问题示例：**
```
# 定义
give_gold = {
    $GIVER$ = {
        remove_short_term_gold = $VALUE$
        $TAKER$ = {
            add_gold = $VALUE$
        }
    }
}

# 使用
give_gold = {
    GIVER = father
    TAKER = mother
    VALUE = 1000
}

# 实际解释（错误！）
father = {
    remove_short_term_gold = 1000
    mother = {  # 错误：mother在father内部
        add_gold = 1000
    }
}
```

**正确做法：** 先保存作用域
```
give_gold = {
    $GIVER$ = { save_scope_as = giver }
    $TAKER$ = { save_scope_as = taker }
    save_scope_value_as = {
        name = gold_amount
        value = $VALUE$
    }
    scope:giver = {
        remove_short_term_gold = scope:gold_amount
        scope:taker = {
            add_gold = scope:gold_amount
        }
    }
    clear_saved_scope = giver
    clear_saved_scope = taker
}
```

---

## 附录：效果速查表

### 角色属性效果

```
add_gold = 100                    # 添加金币
add_prestige = 50                 # 添加威望
add_piety = 25                    # 添加虔诚
add_dread = 10                    # 添加恐惧
add_stress = 20                   # 添加压力
add_tyranny = 5                   # 添加暴政
```

### 生活方式效果

```
add_diplomacy_skill = 1           # 添加外交技能
add_martial_skill = 1             # 添加军事技能
add_stewardship_skill = 1         # 添加管理技能
add_intrigue_skill = 1            # 添加谋略技能
add_learning_skill = 1            # 添加学识技能
add_prowess_skill = 1             # 添加勇武技能

add_diplomacy_lifestyle_xp = 100  # 添加外交生活方式经验
add_perk = diplomat_perk_1        # 添加生活方式 perk
```

### 头衔操作效果

```
create_title = { tier = kingdom } # 创建头衔
usurp_title = title:k_france      # 篡夺头衔
destroy_title = title:k_france    # 销毁头衔
grant_title = scope:recipient     # 授予头衔
revoke_title = scope:target       # 撤销头衔
```

### 变量操作效果

```
set_variable = { name = my_var value = 100 }
change_variable = { name = my_var add = 10 }
remove_variable = my_var
save_scope_as = my_scope
save_scope_value_as = { name = my_value value = 50 }
```

---

**文档版本**：1.0  
**最后更新**：2026-03-27  
**基于**：CK3 Wiki Effects页面
