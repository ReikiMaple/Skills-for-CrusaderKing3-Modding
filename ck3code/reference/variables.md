# CK3 变量（Variables）系统详解

> 本文档基于Paradox官方Wiki的Variables页面整理，介绍CK3脚本中变量的概念、类型和使用方法。

---

## 目录

1. [变量基础概念](#1-变量基础概念)
2. [设置变量](#2-设置变量)
3. [修改变量](#3-修改变量)
4. [删除变量](#4-删除变量)
5. [访问变量](#5-访问变量)
6. [全局变量](#6-全局变量)
7. [局部变量](#7-局部变量)
8. [变量类型总结](#8-变量类型总结)

---

## 1. 变量基础概念

### 1.1 什么是变量

**变量（Variable）**用于在CK3脚本中存储信息，直到被手动移除。变量可以存储在特定的作用域上，并在该作用域内访问。

### 1.2 变量的特点

- 变量名是任意字符串，设置时即定义
- 没有预定义的变量列表
- 变量会一直存在直到被移除或作用域被销毁
- 角色死亡时，其上的变量会被清除

---

## 2. 设置变量

### 2.1 基本语法

使用 `set_variable` 效果在特定作用域上设置变量：

```
set_variable = {
    name = X
    value = Y
}
```

### 2.2 布尔值变量

**完整形式：**
```
set_variable = {
    name = my_flag
    value = yes
}
```

**简单形式（等效）：**
```
set_variable = my_flag
```

**注意：** 这与 `add_character_flag` 效果等效：
```
add_character_flag = my_flag
```

### 2.3 数值变量

**设置具体数值：**
```
set_variable = {
    name = test
    value = 2.37
}
```

**使用脚本数学计算：**
```
set_variable = {
    name = test
    value = {
        value = 5
        add = 2
        multiply = 3
    }
}
# 结果：21
```

**使用脚本值：**
```
set_variable = {
    name = test
    value = some_script_value
}
```

**使用触发器返回值：**
```
set_variable = {
    name = test
    value = prestige
}

set_variable = {
    name = test
    value = "culture.cultural_acceptance(culture:french)"
}
```

### 2.4 标志值变量

```
set_variable = {
    name = test
    value = flag:some_flag
}
```

### 2.5 作用域变量

变量可以存储作用域（不是复制，而是指针）：

```
set_variable = {
    name = my_friend
    value = scope:some_scope
}

# 也可以使用其他方式访问作用域
set_variable = {
    name = my_liege
    value = liege
}

set_variable = {
    name = france_holder
    value = title:k_france.holder
}
```

---

## 3. 修改变量

### 3.1 替换变量

如果变量已存在，使用相同名称设置新变量会替换原有变量，即使类型不同：

```
# 先设置为数值
set_variable = {
    name = test
    value = 100
}

# 替换为布尔值
set_variable = {
    name = test
    value = yes
}
```

### 3.2 数值运算

使用 `change_variable` 对数值变量进行运算：

```
# 加法
change_variable = {
    name = test
    add = 10
}

# 乘法
change_variable = {
    name = test
    multiply = 2
}
```

**注意：** 只能使用 `add` 和 `multiply`，没有 `subtract` 或 `divide`。

---

## 4. 删除变量

### 4.1 手动删除

使用 `remove_variable` 效果：

```
remove_variable = my_variable
```

### 4.2 自动删除时机

变量会在以下情况自动删除：
- 手动在脚本中移除
- 存储变量的作用域被销毁
- 如果是角色变量，当角色死亡时

### 4.3 最佳实践

为避免存档膨胀，不再使用的变量应及时删除：

```
# 使用变量后删除
if = {
    limit = { has_variable = temp_var }
    add_gold = var:temp_var
    remove_variable = temp_var
}
```

---

## 5. 访问变量

### 5.1 基本访问

使用 `var:` 前缀从设置变量的同一作用域访问：

```
# 设置
set_variable = {
    name = my_var
    value = 100
}

# 访问
add_gold = var:my_var

# 检查存在
has_variable = my_var
```

### 5.2 链式访问

与事件目标类似，变量可以链式访问：

```
# 从保存的作用域访问变量
scope:some_scope.var:some_var

# 从其他角色访问
liege.var:tax_rate

# 从头衔访问
title:k_france.var:custom_data
```

### 5.3 变量存储作用域时的链式调用

如果变量存储的是作用域，可以继续链式调用事件目标：

```
# 假设 var:some_var 存储了一个角色
scope:some_scope.var:some_var.father

# 可以继续链式调用
scope:some_scope.var:some_var.father.var:other_var
```

### 5.4 在触发器中使用

```
trigger = {
    var:my_var >= 100
}
```

### 5.5 在UI中显示

```
"[Scope.GetVariable('my_var').GetValue]"
```

---

## 6. 全局变量

### 6.1 什么是全局变量

全局变量存储在游戏状态本身，可以从任何上下文访问。

### 6.2 全局变量操作

**设置：**
```
set_global_variable = {
    name = global_counter
    value = 0
}
```

**修改：**
```
change_global_variable = {
    name = global_counter
    add = 1
}
```

**删除：**
```
remove_global_variable = global_counter
```

**访问：**
```
add_gold = global_var:global_counter
```

**检查存在：**
```
has_global_variable = global_counter
```

### 6.3 全局变量 vs 普通变量

| 特性 | 普通变量 | 全局变量 |
|------|----------|----------|
| 存储位置 | 特定作用域 | 游戏状态 |
| 访问范围 | 同一作用域 | 任何上下文 |
| 自动删除 | 作用域销毁时 | 不会自动删除 |
| 使用前缀 | `var:` | `global_var:` |

---

## 7. 局部变量

### 7.1 什么是局部变量

局部变量存储在顶层作用域（Top Scope）上，在同一顶层作用域内的任何上下文都可以访问。

由于顶层作用域是临时的，局部变量比普通变量更短暂。在大多数情况下，使用保存的作用域或保存的作用域值更实用。

### 7.2 局部变量操作

**设置：**
```
set_local_variable = {
    name = local_temp
    value = 100
}
```

**修改：**
```
change_local_variable = {
    name = local_temp
    add = 10
}
```

**删除：**
```
remove_local_variable = local_temp
```

**访问：**
```
add_gold = local_var:local_temp
```

### 7.3 局部变量 vs 其他变量

| 特性 | 普通变量 | 全局变量 | 局部变量 |
|------|----------|----------|----------|
| 存储位置 | 特定作用域 | 游戏状态 | 顶层作用域 |
| 访问范围 | 同一作用域 | 任何上下文 | 同一顶层作用域 |
| 持久性 | 作用域存在期间 | 永久 | 顶层作用域存在期间 |
| 使用前缀 | `var:` | `global_var:` | `local_var:` |

---

## 8. 变量类型总结

### 8.1 四种变量类型对比

| 类型 | 设置效果 | 修改效果 | 删除效果 | 访问前缀 | 存储位置 |
|------|----------|----------|----------|----------|----------|
| **普通变量** | `set_variable` | `change_variable` | `remove_variable` | `var:` | 特定作用域 |
| **全局变量** | `set_global_variable` | `change_global_variable` | `remove_global_variable` | `global_var:` | 游戏状态 |
| **局部变量** | `set_local_variable` | `change_local_variable` | `remove_local_variable` | `local_var:` | 顶层作用域 |
| **死亡角色变量** | `set_dead_character_variable` | - | - | `dead_var:` | 死亡角色 |

### 8.2 变量可存储的值类型

| 值类型 | 示例 |
|--------|------|
| **布尔值** | `value = yes/no` |
| **数值** | `value = 100` 或 `value = 2.5` |
| **标志值** | `value = flag:some_flag` |
| **作用域** | `value = scope:target` 或 `value = liege` |

### 8.3 使用建议

| 场景 | 推荐变量类型 |
|------|-------------|
| 角色临时数据 | 普通变量（及时删除） |
| 跨事件传递数据 | 保存的作用域值 |
| 游戏全局计数器 | 全局变量 |
| 临时计算 | 局部变量或脚本值 |
| 角色死亡后仍需保留 | 全局变量 |

---

## 附录：变量操作速查表

### 设置变量

```
# 普通变量
set_variable = {
    name = my_var
    value = 100
}
set_variable = my_flag    # 布尔值简写

# 全局变量
set_global_variable = {
    name = global_var
    value = yes
}

# 局部变量
set_local_variable = {
    name = local_var
    value = flag:my_flag
}
```

### 修改变量

```
# 加法
change_variable = {
    name = my_var
    add = 10
}

# 乘法
change_variable = {
    name = my_var
    multiply = 2
}
```

### 删除变量

```
remove_variable = my_var
remove_global_variable = global_var
remove_local_variable = local_var
```

### 访问变量

```
# 在效果中
add_gold = var:my_var
add_gold = global_var:global_counter
add_gold = local_var:local_temp

# 在触发器中
var:my_var >= 100
global_var:counter > 0

# 链式访问
scope:target.var:stored_value
liege.var:tax_rate

# 在UI中
"[Scope.GetVariable('my_var').GetValue]"
"[GetGlobalVariable('global_var').GetValue]"
```

### 检查变量存在

```
has_variable = my_var
has_global_variable = global_var
has_local_variable = local_var
```

---

**文档版本**：1.0  
**最后更新**：2026-03-27  
**基于**：CK3 Wiki Variables页面
