# CK3 Scopes System

> Based on Paradox official Wiki Scopes page.

## 1. Scope Basics

**Scope** is the mechanism for selecting game entities in CK3 scripts.

### Script Execution Context

Effects and triggers always execute in a specific **context**. Most effects/triggers only work on specific scope types.

### Database Scopes

| Scope Type | Description | Example |
|-----------|-------------|---------|
| `character` | Character | Player character, NPC |
| `title` | Title | Kingdom, duchy, county |
| `county` | County | Land on map |
| `province` | Province | Map province |
| `faith` | Faith | Religious denomination |
| `culture` | Culture | Cultural group |
| `dynasty` | Dynasty | Dynasty |
| `house` | House | Family house |
| `war` | War | Ongoing war |
| `scheme` | Scheme | Scheme activity |

Full list in `event_scopes.log` (generated via `script_docs` console command).

### Primitive Scopes

- Numbers
- Booleans (yes/no)
- Flags (`flag:some_string`)

Cannot be modified or accessed as objects.

## 2. Accessing Scopes

### root

`root` points to the default context of the current block.

**Important:** `root` is NOT the player. CK3 can have multiple players.

```
immediate = {
    title:k_france = {
        root = { }   # back to event recipient
    }
}
```

### Direct Database Access

```
title:k_france = { }
character:123456 = { }
set_culture = culture:english
set_character_faith = faith:orthodox
capital_county = title:c_byzantion
```

Note: Only historical characters can be accessed by ID.

### Prefix References

```
set_culture = culture:english
set_character_faith = faith:orthodox
```

## 3. Context Switching

### Basic Syntax

```
<scope> = {
    # new context
}
```

### Example

```
immediate = {
    # context: event recipient character
    title:k_france = {
        # context: Kingdom of France title
        holder = {
            # context: King of France
        }
        # back to France title
    }
    # back to event recipient
}
```

### Using root to Return

```
root = { }   # return to default context
```

## 4. Event Targets

Complete list in `event_targets.log`.

### Common Event Targets

```
primary_heir, spouse, liege, realm_capital,
primary_holder, de_jure_liege, faith, religious_head, culture,
mother, father, employer, court, court_type,
capital_county, capital_barony, dynasty, house
```

## 5. Saved Scopes

```
primary_heir = { save_scope_as = my_son }
scope:my_son = { death = natural }
```

### Save Scope Value

```
save_scope_value_as = {
    name = cost
    value = primary_heir.age
}
add_gold = scope:cost
```

### In Trigger Blocks

Use `save_temporary_scope_as` and `save_temporary_scope_value_as` instead.

## 6. List-builders

```
every_child = { }         # iterate all
random_child = { }        # pick one random
ordered_child = { }       # ordered iteration
any_child = { }           # triggers only
```

## 7. Chaining

```
# Dot-chain
scope:someone.var:my_var.father.var:other_var

# Not allowed: prevprev, prev.prev
```
