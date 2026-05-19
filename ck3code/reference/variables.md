# CK3 Variables System

> Based on Paradox official Wiki Variables page.

## 1. Variable Basics

**Variables** store information in CK3 scripts until manually removed.

- Variable names are arbitrary strings, defined on first use
- No predefined variable list
- Variables persist until removed or their scope is destroyed
- Character variables are cleared on character death

## 2. Setting Variables

### Basic Syntax

```
set_variable = {
    name = X
    value = Y
}
```

### Boolean

```
set_variable = {
    name = my_flag
    value = yes
}

# Short form (equivalent)
set_variable = my_flag
```

### Numeric

```
set_variable = {
    name = test
    value = 2.37
}

# Using script math
set_variable = {
    name = test
    value = {
        value = 5
        add = 2
        multiply = 3
    }
}
# Result: 21

# Using script value
set_variable = {
    name = test
    value = some_script_value
}

# Using trigger return value
set_variable = {
    name = test
    value = prestige
}
```

### Flag Value

```
set_variable = {
    name = test
    value = flag:some_flag
}
```

### Scope Variable (Pointer)

```
set_variable = {
    name = my_friend
    value = scope:some_scope
}
```

## 3. Modifying Variables

### Replacement

Setting a variable with the same name replaces it:

```
set_variable = { name = test value = 100 }
set_variable = { name = test value = yes }  # replaced with boolean
```

### Arithmetic

Using `change_variable`:

```
change_variable = {
    name = test
    add = 10
}

change_variable = {
    name = test
    multiply = 2
}
```

Note: Only `add` and `multiply` available (no subtract/divide).

## 4. Removing Variables

```
remove_variable = my_variable
```

Auto-removed when the scope is destroyed or character dies.

## 5. Accessing Variables

```
# In triggers
var:my_variable > 5

# In effects
add_gold = var:some_variable

# In script values
value = var:my_var

# Chaining
scope:someone.var:my_var.father.var:other_var
```

### Existence Check

```
exists = var:my_variable
```

## 6. Global Variables

```
set_global_variable = {
    name = my_global
    value = 100
}

# Access
global_var:my_global > 50
```

Persist in save file. Accessible from anywhere.

## 7. Local Variables

```
set_local_variable = {
    name = temp
    value = 42
}

# Access
local_var:temp
```

Gone when the current block ends.

## 8. Dead Character Variables

```
set_variable = {
    name = legacy
    value = 100
    days = 36500  # survives 50 years after death
}

# Access
scope:dead_char.dead_var:legacy
```

## Variable Type Summary

| Type | Access | Storage |
|------|--------|---------|
| Normal | `var:` | On scope (lost on death) |
| Global | `global_var:` | Gamestate (anywhere) |
| Local | `local_var:` | Temporary (gone when block ends) |
| Dead | `dead_var:` | Dead character (requires duration) |
