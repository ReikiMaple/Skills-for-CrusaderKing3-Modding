# CK3 Triggers System

> Based on Paradox official Wiki Triggers page.

## 1. Trigger Basics

**Triggers** check conditions and return **true** or **false**.

```
is_ai = yes    # returns true if AI character
```

### Triggers vs Effects

| Type | Purpose | Return | Example |
|------|---------|--------|---------|
| **Triggers** | Check conditions | true/false | `is_ai = yes` |
| **Effects** | Execute operations | none | `add_gold = 100` |

Full list in `triggers.log` (generated via `script_docs` console command).

## 2. Trigger Blocks

| Block | Purpose | Usage |
|-------|---------|-------|
| `trigger = {}` | Standard trigger block | Events, decisions |
| `is_shown = {}` | Visibility check | Decisions, interactions |
| `is_valid = {}` | Validity check | Decisions, interactions |
| `limit = {}` | Condition | if statements, list builders |
| `filter = {}` | Filter | any_X list builders |

### Early Out

Trigger blocks use **early out**: once any condition is false, subsequent triggers are not checked.

```
trigger = {
    is_ai = no              # checked first
    is_independent_ruler = yes
}
```

## 3. Logic Blocks

### AND (default)

```
AND = {
    is_ai = no
    is_independent_ruler = yes
}
```

### OR

```
OR = {
    is_ai = no
    is_independent_ruler = yes
}
```

### NOT

```
NOT = { has_title = title:k_france }
```

### NOR

```
NOR = {
    has_title = title:k_france
    has_title = title:k_aquitaine
}
```

### NAND

```
NAND = {
    has_title = title:k_france
    has_title = title:k_aquitaine
}
```

## 4. Comparison Operators

| Operator | Description |
|----------|-------------|
| `=` | Equality / scope comparison |
| `!=` | Not equal |
| `<` | Less than |
| `<=` | Less than or equal |
| `>` | Greater than |
| `>=` | Greater than or equal |
| `?=` | Safe comparison (checks existence first) |

## 5. trigger_if / trigger_else_if / trigger_else

For conditional checks in trigger blocks:

```
trigger_if = {
    limit = { exists = primary_spouse }
    culture = primary_spouse.culture
}
trigger_else_if = {
    limit = { exists = liege }
    culture = liege.culture
}
trigger_else = {
    has_culture = culture:english
}
```

## 6. Inline Values from Triggers

Triggers that check a value can also return it:

```
add_gold = age         # add gold equal to character's age
add_gold = gold        # add gold equal to current gold
```

Complex triggers with targets:

```
add_gold = "opinion(liege)"  # quotes required
```

## 7. Scripted Triggers

```
# common/scripted_triggers/my_triggers.txt
is_powerful_vassal = {
    is_ai = no
    is_vassal = yes
    monthly_prestige > 5
}
```

Usage:

```
limit = { is_powerful_vassal = yes }
```

Can take parameters:

```
is_same_family = {
    dynasty = $DYNASTY$
}

# Usage
is_same_family = { DYNASTY = scope:other.dynasty }
```

## 8. any_ List Builders (Trigger Only)

```
any_child = {
    is_male = yes
}
# returns true if any child is male
```

Can have `count`:

```
any_child = {
    count = 3
    is_male = yes
}
# returns true if at least 3 children are male
```

## 9. Logical Operators Summary

- `AND` - all true
- `OR` - any true
- `NOT` - all false (single condition)
- `NOR` - all false
- `NAND` - any false
