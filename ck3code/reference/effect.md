# CK3 Effects System

> Based on Paradox official Wiki Effects page.

## 1. Effect Basics

**Effects** change game state. Unlike triggers (which check conditions), effects perform operations and modify game data.

Full list in `effects.log` (generated via `script_docs` console command).

### Effects vs Triggers

| Type | Purpose | Example |
|------|---------|---------|
| **Triggers** | Check conditions, return true/false | `is_ai = yes` |
| **Effects** | Execute operations, modify state | `add_gold = 100` |

## 2. Effect Blocks

| Block | Description | Usage |
|-------|-------------|-------|
| `immediate = {}` | Execute immediately on trigger | Events |
| `effect = {}` | Standard effect block | Decisions, interactions |
| `on_accept = {}` | Execute on acceptance | Character interactions |
| `on_decline = {}` | Execute on decline | Character interactions |
| `after = {}` | Execute after option selection | Events |

### Mixed Block Example

```
option = {
    is_shown = { is_ai = yes }      # trigger block
    ai_will_do = { base = 100 }      # AI logic block
    add_gold = 100                   # effect (executed on selection)
}
```

## 3. Effect Syntax Forms

### Boolean Form

```
release_from_prison = yes
clear_traits = yes
end_war = white_peace
```

### Simple Form

**Scope argument:**
```
marry = scope:bride
divorce = scope:spouse
```

**Database key argument:**
```
change_prison_type = house_arrest
add_trait = brave
remove_trait = craven
```

**Value argument:**
```
add_gold = 1000
add_prestige = 500
add_piety = 250
```

### Complex Form (Block)

```
imprison = {
    target = scope:imprisoned_character
    type = house_arrest
}

add_opinion = {
    target = scope:other_character
    modifier = opinion_modifier_name
    value = 20
    days = 365
}
```

## 4. Conditional Effects

### if / else_if / else

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

### while

```
while = {
    count = 10
    add_gold = 100
}

while = {
    limit = { gold > 0 }
    remove_short_term_gold = 50
}
```

Max 1000 iterations. No break.

### switch

```
switch = {
    trigger = has_culture
    culture:english = { add_gold = 10 }
    culture:french = { add_gold = 20 }
    fallback = { add_gold = 5 }
}
```

## 5. Scripted Effects

### Definition

```
# common/scripted_effects/my_effects.txt
my_custom_effect = {
    add_gold = $AMOUNT$
    add_prestige = { value = $AMOUNT$ divide = 2 }
}
```

### Usage

```
my_custom_effect = {
    AMOUNT = 100
}
```

**Text replacement is literal** - happens before evaluation. Important when passing event targets or script values.

## 6. Common Effect Categories

- Gold/Piety/Prestige: `add_gold`, `add_prestige`, `add_piety`
- Traits: `add_trait`, `remove_trait`
- Opinion: `add_opinion`
- Prison: `imprison`, `release_from_prison`
- Marriage: `marry`, `divorce`
- Death: `death`, `kill`
- Title: `create_title`, `grant_title`, `destroy_title`
- War: `declare_war`, `end_war`
- Modifier: `add_modifier`, `remove_modifier`
