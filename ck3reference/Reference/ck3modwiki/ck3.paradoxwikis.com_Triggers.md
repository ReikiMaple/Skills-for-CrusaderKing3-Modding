[Forum list](https://forum.paradoxplaza.com/forum/forums/) [Trending](https://forum.paradoxplaza.com/forum/threads/trending) [Latest](https://forum.paradoxplaza.com/forum/threads/latest) [New posts](https://forum.paradoxplaza.com/forum/threads/newest)

Paradox

[Store](https://www.paradoxplaza.com/) [Mods](https://mods.paradoxplaza.com/) [Forum](https://forum.paradoxplaza.com/forum/forums/) [Launcher](https://play.paradoxplaza.com/) [PDXCON\\
2019](https://pdxcon.paradoxplaza.com/?utm_source=pdxplaza-owned&utm_medium=web-owned&utm_content=topmenu-banner&utm_campaign=pc18_pdxcon_20190412_cawe_ann)

[Paradox Wikis](https://ck3.paradoxwikis.com/Crusader_Kings_III_Wiki)

CK3 Wiki


Active Wikis

[Age of Wonders 4](https://aow4.paradoxwikis.com/) [Empire of Sin](https://eos.paradoxwikis.com/Empire_of_Sin_Wiki) [Cities: Skylines 2](https://cs2.paradoxwikis.com/Cities_Skylines_II_Wiki) [Crusader Kings 3](https://ck3.paradoxwikis.com/Crusader_Kings_III_Wiki) [Europa Universalis 5](https://eu5.paradoxwikis.com/Europa_Universalis_5_Wiki) [Hearts of Iron 4](https://hoi4.paradoxwikis.com/Hearts_of_Iron_4_Wiki) [Hunter: The Reckoning](https://htr.paradoxwikis.com/) [Imperator: Rome](https://imperator.paradoxwikis.com/Imperator_Wiki) [Millennia](https://millennia.paradoxwikis.com/Millennia_Wiki) [Prison Architect](https://prisonarchitect.paradoxwikis.com/) [Stellaris](https://stellaris.paradoxwikis.com/Stellaris_Wiki) [Surviving Mars](https://survivingmars.paradoxwikis.com/Surviving_Mars_Wiki) [Surviving the Aftermath](https://sta.paradoxwikis.com/Surviving_The_Aftermath_Wiki) [Werewolf: the Apocalypse](https://wta.paradoxwikis.com/Werewolf_The_Apocalypse_Wiki) [Vampire: The Masquerade](https://vtm.paradoxwikis.com/VTM_Wiki) [Victoria 3](https://vic3.paradoxwikis.com/Victoria_3_Wiki)

Legacy Wikis

[AoW: Planetfall](https://aowplanetfall.paradoxwikis.com/AoW_Planetfall_Wiki) [Cities: Skylines](https://skylines.paradoxwikis.com/Cities:_Skylines_Wiki) [Crusader Kings 2](https://ck2.paradoxwikis.com/Crusader_Kings_II_Wiki) [Arsenal of Democracy](https://aod.paradoxwikis.com/Main_Page) [Europa Universalis 2](https://eu2.paradoxwikis.com/Main_Page) [Europa Universalis 3](https://eu3.paradoxwikis.com/Europa_Universalis_3_Wiki) [Europa Universalis 4](https://eu4.paradoxwikis.com/Europa_Universalis_4_Wiki) [Europa Universalis: Rome](https://eurome.paradoxwikis.com/Europa_Universalis:_Rome_Wiki) [Hearts of Iron 2](https://hoi2.paradoxwikis.com/Main_Page) [Hearts of Iron 3](https://hoi3.paradoxwikis.com/Hearts_of_Iron_3_Wiki) [Tyranny](https://tyranny.paradoxwikis.com/Tyranny_Wiki) [Victoria 1](https://vic1.paradoxwikis.com/Main_Page) [Victoria 2](https://vic2.paradoxwikis.com/Victoria_2_Wiki)

### Search

### Personal tools

Log in

## Navigation menu

[Visit the main page](https://ck3.paradoxwikis.com/Crusader_Kings_III_Wiki "Visit the main page")

# Triggers

From CK3 Wiki

[Jump to navigation](https://ck3.paradoxwikis.com/Triggers#mw-head) [Jump to search](https://ck3.paradoxwikis.com/Triggers#searchInput)

Please help with verifying or updating older sections of this article.

At least some were last verified for [version](https://ck3.paradoxwikis.com/CK3_Wiki:Versioning "CK3 Wiki:Versioning") 1.7.

This article is for the PC version of Crusader Kings 3 only.

[![a screenshot of the in-game tool to check triggers showing multiple triggers being false or true](https://ck3.paradoxwikis.com/images/thumb/4/42/Trigger_runner.png/300px-Trigger_runner.png)](https://ck3.paradoxwikis.com/File:Trigger_runner.png)

[Enlarge](https://ck3.paradoxwikis.com/File:Trigger_runner.png "Enlarge")

trigger runner

A trigger is a check that returns **true** or **false** for the scope where it's used.

For example, `is_ai = yes` would return **true** for an AI character, and **false** for a player.

This could be used to disable an event for a player, by using it in a trigger block of an event.

Triggers that compare values can also return the value itself.

For example, `add_gold = gold` would add the same amount of gold that the character currently has.

The full list of available code triggers can be found in [triggers.log](https://ck3.paradoxwikis.com/Triggers_list "Triggers list").

Run `script_docs` console command in the game and find the log in Documents\\Paradox Interactive\\Crusader Kings III\\logs.

## Contents

- [1Trigger blocks](https://ck3.paradoxwikis.com/Triggers#Trigger_blocks)
  - [1.1Early out](https://ck3.paradoxwikis.com/Triggers#Early_out)
  - [1.2Logic blocks](https://ck3.paradoxwikis.com/Triggers#Logic_blocks)
    - [1.2.1AND](https://ck3.paradoxwikis.com/Triggers#AND)
    - [1.2.2OR](https://ck3.paradoxwikis.com/Triggers#OR)
    - [1.2.3NOT/NOR/NAND](https://ck3.paradoxwikis.com/Triggers#NOT/NOR/NAND)
  - [1.3Limit blocks](https://ck3.paradoxwikis.com/Triggers#Limit_blocks)
    - [1.3.1if/else\_if](https://ck3.paradoxwikis.com/Triggers#if/else_if)
    - [1.3.2effect list-builders](https://ck3.paradoxwikis.com/Triggers#effect_list-builders)
    - [1.3.3trigger\_if/trigger\_else\_if/trigger\_else](https://ck3.paradoxwikis.com/Triggers#trigger_if/trigger_else_if/trigger_else)
- [2Trigger syntax](https://ck3.paradoxwikis.com/Triggers#Trigger_syntax)
  - [2.1Scope comparison](https://ck3.paradoxwikis.com/Triggers#Scope_comparison)
  - [2.2Value comparison](https://ck3.paradoxwikis.com/Triggers#Value_comparison)
  - [2.3Code triggers](https://ck3.paradoxwikis.com/Triggers#Code_triggers)
    - [2.3.1Basic triggers](https://ck3.paradoxwikis.com/Triggers#Basic_triggers)
    - [2.3.2Simple triggers](https://ck3.paradoxwikis.com/Triggers#Simple_triggers)
    - [2.3.3Complex triggers](https://ck3.paradoxwikis.com/Triggers#Complex_triggers)
    - [2.3.4In-line complex triggers](https://ck3.paradoxwikis.com/Triggers#In-line_complex_triggers)
  - [2.4scripted\_triggers](https://ck3.paradoxwikis.com/Triggers#scripted_triggers)
    - [2.4.1Basic scripted\_triggers](https://ck3.paradoxwikis.com/Triggers#Basic_scripted_triggers)
    - [2.4.2Complex scripted\_triggers](https://ck3.paradoxwikis.com/Triggers#Complex_scripted_triggers)
- [3Logical Operators/Triggers](https://ck3.paradoxwikis.com/Triggers#Logical_Operators/Triggers)
- [4References](https://ck3.paradoxwikis.com/Triggers#References)

## Trigger blocks\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Triggers&veaction=edit&section=1 "Edit section: Trigger blocks") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Triggers&action=edit&section=1 "Edit section: Trigger blocks")\]

Triggers are used in trigger script blocks.

Those usually are either explicitly named so, like an event's `trigger = { }` block, or their name are questions which can be answered by yes or no, like a decision's `is_shown = { }` and `is_valid = { }`.

In some cases, triggers are used in hybrid script blocks that accept triggers amongst other things.

Ex: [weight modifier](https://ck3.paradoxwikis.com/Weight_modifier "Weight modifier")

```
modifier = {
   is_ai = yes
   factor = 0
}
```

In this block, `is_ai = no` is a trigger, but `factor = 0` is an operator.

### Early out\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Triggers&veaction=edit&section=2 "Edit section: Early out") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Triggers&action=edit&section=2 "Edit section: Early out")\]

Unless they are being tooltipped, trigger blocks operate on the so-called "early out" principle.

For a trigger block to be true, all triggers within must be true. "early out" means that as soon as a trigger in the block is evaluated as false, the rest of the triggers in that block are not evaluated.

This is useful to avoid errors.

Ex: the following trigger block checks that the current character scope's primary spouse has the same culture as them. To avoid errors, it first checks that the character \`has\` a spouse to begin with.

```
trigger = {
   exists = primary_spouse
   culture = primary_spouse.culture
}
```

If `exists = primary_spouse` is false, the second trigger is not evaluated.

It is also useful for performance optimization. In a trigger block containing multiple triggers, putting the ones most likely to fail first can significantly reduce the number of triggers checked overall.

Ex: this trigger block checks that the current character scope is a player and an independent ruler.

```
trigger = {
   is_ai = no
   is_independent_ruler = yes
}
```

If this trigger block is evaluated once a year for each character in the game, since most characters in the game are not players, `is_ai = no` will almost always be false, and the 2nd trigger will almost never be evaluated at all.

### Logic blocks\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Triggers&veaction=edit&section=3 "Edit section: Logic blocks") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Triggers&action=edit&section=3 "Edit section: Logic blocks")\]

Trigger blocks can contain several triggers. By default, if all of them are true, the trigger block as a whole is true, but some logic blocks can manipulate that logic.

#### AND\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Triggers&veaction=edit&section=4 "Edit section: AND") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Triggers&action=edit&section=4 "Edit section: AND")\]

```
AND = {
   is_ai = no
   is_independent_ruler = yes
}
```

The `AND` block is true if the current character both is a player and an independent ruler.

#### OR\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Triggers&veaction=edit&section=5 "Edit section: OR") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Triggers&action=edit&section=5 "Edit section: OR")\]

```
OR = {
   is_ai = no
   is_independent_ruler = yes
}
```

The `OR` block is true if the current character scope is either a player \`or\` an independent ruler.

#### NOT/NOR/NAND\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Triggers&veaction=edit&section=6 "Edit section: NOT/NOR/NAND") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Triggers&action=edit&section=6 "Edit section: NOT/NOR/NAND")\]

```
NOT = { has_title = title:k_france }
```

The `NOT` block is true if the current character scope does not hold the Kingdom of France.

To avoid ambiguity, `NOT` should only contain a single trigger. For multiple triggers, using `NOR` or `NAND` makes the intent clear.

```
NAND = {
   has_title = title:k_france
   has_title = title:k_aquitaine
}
```

The `NAND` block is true if the current character scope holds either the Kingdom of France or the Kingdom of Aquitaine or neither of the two. It is false if they hold both titles.

```
NOR = {
   has_title = title:k_france
   has_title = title:k_aquitaine
}
```

The `NOR` block is true if the current character scope holds neither the Kingdom of France nor the Kingdom of Aquitaine. It is false if they hold either of the titles.

### Limit blocks\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Triggers&veaction=edit&section=7 "Edit section: Limit blocks") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Triggers&action=edit&section=7 "Edit section: Limit blocks")\]

The `limit` block is used for conditional effects and triggers.

#### if/else\_if\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Triggers&veaction=edit&section=8 "Edit section: if/else if") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Triggers&action=edit&section=8 "Edit section: if/else if")\]

The most common use of the `limit` block is with the `if`/`else_if` effects, to execute effects only if the `limit` block is true.

Ex: this effect adds gold to the current character scope if they are a player.

```
if = {
   limit = { is_ai = no }
   add_gold = 100
}
```

#### effect list-builders\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Triggers&veaction=edit&section=9 "Edit section: effect list-builders") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Triggers&action=edit&section=9 "Edit section: effect list-builders")\]

Limit blocks are also commonly used to restrict effect list builders.

Ex: this effect adds gold to the current character scope's children if they are male

```
every_child = {
   limit = { is_male = yes }
   add_gold = 100
}
```

Note: the `any_X` list-builder does _not_ use a `limit` block.

#### trigger\_if/trigger\_else\_if/trigger\_else\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Triggers&veaction=edit&section=10 "Edit section: trigger if/trigger else if/trigger else") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Triggers&action=edit&section=10 "Edit section: trigger if/trigger else if/trigger else")\]

`trigger_if` can be used to check a trigger only if the `limit` block is true.

Ex: if the current character scope is not an ai, this trigger checks whether they are an independent ruler

```
trigger_if = {
   limit = { is_ai = no }
   is_independent_ruler = yes
}
```

Conditional triggers are often used in tooltipped trigger blocks both for legibility and to avoid errors, because when tooltipped, early-out does not apply.

Ex: this trigger, when tooltipped, would throw an error when `primary_spouse` does not exist.

```
trigger = {
   exists = primary_spouse
   culture = primary_spouse.culture
}
```

but this would not throw an error, because if the `limit` block is false, the trigger is not evaluated.

```
trigger_if = {
   limit = { exists = primary_spouse }
   culture = primary_spouse.culture
}
```

## Trigger syntax\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Triggers&veaction=edit&section=11 "Edit section: Trigger syntax") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Triggers&action=edit&section=11 "Edit section: Trigger syntax")\]

### Scope comparison\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Triggers&veaction=edit&section=12 "Edit section: Scope comparison") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Triggers&action=edit&section=12 "Edit section: Scope comparison")\]

A scope comparison is a statement with two scopes on either side of an `=` sign. It is true if both objects are the same, and false otherwise.

Scopes in a scope comparison can be database scopes, event targets, saved scopes or variables.

Note: even if both scopes are not the same objects, they do need to be of the same scope type.

Ex: this trigger checks whether whoever holds the kingdom of France is the same character as the father of the current character scope.

```
title:k_france.holder = father
```

In a scope comparison, both sides need to be valid. In this example, the current character must have a father, and the Kingdom of France must be created, otherwise the scope comparison throws an error in the error log, so the existence of both scopes needs to be checked at some point before the comparison is made.

The existence of the scope on the left-hand side of the comparison itself by using `?=`:

```
title:k_france.holder ?= father
```

### Value comparison\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Triggers&veaction=edit&section=13 "Edit section: Value comparison") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Triggers&action=edit&section=13 "Edit section: Value comparison")\]

A value comparison is a statement with two numerical values on either side of either

- an equal sign `=`
- a comparison symbol
  - strictly greater than `>`
  - greater than or equal to `>=`
  - lower than `<`
  - lower than or equal to `<=`

It is true if the comparison is mathematically correct.

Numerical values in a value comparison can be:

- a number
- a named value
- a [script\_value](https://ck3.paradoxwikis.com/index.php?title=Script_value&action=edit&redlink=1 "Script value (page does not exist)")
- a saved scope value
- a [variable](https://ck3.paradoxwikis.com/index.php?title=Variable&action=edit&redlink=1 "Variable (page does not exist)") storing a number

Ex: this trigger checks whether the current character scope's gold is strictly greater than 1000.

```
gold > 1000
```

### Code triggers\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Triggers&veaction=edit&section=14 "Edit section: Code triggers") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Triggers&action=edit&section=14 "Edit section: Code triggers")\]

Code triggers have a predetermined syntax. They usually require a specific scope type context to work.

Code triggers can take several forms:

#### Basic triggers\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Triggers&veaction=edit&section=15 "Edit section: Basic triggers") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Triggers&action=edit&section=15 "Edit section: Basic triggers")\]

Basic triggers check whether the statement has the expected positive or negative result.

Ex: this trigger is true if the current character scope is _not_ an AI.
`is_ai = no`

#### Simple triggers\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Triggers&veaction=edit&section=16 "Edit section: Simple triggers") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Triggers&action=edit&section=16 "Edit section: Simple triggers")\]

Simple triggers check whether they are true depending on the argument provided on the right hand side of the `=` sign.

The argument is either:

- a scope

Ex: this trigger checks whether the current character scope is a vassal of the saved scope `scope:actor`.

```
is_vassal_of = scope:actor
```

- a database key

Ex: this trigger checks whether the current character scope has the trait defined with the `infirm` key.

```
has_trait = infirm
```

#### Complex triggers\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Triggers&veaction=edit&section=17 "Edit section: Complex triggers") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Triggers&action=edit&section=17 "Edit section: Complex triggers")\]

Complex triggers use several parameters in a script block. Those parameters can be a scope, a database key, a numerical value or a flag value.

Ex: this trigger checks whether the current character scope has an active scheme of the murder type targeting their liege.

```
is_scheming_against = {
  target = liege
  type = murder
}
```

Some code triggers have both a simple form and a complex form.

#### In-line complex triggers\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Triggers&veaction=edit&section=18 "Edit section: In-line complex triggers") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Triggers&action=edit&section=18 "Edit section: In-line complex triggers")\]

Some complex triggers can be written in one line to return a value.

It is written in quotation marks, with the additional argument in brackets.

For example, a script value would look like this:

```
distance_to_liege_sval = {
  value = "realm_to_title_distance_squared(liege.capital_county)"
}
```

This feature is not documented and doesn't work with all triggers. From testing, it seems to only support triggers with this line in their description: `Traits: <, <=, =, !=, >, >=`

If a trigger has multiple arguments, like `has_trait_xp` which requires trait and track, they are added with a \|

`value = "has_trait_xp(lifestyle_traveler|danger)"`

So far, this is the only known trigger with this multi-argument syntax.

### scripted\_triggers\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Triggers&veaction=edit&section=19 "Edit section: scripted triggers") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Triggers&action=edit&section=19 "Edit section: scripted triggers")\]

Scripted\_triggers are macros that enable replacing a set of triggers with a single statement, to make script more legible and avoid repetition.

They are usually defined in `common/scripted_triggers`, and can then be used anywhere triggers are allowed.

They are sometimes defined locally in event files (see [events](https://ck3.paradoxwikis.com/Events "Events")), in which case they can only be used in events from the same file.

#### Basic scripted\_triggers\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Triggers&veaction=edit&section=20 "Edit section: Basic scripted triggers") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Triggers&action=edit&section=20 "Edit section: Basic scripted triggers")\]

Simple scripted\_triggers check whether a predetermined set of triggers is evaluated as a whole as true (`= yes`) or false (`= no`).

Ex: if the following set of triggers is repeatedly used to check whether a character is a rich adult independent ruler:

```
is_independent_ruler = yes
is_adult = yes
gold > 1000
```

instead of repeating the same set of triggers in different places, they can be defined as a scripted\_trigger:

```
is_rich_adult_independent_ruler = {
   is_adult = yes
   is_independent_ruler = yes
   gold > 1000
}
```

and anywhere that set of triggers needs to be checked, it can be replaced by the following statement:
`is_rich_adult_independent_ruler = yes`

Using the negative version

```
is_rich_adult_independent_ruler = no
```

is the same as using a `NOT` logic block

```
NOT = { is_rich_adult_independent_ruler = yes }
```

Because scripted\_triggers can be used in a variety of different contexts, it is advised not to use in their definition ambiguous event targets such as `root` or `prev`.

#### Complex scripted\_triggers\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Triggers&veaction=edit&section=21 "Edit section: Complex scripted triggers") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Triggers&action=edit&section=21 "Edit section: Complex scripted triggers")\]

Scripted\_triggers can also have a complex form that handles literal text replacement, allowing to pass arguments.

For example, if the following set of triggers are used to check that the current character scope is a vassal of the King of France and related to them:

```
is_vassal_of = title:k_france.holder
is_close_family_of = title:k_france.holder
```

that set of triggers can be defined as a scripted\_trigger, but instead of referencing `title:k_france.holder` specifically, the scripted\_trigger uses an argument defined in uppercase letters wrapped in two `$` signs:

```
is_related_vassal_of = {
   is_vassal_of = $TARGET$
   is_close_family_of = $TARGET$
}
```

When used, the complex form of the scripted\_trigger specifies what the expected argument is, by using the same name but without the `$` signs:

```
is_related_vassal_of = {
   TARGET = title:k_france.holder
}
```

With that form, every occurrence of `$TARGET$` in the scripted\_trigger will be _literally_ replaced with the argument provided: the text replacement happens _before_ the scripted\_trigger is evaluated.

## Logical Operators/Triggers\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Triggers&veaction=edit&section=22 "Edit section: Logical Operators/Triggers") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Triggers&action=edit&section=22 "Edit section: Logical Operators/Triggers")\]

These triggers provide basic logical functionality.

| Name | Description | Usage | Traits | Supported Scopes | Supported Targets |
| --- | --- | --- | --- | --- | --- |
| always | Always the same value | always = yes | yes/no |  |  |
| AND | All inside trigger must be true | AND = { <triggers> } |  |  |  |
| OR | At least one entry inside trigger must be true | OR = { <triggers> } |  |  |  |
| NOT | Negates content of trigger | NOT = { <triggers> } |  |  |  |
| NOR | A negated OR trigger | NOR = { <triggers> } |  |  |  |
| NAND | A negated AND trigger | NAND = { <triggers> } |  |  |  |
| all\_false | True if all children are false (equivalent to NOR) | all\_false = { <triggers> } |  |  |  |
| any\_false | True if any child is false (equivalent to NAND) | any\_false = { <triggers> } |  |  |  |
| switch | Switch on a trigger for the evaluation of another trigger with an optional fallback trigger | switch = {<br>trigger = simple\_assign\_trigger<br>case\_1 = { <triggers> }<br>case\_2 = { <triggers> }<br>case\_n = { <triggers> }<br>fallback = { <triggers> }<br>} |  |  |  |
| trigger\_if | Evaluates the triggers if the display\_triggers of the limit are met | trigger\_if = { limit = { <display\_triggers> } <triggers> } |  |  |  |
| trigger\_else\_if | Evaluates the enclosed triggers if the display\_triggers of the preceding \`trigger\_if\` or \`trigger\_else\_if\` is not met and its own display\_trigger of the limit is met | trigger\_if = { limit = { <display\_triggers> } <triggers> }<br>trigger\_else\_if = { limit = { <display\_triggers> } <triggers> } |  |  |  |
| trigger\_else | Evaluates the triggers if the display\_triggers of preceding 'trigger\_if' or 'trigger\_else\_if' is not met | trigger\_if = { limit = { <display\_triggers> } <triggers> }<br>trigger\_else = { <triggers> } |  |  |  |

## References\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Triggers&veaction=edit&section=23 "Edit section: References") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Triggers&action=edit&section=23 "Edit section: References")\]

**[Modding](https://ck3.paradoxwikis.com/Modding "Modding")**

|     |     |
| --- | --- |
| Documentation | [Scripting](https://ck3.paradoxwikis.com/Scripting "Scripting") • [Scopes](https://ck3.paradoxwikis.com/Scopes "Scopes") • [Effects](https://ck3.paradoxwikis.com/Effects "Effects") • Triggers • [Variables](https://ck3.paradoxwikis.com/Variables "Variables") • [Modifiers](https://ck3.paradoxwikis.com/Modifier_list "Modifier list") |

|     |     |
| --- | --- |
| Scripting | [AI](https://ck3.paradoxwikis.com/AI_modding "AI modding") • [Bookmarks](https://ck3.paradoxwikis.com/Bookmarks_modding "Bookmarks modding") • [Characters](https://ck3.paradoxwikis.com/Characters_modding "Characters modding") • [Commands](https://ck3.paradoxwikis.com/Commands "Commands") • [Council](https://ck3.paradoxwikis.com/Council_modding "Council modding") • [Culture](https://ck3.paradoxwikis.com/Culture_modding "Culture modding") • [Decisions](https://ck3.paradoxwikis.com/Decisions_modding "Decisions modding") • [Dynasties](https://ck3.paradoxwikis.com/Dynasties_modding "Dynasties modding") • [Events](https://ck3.paradoxwikis.com/Event_modding "Event modding") • [Governments](https://ck3.paradoxwikis.com/Governments_modding "Governments modding") • [History](https://ck3.paradoxwikis.com/History_modding "History modding") • [Holdings](https://ck3.paradoxwikis.com/Holdings_modding "Holdings modding") • [Lifestyles](https://ck3.paradoxwikis.com/Lifestyles_modding "Lifestyles modding") • [Regiments](https://ck3.paradoxwikis.com/Regiments_modding "Regiments modding") • [Religions](https://ck3.paradoxwikis.com/Religions_modding "Religions modding") • [Script Values](https://ck3.paradoxwikis.com/Script_values "Script values") • [Story cycles](https://ck3.paradoxwikis.com/Story_cycles_modding "Story cycles modding") • [Struggles](https://ck3.paradoxwikis.com/Struggle_modding "Struggle modding") • [Titles](https://ck3.paradoxwikis.com/Title_modding "Title modding") • [Traits](https://ck3.paradoxwikis.com/Trait_modding "Trait modding") |

|     |     |
| --- | --- |
| Interface | [Interface](https://ck3.paradoxwikis.com/Interface "Interface") • [Data types](https://ck3.paradoxwikis.com/Data_types "Data types") • [Localization](https://ck3.paradoxwikis.com/Localization "Localization") • [Customizable localization](https://ck3.paradoxwikis.com/Customizable_localization "Customizable localization") • [Flavorization](https://ck3.paradoxwikis.com/Flavorization "Flavorization") |

|     |     |
| --- | --- |
| Map | [Map](https://ck3.paradoxwikis.com/Map_modding "Map modding") • [Terrain](https://ck3.paradoxwikis.com/Terrain_modding "Terrain modding") |

|     |     |
| --- | --- |
| Graphics | [3D models](https://ck3.paradoxwikis.com/3D_models "3D models") • [Exporters](https://ck3.paradoxwikis.com/Exporters "Exporters") • [Coat of arms](https://ck3.paradoxwikis.com/Coat_of_arms_modding "Coat of arms modding") • [Graphical assets](https://ck3.paradoxwikis.com/Graphical_assets "Graphical assets") • [Fonts](https://ck3.paradoxwikis.com/Fonts "Fonts") • [Particles](https://ck3.paradoxwikis.com/index.php?title=Particles&action=edit&redlink=1 "Particles (page does not exist)") • [Shaders](https://ck3.paradoxwikis.com/index.php?title=Shaders&action=edit&redlink=1 "Shaders (page does not exist)") • [Unit models](https://ck3.paradoxwikis.com/index.php?title=Unit_models&action=edit&redlink=1 "Unit models (page does not exist)") |

|     |     |
| --- | --- |
| Audio | [Music](https://ck3.paradoxwikis.com/Music_modding "Music modding") • [Sound](https://ck3.paradoxwikis.com/Sound_modding "Sound modding") |

|     |     |
| --- | --- |
| Other | [Console commands](https://ck3.paradoxwikis.com/Console_commands "Console commands") • [Checksum](https://ck3.paradoxwikis.com/Checksum "Checksum") • [Mod structure](https://ck3.paradoxwikis.com/Mod_structure "Mod structure") • [Mod compatibility](https://ck3.paradoxwikis.com/Mod_compatibility "Mod compatibility") • [Modding tools](https://ck3.paradoxwikis.com/Modding_tools "Modding tools") • [Troubleshooting](https://ck3.paradoxwikis.com/Mod_troubleshooting "Mod troubleshooting") |

Retrieved from " [https://ck3.paradoxwikis.com/index.php?title=Triggers&oldid=26702](https://ck3.paradoxwikis.com/index.php?title=Triggers&oldid=26702)"

[Categories](https://ck3.paradoxwikis.com/Special:Categories "Special:Categories"):

- [Potentially outdated](https://ck3.paradoxwikis.com/Category:Potentially_outdated "Category:Potentially outdated")
- [1.7](https://ck3.paradoxwikis.com/Category:1.7 "Category:1.7")
- [Modding](https://ck3.paradoxwikis.com/Category:Modding "Category:Modding")