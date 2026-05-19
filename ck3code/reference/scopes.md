# CK3 作用域（Scopes）系统详解

> 本文档基于Paradox官方Wiki的Scopes页面整理，介绍CK3脚本中作用域的概念、类型和使用方法。

---

## 目录

1. [作用域基础概念](#1-作用域基础概念)
2. [作用域类型](#2-作用域类型)
3. [访问作用域的方法](#3-访问作用域的方法)
4. [上下文切换](#4-上下文切换)
5. [事件目标（Event Targets）](#5-事件目标event-targets)
6. [保存的作用域（Saved Scopes）](#6-保存的作用域saved-scopes)
7. [列表构建器（List-builders）](#7-列表构建器list-builders)
8. [保存的作用域值](#8-保存的作用域值)

---

## 1. 作用域基础概念

### 1.1 什么是作用域

**作用域（Scope）**是CK3脚本中用于选择游戏实体的机制。通过作用域，我们可以：
- 使用**触发器（Triggers）**读取信息
- 使用**效果（Effects）**写入或修改信息
- 在不同实体之间切换

### 1.2 脚本执行上下文

在脚本中，效果和触发器总是在特定的**上下文（Context）**中执行。大多数效果和触发器只能在特定的作用域类型上工作。

**示例：**
```
# is_ai 触发器只能在角色作用域上使用
is_ai = no    # 检查当前作用域是否是玩家（非AI）
```

如果在一个错误的作用域类型上使用触发器，会抛出错误。

---

## 2. 作用域类型

### 2.1 数据库作用域（Database Scope）

最常见的作用域类型，指代游戏中的数据库对象。

**主要特点：**
- 可以读取信息（使用Triggers）
- 可以写入或修改信息（使用Effects）
- 可以在不同作用域之间移动

**常见的数据库作用域类型：**

| 作用域类型 | 说明 | 示例 |
|-----------|------|------|
| `character` | 角色 | 玩家角色、NPC |
| `title` | 头衔 | 王国、公国、伯爵领 |
| `county` | 伯爵领 | 地图上的领地 |
| `province` | 省份 | 地图省份 |
| `faith` | 信仰 | 宗教派别 |
| `culture` | 文化 | 文化群体 |
| `dynasty` | 宗族 | 宗族 |
| `house` | 家族 | 家族 |
| `war` | 战争 | 进行中的战争 |
| `scheme` | 阴谋 | 阴谋活动 |

**完整列表**可在 `event_scopes.log` 中查看（运行 `script_docs` 控制台命令生成）。

### 2.2 原始作用域（Primitive Scope）

原始作用域包括：
- **数字**（Numbers）
- **布尔值**（Booleans: yes/no）
- **标志值**（Flags: `flag:some_string`）

这些作用域不能被修改或访问，但了解它们有助于理解高级功能或错误日志。

### 2.3 顶层作用域（Top Scope）

顶层作用域是一个临时的抽象对象，用于存储信息，主要用于本地化和GUI中检索和显示数据。

---

## 3. 访问作用域的方法

### 3.1 root - 根作用域

`root` 是一个快捷方式，指向效果块或触发器块的默认上下文。

**重要说明：**
- `root` **不是**玩家！CK3是一个可以有多个玩家的游戏
- `root` 不一定是角色作用域，取决于具体的效果/触发器块
- 不是所有效果/触发器块都有 `root`

**示例：**
```
immediate = {
    # 这里的上下文是接收事件的角色
    title:k_france = {
        # 这里的上下文是法兰西王国头衔
        root = {
            # 回到接收事件的角色上下文
        }
    }
}
```

### 3.2 数据库直接访问

使用 `<scope type>:<scope key>` 语法直接访问数据库对象。

```
# 访问法兰西王国头衔
title:k_france = {
    # 上下文是法兰西王国
}

# 访问特定角色（使用历史ID）
character:123456 = {
    # 上下文是角色123456
}
```

**注意：**
- 角色有两个ID：历史ID（预定）和运行时ID（动态分配）
- 只有历史角色可以通过ID访问
- 非历史角色的运行时ID在不同游戏中不一致，无法引用

### 3.3 前缀引用

使用特殊前缀直接引用特定对象：

```
# 引用文化
set_culture = culture:english

# 引用信仰
set_character_faith = faith:orthodox

# 引用头衔
capital_county = title:c_byzantion
```

---

## 4. 上下文切换

### 4.1 基本语法

通过打开新的脚本块来切换上下文：

```
<scope> = {
    # 新的上下文
}
```

**示例：**
```
immediate = {
    # 上下文：接收事件的角色
    title:k_france = {
        # 上下文：法兰西王国头衔
        holder = {
            # 上下文：法兰西国王
        }
        # 回到法兰西王国上下文
    }
    # 回到接收事件的角色上下文
}
```

### 4.2 上下文切换失败

如果尝试切换到无效的作用域，会导致上下文切换失败：

```
# 错误示例：拼写错误
title:k_frnace = {    # k_frnace 未定义，切换失败
```

### 4.3 使用root返回

可以使用 `root` 随时返回到默认上下文：

```
immediate = {
    title:k_france = {
        # 法兰西王国上下文
        root = {
            # 回到接收事件的角色上下文
        }
        # 回到法兰西王国上下文
    }
}
```

---

## 5. 事件目标（Event Targets）

### 5.1 什么是事件目标

事件目标用于访问具有唯一关系的两个作用域之间的一个。游戏知道所有事件目标的作用域类型，因此不需要前缀。

**完整列表**可在 `event_targets.log` 中查看。

### 5.2 事件目标格式

```
<Input Scope> --[Event Target]--> <Output Scope>
```

**示例：**
```
holder - 获取头衔的持有者
Input Scopes: landed_title
Output Scopes: character
```

### 5.3 常用事件目标

| 事件目标 | 输入作用域 | 输出作用域 | 说明 |
|---------|-----------|-----------|------|
| `holder` | title | character | 头衔持有者 |
| `primary_heir` | character | character | 主要继承人 |
| `spouse` | character | character | 配偶 |
| `liege` | character | character | 领主 |
| `mother` | character | character | 母亲 |
| `father` | character | character | 父亲 |
| `faith` | character | faith | 信仰 |
| `culture` | character | culture | 文化 |
| `religious_head` | faith | character | 宗教领袖 |
| `title_holder` | title | character | 头衔持有者 |
| `de_jure_liege` | title | title | 法理领主 |
| `realm_capital` | character | title | 领地首都 |

### 5.4 链式调用

事件目标可以用点号链式调用：

```
# 方法1：点号链式
title:k_france.holder = {
    # 法兰西国王
}

# 方法2：代码块嵌套（等效）
title:k_france = {
    holder = {
        # 法兰西国王
    }
}

# 更长的链式调用
title:k_france.holder.spouse = {
    # 法兰西国王的配偶
}
```

### 5.5 特殊事件目标

#### this - 当前作用域

`this` 指代当前作用域，主要用于作用域比较或作为参数传递。

```
county.holder = {
    OR = {
        this = root
        this = root.primary_spouse
    }
}
```

#### prev - 上一个作用域

`prev` 指代上一个作用域，常用于返回上一级上下文或作为参数。

```
title:k_france = {
    holder = {
        prev = {
            # 回到 title:k_france 上下文
        }
    }
}
```

**注意：**
- CK3中 `prev` **不能**链式调用（不同于CK2）
- `prev = { prev = {` 会回到原始作用域

---

## 6. 保存的作用域（Saved Scopes）

### 6.1 什么是保存的作用域

保存的作用域是一个命名的指针，指向特定作用域，使用语法 `scope:<name>`。

### 6.2 代码提供的保存作用域

某些功能会预先提供保存的作用域：

**角色互动（Character Interactions）：**
- `scope:actor` - 发起互动的角色
- `scope:recipient` - 接收互动的角色

**on_actions：**
- 查看文件中的注释，了解可用的保存作用域

### 6.3 脚本中保存作用域

使用 `save_scope_as` 效果保存当前作用域：

```
title:k_france.holder = {
    save_scope_as = king_of_france
}

# 之后可以随时访问
scope:king_of_france = {
    # 法兰西国王上下文
}
```

### 6.4 保存作用域的生命周期

- 保存的作用域在**未中断的效果链**中持续存在
- 如果事件A保存了作用域，然后触发事件B，事件B中可以访问该作用域
- 当效果链结束时，保存的作用域自动清除
- 可以使用 `clear_saved_scope` 手动清除

### 6.5 临时保存作用域

使用 `save_temporary_scope_as`：

- 可以在效果或触发器中使用
- 不会跨效果链传递
- 在当前效果/触发器块结束时过期

```
any_child = {
    age > 10
    save_temporary_scope_as = teenage_child
}
```

### 6.6 命名冲突

同一时间只能有一个特定名称的保存作用域。保存同名作用域会覆盖之前的。

---

## 7. 列表构建器（List-builders）

### 7.1 什么是列表构建器

当作用域之间存在**一对多**关系时，无法使用事件目标（因为会产生歧义）。此时使用列表构建器来访问列表中的多个作用域。

**示例：**
- 一个母亲可以有多个孩子 → 不能使用 `child` 事件目标
- 使用 `every_child` 列表构建器遍历所有孩子

### 7.2 every_X - 遍历所有

遍历列表中的所有作用域，为每个执行效果。

```
every_child = {
    add_gold = 10
}
# 每个子女获得10金币
```

**使用 limit 过滤：**
```
every_child = {
    limit = { is_female = yes }
    add_gold = 10
}
# 每个女性子女获得10金币
```

**结合 prev 使用：**
```
every_child = {
    limit = { is_female = yes }
    prev = {
        add_gold = 10
    }
}
# 当前角色为每个女性子女获得10金币
```

**注意：** 在 `every_X` 中保存作用域，只有最后一个会被保存。

### 7.3 random_X - 随机选择

随机选择列表中的一个作用域执行效果。

```
random_child = {
    add_gold = 10
}
# 一个随机子女获得10金币
```

**使用 limit 过滤：**
```
random_child = {
    limit = { is_female = yes }
    save_scope_as = random_daughter
}
# 保存一个随机女性子女
```

### 7.4 ordered_X - 排序选择

按指定值排序后选择作用域。

```
ordered_child = {
    order_by = age
    add_gold = 10
}
# 最年长的子女获得10金币
```

**参数：**
- `order_by` - 排序依据（可以是命名值或脚本值）
- `position` - 指定索引（从0开始）
- `min` / `max` - 范围限制
- `check_range_bounds` - 避免范围超出列表大小时的错误

```
ordered_child = {
    limit = { is_female = yes }
    order_by = age
    position = 1
    add_gold = 10
}
# 第二年长的女儿获得10金币
```

### 7.5 any_X - 触发器检查

在触发器块中使用，检查列表中是否有满足条件的作用域。

```
any_child = {
    age > 10
}
# 如果有任何子女年龄大于10，返回true
```

**使用 filter 过滤：**
```
any_child = {
    filter = { is_female = yes }
    age > 10
}
# 如果有任何女性子女年龄大于10，返回true
```

**保存临时作用域：**
```
any_child = {
    filter = { is_female = yes }
    age > 10
    save_temporary_scope_as = teenage_daughter
}
```

**count 参数：**
```
any_child = {
    condition = { is_female = yes }
    age > 10
    count >= 2
}
# 如果至少2个女性子女年龄大于10，返回true
```

**percent 参数：**
```
any_child = {
    condition = { is_female = yes }
    age > 10
    percent >= 0.5
}
# 如果至少一半的女性子女年龄大于10，返回true
```

---

## 8. 保存的作用域值

### 8.1 什么是保存的作用域值

保存的作用域值是一个命名的指针，指向特定的**原始作用域**（数字、布尔值或标志值），使用语法 `scope:<name>`。

### 8.2 代码提供的保存作用域值

某些功能会提供保存的作用域值：

**角色互动选项：**
- `scope:option_1` - 布尔值，表示选项1是否被选中

### 8.3 脚本中保存作用域值

使用 `save_scope_value_as` 效果：

```
save_scope_value_as = {
    name = some_name
    value = <boolean>/<number>/<flag value>
}
```

**示例：**
```
save_scope_value_as = {
    name = cost
    value = 100
}

# 使用
add_gold = scope:cost
```

### 8.4 临时保存作用域值

使用 `save_temporary_scope_value_as`：

- 可以在效果或触发器中使用
- 遵循与保存的作用域相同的可用性规则

---

## 附录：常用事件目标速查表

### 角色相关

| 事件目标 | 说明 |
|---------|------|
| `primary_heir` | 主要继承人 |
| `spouse` | 配偶 |
| `liege` | 领主 |
| `mother` | 母亲 |
| `father` | 父亲 |
| `dynasty` | 宗族 |
| `house` | 家族 |
| `faith` | 信仰 |
| `culture` | 文化 |
| `realm_capital` | 领地首都 |

### 头衔相关

| 事件目标 | 说明 |
|---------|------|
| `holder` | 头衔持有者 |
| `de_jure_liege` | 法理领主 |
| `de_facto_liege` | 事实领主 |

### 信仰相关

| 事件目标 | 说明 |
|---------|------|
| `religious_head` | 宗教领袖 |
| `religious_head_title` | 宗教领袖头衔 |

### 特殊

| 事件目标 | 说明 |
|---------|------|
| `root` | 根作用域 |
| `prev` | 上一个作用域 |
| `this` | 当前作用域 |

---

## 附录：列表构建器速查表

| 构建器 | 类型 | 说明 |
|--------|------|------|
| `every_X` | 效果 | 遍历所有 |
| `random_X` | 效果 | 随机选择一个 |
| `ordered_X` | 效果 | 排序后选择 |
| `any_X` | 触发器 | 检查是否有满足条件的 |

**常用列表：**
- `every_child` / `random_child` / `any_child` - 子女
- `every_vassal` / `random_vassal` / `any_vassal` - 封臣
- `every_courtier` / `random_courtier` / `any_courtier` - 廷臣
- `every_ruler` / `random_ruler` / `any_ruler` - 统治者
- `every_living_character` / `random_living_character` / `any_living_character` - 存活角色
- `every_province` / `random_province` / `any_province` - 省份

---

**文档版本**：1.0  
**最后更新**：2026-03-27  
**基于**：CK3 Wiki Scopes页面
