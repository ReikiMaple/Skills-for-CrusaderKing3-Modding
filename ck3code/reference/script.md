# CK3 Mod Script Language Guide

> Based on Paradox official Wiki Scripting page.

## 1. Language Overview

### What is Jomini Script

CK3 uses **Jomini Script** (Paradox Scripting Language) on the **Clausewitz** engine.

Used in:
- `common/` folder: define decisions, events, religions, cultures, etc.
- `events/` folder: write event logic

### Hardcoded Limitations

- AI behavior logic
- Army behavior logic
- UI system (except Scripted GUI)
- Core game mechanics algorithms

### Three Core Function Types

| Type | Purpose | Usage Location |
|------|---------|----------------|
| **Effects** | Execute operations, modify game state | `immediate = {}`, `effect = {}`, `on_accept = {}` |
| **Triggers** | Check conditions, return true/false | `limit = {}`, `trigger = {}` |
| **Event Targets** | Switch scopes | Anywhere scope switching is needed |

## 2. Basic Syntax

### Structure

```
# Simple assignment
key = value

# Block
key = {
    sub_key = sub_value
}

# Nested block
key = {
    a = b
    e = {
        f = g
    }
}
```

### Examples

```
is_alive = yes                    # boolean
add_gold = 100                    # integer
debug_log = "hello world"         # string
player_heir = { marry = root }    # nested effect
```

### Syntax Rules

| Rule | Description | Example |
|------|-------------|---------|
| Equals sign | Assignment or comparison | `key = value` |
| Curly braces | Define blocks | `{ ... }` |
| Comments | Using `#` | `# this is a comment` |
| Quotes | Strings need quotes | `"hello"` |
| Indentation | No effect on execution, readability only | Tabs or 4 spaces |

### Special Syntax: Triggers with Targets

```
# Quotes required for complex expressions
add_gold = "opinion(liege)"
```

## 3. Scope System

### What are Scopes

Scopes are game entity objects like characters, titles, faiths, etc. Effects and triggers must be used on the correct scope type.

### Common Scopes

| Scope | Description | Example Trigger |
|--------|-------------|----------------|
| `character` | Character | `age`, `is_alive` |
| `title` | Title | `tier`, `is_landed` |
| `county` | County | `development`, `culture` |
| `faith` | Faith | `religious_head`, `fervor` |
| `culture` | Culture | `traditions`, `era` |

### Event Targets (Scope Switching)

```
primary_heir          # primary heir
spouse               # spouse
liege                # liege
realm_capital        # realm capital
title_holder         # title holder
de_jure_liege        # de jure liege
faith                # faith
religious_head       # religious head
culture              # culture
```

### Chaining

```
# Dot-chain
primary_heir.faith.religious_head

# Block nesting (equivalent)
primary_heir = {
    faith = {
        religious_head = { }
    }
}
```

### Direct Database Access

```
set_culture = culture:english
set_character_faith = faith:orthodox
capital_county = title:c_byzantion
holder = title:k_england
marry = character:123456
```

## 4. Keywords

| Keyword | Purpose | Example |
|---------|---------|---------|
| `root` | Root object of the script | `primary_heir = { set_relation_grudge = root }` |
| `prev` | Previous scope | Used to return to previous object |
| `this` | Current scope | `this = root` |

### Saved Scopes

```
primary_heir = { save_scope_as = my_son }
scope:my_son = { death = natural }
```

## 5. Operators

| Operator | Description |
|----------|-------------|
| `=` | Equality / scope comparison |
| `!=` | Not equal |
| `<`, `<=`, `>`, `>=` | Value comparison |
| `?=` | Safe comparison (checks existence first) |

### Logic Operators

`AND`, `OR`, `NOT`, `NOR`, `NAND`

## 6. Conditional Statements

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

### switch

```
switch = {
    trigger = has_culture
    culture:english = { add_gold = 10 }
    culture:french = { add_gold = 20 }
    fallback = { add_gold = 5 }
}
```

### while

```
while = {
    count = 10
    add_gold = 100
}
```

## 7. Lists & Iterators

```
every_child = {
    limit = { is_male = yes }
    add_gold = 100
}

ordered_child = {
    order_by = age
    max = 3
    add_gold = age
}
```

**Do not use `any_` in script values or effects** - they are for triggers only.

## 8. Debug & Testing

```
# Console commands (with -debug_mode)
effect add_gold = 100
trigger is_ai = yes
event my_event.1
explorer
script_docs
```

### Log effect

```
log = "some text [script_value]"
```
