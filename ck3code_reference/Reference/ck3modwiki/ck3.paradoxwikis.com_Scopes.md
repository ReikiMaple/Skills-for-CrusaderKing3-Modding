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

# Scopes

From CK3 Wiki

[Jump to navigation](https://ck3.paradoxwikis.com/Scopes#mw-head) [Jump to search](https://ck3.paradoxwikis.com/Scopes#searchInput)

Please help with verifying or updating older sections of this article.

At least some were last verified for [version](https://ck3.paradoxwikis.com/CK3_Wiki:Versioning "CK3 Wiki:Versioning") 1.1.

This article is for the PC version of Crusader Kings 3 only.

[![](https://ck3.paradoxwikis.com/images/thumb/8/8a/CK3_Scopes.png/300px-CK3_Scopes.png)](https://ck3.paradoxwikis.com/File:CK3_Scopes.png)

[Enlarge](https://ck3.paradoxwikis.com/File:CK3_Scopes.png "Enlarge")

CK3 Scope Overview Chart

**Scopes** are used in [scripting](https://ck3.paradoxwikis.com/Scripting "Scripting") to select entities in order to check [triggers](https://ck3.paradoxwikis.com/Triggers "Triggers") or execute [effects](https://ck3.paradoxwikis.com/Effects "Effects").

[![](https://ck3.paradoxwikis.com/images/thumb/4/44/Exportedscopes190.png/300px-Exportedscopes190.png)](https://ck3.paradoxwikis.com/File:Exportedscopes190.png)

[Enlarge](https://ck3.paradoxwikis.com/File:Exportedscopes190.png "Enlarge")

These are the color-coded direct scopes as of 1.8.0, generated via automated export from the game files.

## Contents

- [1Definition](https://ck3.paradoxwikis.com/Scopes#Definition)
  - [1.1Database scope](https://ck3.paradoxwikis.com/Scopes#Database_scope)
  - [1.2Primitive scope](https://ck3.paradoxwikis.com/Scopes#Primitive_scope)
  - [1.3Top scope](https://ck3.paradoxwikis.com/Scopes#Top_scope)
- [2Accessing scopes](https://ck3.paradoxwikis.com/Scopes#Accessing_scopes)
  - [2.1root](https://ck3.paradoxwikis.com/Scopes#root)
  - [2.2Context switch](https://ck3.paradoxwikis.com/Scopes#Context_switch)
  - [2.3Database access](https://ck3.paradoxwikis.com/Scopes#Database_access)
  - [2.4Event target](https://ck3.paradoxwikis.com/Scopes#Event_target)
    - [2.4.1this](https://ck3.paradoxwikis.com/Scopes#this)
    - [2.4.2prev](https://ck3.paradoxwikis.com/Scopes#prev)
  - [2.5Saved scope](https://ck3.paradoxwikis.com/Scopes#Saved_scope)
  - [2.6List-builder](https://ck3.paradoxwikis.com/Scopes#List-builder)
    - [2.6.1every\_X](https://ck3.paradoxwikis.com/Scopes#every_X)
    - [2.6.2random\_X](https://ck3.paradoxwikis.com/Scopes#random_X)
    - [2.6.3ordered\_X](https://ck3.paradoxwikis.com/Scopes#ordered_X)
    - [2.6.4any\_X](https://ck3.paradoxwikis.com/Scopes#any_X)
  - [2.7Saved scope value](https://ck3.paradoxwikis.com/Scopes#Saved_scope_value)
- [3References](https://ck3.paradoxwikis.com/Scopes#References)

## Definition\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Scopes&veaction=edit&section=1 "Edit section: Definition") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Scopes&action=edit&section=1 "Edit section: Definition")\]

[\[top\]](https://ck3.paradoxwikis.com/Scopes#top)

### Database scope\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Scopes&veaction=edit&section=2 "Edit section: Database scope") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Scopes&action=edit&section=2 "Edit section: Database scope")\]

Scope most often refers to a database object, and the database itself is referred to as the scope type. Those include for example characters, titles, provinces, etc.

The full list of available scope types an be found in [event\_scopes.log](https://ck3.paradoxwikis.com/Scopes_list "Scopes list").

Unless specified otherwise, the term scope will always refer to a database scope.

A database scope usually has the following three characteristics:

- you can read information from it, using [triggers](https://ck3.paradoxwikis.com/Triggers "Triggers")
- you can write information on it or modify it, using [effects](https://ck3.paradoxwikis.com/Effects "Effects")
- you can move from one to another

Some scopes are created on game start, either from /Crusader Kings III/game/history files (historical characters, titles), /Crusader Kings III/game/map data (provinces), or /Crusader Kings III/game/common folders (cultures, faiths, governments, traits...).

Some scopes can also be created on runtime either in code (ex: naturally born characters), or in script (ex: characters created using the `create_character` effect, dynamic titles).

### Primitive scope\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Scopes&veaction=edit&section=3 "Edit section: Primitive scope") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Scopes&action=edit&section=3 "Edit section: Primitive scope")\]

[\[top\]](https://ck3.paradoxwikis.com/Scopes#top)

Numbers, booleans (yes/no) and flag values (`flag:some_string`) are so-called primitive scopes. They cannot be modified or accessed, and while "numbers are scopes" can possibly be a confusing statement to beginners, it is useful to know to better understand some advanced functionalities or error logging.

### Top scope\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Scopes&veaction=edit&section=4 "Edit section: Top scope") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Scopes&action=edit&section=4 "Edit section: Top scope")\]

[\[top\]](https://ck3.paradoxwikis.com/Scopes#top)

A top scope is a temporary and abstract object created by the game to store information, amongst other things so that it can be retrieved and displayed in localization or GUI.

## Accessing scopes\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Scopes&veaction=edit&section=5 "Edit section: Accessing scopes") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Scopes&action=edit&section=5 "Edit section: Accessing scopes")\]

[\[top\]](https://ck3.paradoxwikis.com/Scopes#top)

Unless specified otherwise, the term scope always refers to a database scope.

In script, [effects](https://ck3.paradoxwikis.com/Effects "Effects") and [triggers](https://ck3.paradoxwikis.com/Triggers "Triggers") are executed in a context, and most of them work from specific scope types.

Ex: the [trigger](https://ck3.paradoxwikis.com/Trigger "Trigger")`is_ai = no` checks whether the current scope is a player, which only makes sense in the context of a character scope. Using it in the context of another scope type will throw an error.

This section explains how to change the context in which script is interpreted. Scopes can also be used as arguments for [effects](https://ck3.paradoxwikis.com/Effects "Effects") and [triggers](https://ck3.paradoxwikis.com/Triggers "Triggers"), where the following methods of access will also be used.

#### root\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Scopes&veaction=edit&section=6 "Edit section: root") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Scopes&action=edit&section=6 "Edit section: root")\]

[\[top\]](https://ck3.paradoxwikis.com/Scopes#top)

[Trigger](https://ck3.paradoxwikis.com/Trigger "Trigger") blocks and [effect](https://ck3.paradoxwikis.com/Effect "Effect") blocks often have a default context provided by code. When such is the case, unless the context is changed, [triggers](https://ck3.paradoxwikis.com/Triggers "Triggers") are evaluated and [effects](https://ck3.paradoxwikis.com/Effects "Effects") are executed in the context of that scope.

Ex: in an event's `immediate` effect block, the context is the character that receives the event, and by default, all effects in that block are executed in the context of that specific character scope.

In [effect](https://ck3.paradoxwikis.com/Effect "Effect") and [trigger](https://ck3.paradoxwikis.com/Trigger "Trigger") blocks that have a default context, `root` is a shortcut to that default context. Contrary to a common misconception, `root` is not the player. As a matter of fact, "the" player is a very dubious concept in a game that can have several players.

Not all [effect](https://ck3.paradoxwikis.com/Effect "Effect") blocks and [trigger](https://ck3.paradoxwikis.com/Trigger "Trigger") blocks have a `root`. For example, those in [character interactions](https://ck3.paradoxwikis.com/index.php?title=Character_interactions&action=edit&redlink=1 "Character interactions (page does not exist)") do not have one, because it could possibly be ambiguous: would it be the character sending the interaction, or the character receiving it?

`root` is not necessarily a character scope either. Whether there is a `root` and what scope it is depends on each [effect](https://ck3.paradoxwikis.com/Effect "Effect") block or [trigger](https://ck3.paradoxwikis.com/Trigger "Trigger") block.

### Context switch\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Scopes&veaction=edit&section=7 "Edit section: Context switch") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Scopes&action=edit&section=7 "Edit section: Context switch")\]

[\[top\]](https://ck3.paradoxwikis.com/Scopes#top)

The context of an [effect](https://ck3.paradoxwikis.com/Effect "Effect") block or [trigger](https://ck3.paradoxwikis.com/Trigger "Trigger") block can be changed at any time by opening a new script block with the scope you want to set the context to, followed by an equal sign `=` and an opening bracket `{`. The context change is in effect until the corresponding closing bracket `}` is found.

Ex: in an event's `immediate` effect block

```
immediate = {
   < context here is the character receiving the event, a character scope >
   title:k_france = {
      < context here is the Kingdom of France, a title scope >
   }
   < closing the block reverts back to the initial character scope >
}
```

Context can be changed multiple times by opening further nested script blocks. Each time a new block is opened, indentation should be increased. When the block is closed, indentation should be decreased. Keeping a clean indentation helps understanding at a glance in what context [triggers](https://ck3.paradoxwikis.com/Triggers "Triggers") and [effects](https://ck3.paradoxwikis.com/Effects "Effects") are interpreted.

When `root` is provided, it can be accessed at any time to set the context back to it.

Ex:

```
immediate = {
   title:k_france = {
      < context here is the Kingdom of France >
      root = {
         < context here is the character receiving the event >
      }
   }
}
```

Trying to change the context of a script block to an invalid scope results in a failed context switch.
Ex:

```
immediate = {
   title:k_frnace = {
```

The typo causes a failed context switch because `k_frnace` is not defined.

### Database access\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Scopes&veaction=edit&section=8 "Edit section: Database access") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Scopes&action=edit&section=8 "Edit section: Database access")\]

[\[top\]](https://ck3.paradoxwikis.com/Scopes#top)

Scopes being database objects, they have a unique key or ID. They are identified using the syntax `<scope type>:<scope key>`.

Ex: `title:k_france` is the Kingdom of France, as defined in `common/landed_titles/`.

```
title:k_france = {
   # context here is the Kingdom of France
}
```

Characters have two IDs: a historical ID, and a runtime ID.
Historical IDs are predetermined in the /Crusader Kings III/game/history files, so historical characters can be accessed with that ID. Non-historical characters, on the other hand, only have a runtime ID, assigned when the character is created. As it cannot be known in advance, and is not consistent across different games, it cannot be referenced in script, and non-historical characters can never be accessed through this method.

### Event target\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Scopes&veaction=edit&section=9 "Edit section: Event target") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Scopes&action=edit&section=9 "Edit section: Event target")\]

[\[top\]](https://ck3.paradoxwikis.com/Scopes#top)

Scopes that have a unique relation from one to another can be accessed through event targets. As the game knows the scope type of all event targets, those are not prefixed.

The full list of available event targets can be found in [event\_targets.log](https://ck3.paradoxwikis.com/Scopes_list "Scopes list").

Ex:

```
holder - Get holder of scoped title
Input Scopes: landed_title
Output Scopes: character
```

`Output Scopes` is the scope type of the event target.
`Input Scopes` is the scope type an event target can be used from.

A title can only ever be held by a single character at a time. As such, the `holder` event target allows moving from a title scope to the unique character scope holding that title.

```
title:k_france = {
   holder = {
```

Event targets can be chained and separated by a dot.

Ex:

```
title:k_france.holder = {
```

The following event targets have a specific contextual behavior.

#### this\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Scopes&veaction=edit&section=10 "Edit section: this") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Scopes&action=edit&section=10 "Edit section: this")\]

[\[top\]](https://ck3.paradoxwikis.com/Scopes#top)

`this` is the current scope. It is useful specifically in [scope comparison](https://ck3.paradoxwikis.com/index.php?title=Scope_comparison&action=edit&redlink=1 "Scope comparison (page does not exist)"), or to feed the current scope as an argument.

#### prev\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Scopes&veaction=edit&section=11 "Edit section: prev") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Scopes&action=edit&section=11 "Edit section: prev")\]

[\[top\]](https://ck3.paradoxwikis.com/Scopes#top)

`prev` is the previous scope. Like `this`, it is often useful in [scope comparison](https://ck3.paradoxwikis.com/index.php?title=Scope_comparison&action=edit&redlink=1 "Scope comparison (page does not exist)") or to feed the previous scope as an argument, but it can also be useful when used in conjunction with list-builders below.

```
title:k_france = {
   holder = {
      prev = {
         # context here has been set back one step to title:k_france
```

Unlike in CK2, `prev` cannot be chained to go back several steps.

### Saved scope\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Scopes&veaction=edit&section=12 "Edit section: Saved scope") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Scopes&action=edit&section=12 "Edit section: Saved scope")\]

[\[top\]](https://ck3.paradoxwikis.com/Scopes#top)

A saved scope is an arbitrarily-named pointer to a specific scope, using the syntax `scope:<scope name>`.

Saved scopes can be saved in and provided by code. For example, in [character interactions](https://ck3.paradoxwikis.com/Interactions_modding "Interactions modding"), `scope:actor` is the character sending the interaction, and `scope:recipient` the character receiving the interaction.

Some on\_actions also provide pre-saved scopes. Check the comments in the files to see which scopes are available.

Saved scopes can also be saved in script using the `save_scope_as` [effect](https://ck3.paradoxwikis.com/Effect "Effect"), which saves the current scope with the provided name.

```
title:k_france.holder = {
   save_scope_as = king_of_france
}
```

From then on, that saved scope can be accessed at any time:

```
scope:king_of_france = {
```

Saved scopes can be passed from UI to scripted guis or script values/custom localization with AddScope:

`"[ScriptedGui.Execute( GuiScope.SetRoot( GetPlayer.MakeScope ).AddScope( 'target', CharacterWindow.GetCharacter.MakeScope ).End )]"`

`"[GuiScope.SetRoot( GetPlayer.MakeScope ).AddScope( 'target', CharacterWindow.GetCharacter.MakeScope ).ScriptValue('sval_name')|0]"`

Saved scopes carry throughout an unbroken effect chain. For example, if `scope:king_of_france` is saved in event A, and event A then fires event B, `scope:king_of_france` will be accessible in event B.

When the unbroken effect chain reaches its end, saved scopes are automatically cleared. If necessary, they can also be manually cleared using the `clear_saved_scope` [effect](https://ck3.paradoxwikis.com/Effect "Effect").

`save_temporary_scope_as` can be used either as an [effect](https://ck3.paradoxwikis.com/Effect "Effect") or as a [trigger](https://ck3.paradoxwikis.com/Trigger "Trigger"). Saved temporary scopes do not carry throughout an unbroken effect chain, and expire at the end of the current [effect](https://ck3.paradoxwikis.com/Effect "Effect") block or [trigger](https://ck3.paradoxwikis.com/Trigger "Trigger") block they were saved in.

A saved scope name can only be used once at any given time. Saving a scope with the same name as another previously saved scope overwrites it.

### List-builder\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Scopes&veaction=edit&section=13 "Edit section: List-builder") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Scopes&action=edit&section=13 "Edit section: List-builder")\]

[\[top\]](https://ck3.paradoxwikis.com/Scopes#top)

Scopes that have a relation from one to multiple others cannot be accessed through event targets.

For example, a character only ever has one mother, accessible using the `mother` event target. But the opposite is not true: a mother can have multiple children, and as such there cannot be a `child` event target, as that would be ambiguous.

In that case, scopes can be provided in a list, which can be accessed using a list-builder, of which there are 3 [effect](https://ck3.paradoxwikis.com/Effect "Effect") variants, and 1 [trigger](https://ck3.paradoxwikis.com/Trigger "Trigger") variant.

In the following sections, all script examples are executed in the context of a character scope, using the `child` list. There are different kinds of lists, including lists built in script.

_Main article: [Lists](https://ck3.paradoxwikis.com/Lists "Lists")_

#### every\_X\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Scopes&veaction=edit&section=14 "Edit section: every X") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Scopes&action=edit&section=14 "Edit section: every X")\]

[\[top\]](https://ck3.paradoxwikis.com/Scopes#top)

`every_X` is an [effect](https://ck3.paradoxwikis.com/Effect "Effect") that accesses all scopes in the list one after the other, and executes the [effects](https://ck3.paradoxwikis.com/Effects "Effects") within for each one of them.

```
every_child = {
   add_gold = 10
}
# every child of the current character scope gets 10 gold
```

If the list is empty, enclosed [effects](https://ck3.paradoxwikis.com/Effects "Effects") are not executed.

The list can be trimmed out using [triggers](https://ck3.paradoxwikis.com/Triggers "Triggers") in a [limit](https://ck3.paradoxwikis.com/Limit "Limit") block. [Effects](https://ck3.paradoxwikis.com/Effects "Effects") will only be executed for scopes for which the limit is evaluated as true.

```
every_child = {
   limit = { is_female = yes }
   add_gold = 10
}
# every female child of the current character scope gets 10 gold
```

If the filtered list is empty, enclosed [effects](https://ck3.paradoxwikis.com/Effects "Effects") are not executed.

As mentioned above, `prev` is often used in list-builders to access back the scope the list-builder is used from.

```
every_child = {
   limit = { is_female = yes }
   prev = {
      add_gold = 10
   }
}
# the current character scope gets 10 gold for every female child they have
```

Saving scopes in `every_X` list builders can be useful, but since only one saved scope with a given name can exist at any given time, once `every_X` has finished running, only the last scope in the list is effectively saved.

```
every_child = {
   limit = { is_female = yes }
   save_scope_as = female_child
}
scope:female_child = {
   # this is the last female child in the list, not all of them
}
```

#### random\_X\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Scopes&veaction=edit&section=15 "Edit section: random X") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Scopes&action=edit&section=15 "Edit section: random X")\]

[\[top\]](https://ck3.paradoxwikis.com/Scopes#top)

`random_X` accesses a random scope in the list, and executes the enclosed [effects](https://ck3.paradoxwikis.com/Effects "Effects") only for that one scope.

```
random_child = {
   add_gold = 10
}
# one child gets 10 gold
```

If the list is empty, enclosed [effects](https://ck3.paradoxwikis.com/Effects "Effects") are not executed.

The list can be trimmed out using [triggers](https://ck3.paradoxwikis.com/Triggers "Triggers") in a [limit](https://ck3.paradoxwikis.com/Limit "Limit") block, and `random_X` will access a random scope in the list for which the limit is evaluated as true.

```
random_child = {
   limit = { is_female = yes }
   add_gold = 10
}
# one female child gets 10 gold
```

If no scope in the list meets the requirements of the [limit](https://ck3.paradoxwikis.com/Limit "Limit") block, enclosed [effects](https://ck3.paradoxwikis.com/Effects "Effects") are not executed.

Saved scopes are often used in conjunction with `random_X` list-builders, especially when trying to scope to specific characters. As most characters in the game are not historical characters, and cannot be accessed through their ID, they need to be accessed relatively to another scope, and then saved as a scope to be easily accessed again later.

```
random_child = {
   limit = {
      is_female = yes
      is_adult = yes
      is_married = no
   }
   save_scope_as = celibate_daughter
}
```

#### ordered\_X\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Scopes&veaction=edit&section=16 "Edit section: ordered X") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Scopes&action=edit&section=16 "Edit section: ordered X")\]

[\[top\]](https://ck3.paradoxwikis.com/Scopes#top)

`ordered_X` sorts the list according to its `order_by` parameter, and by default accesses the first scope in the list in descending order, and executes the enclosed [effect](https://ck3.paradoxwikis.com/Effect "Effect") for that scope only. `order_by` can either be a named value or a script value, interpreted in the context of each scope in the list.

Warning: in [script math](https://ck3.paradoxwikis.com/index.php?title=Script_math&action=edit&redlink=1 "Script math (page does not exist)"), the default behavior of `ordered_X` is to iterate through _all_ scopes in the list in order. It is unclear whether this is a bug, or working as intended.

```
ordered_child = {
   order_by = age
   add_gold = 10
}
# the eldest child gets 10 gold
```

The list can be trimmed out using [triggers](https://ck3.paradoxwikis.com/Triggers "Triggers") in a [limit](https://ck3.paradoxwikis.com/Limit "Limit") block, and `ordered_X` will pick the first scope in the list for which the limit is evaluated as true.

```
ordered_child = {
   limit = { is_female = yes }
   order_by = age
   add_gold = 10
}
# the oldest female child gets 10 gold
```

The `position` parameter enables overriding the default behavior of `ordered_X` to access the scope in the list with the specified index< starting at 0. It uses either an integer, or a script value that automatically rounds down to the nearest integer. `position = 0` is the first scope in the list.

```
ordered_child = {
   limit = { is_female = yes }
   order_by = age
   position = 1
}
# the 2nd eldest daughter gets 10 gold
```

The `min` and `max` parameters make `ordered_X` iterate through all scopes in the list in order that have a higher or equal index than `min` and a lower or equal index than `max`. The `check_range_bounds` parameter avoids errors when the specified range is larger than the size of the list.

```
ordered_child = {
   limit = { is_female = yes }
   order_by = age
   max = 2
   check_range_bounds = no
}
# the 3 elder daughters get 10 gold, starting with the oldest
```

#### any\_X\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Scopes&veaction=edit&section=17 "Edit section: any X") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Scopes&action=edit&section=17 "Edit section: any X")\]

[\[top\]](https://ck3.paradoxwikis.com/Scopes#top)

`any_X` accesses scopes in the list in an undetermined order until the triggers nested within evaluate to true for one of them, in which case `any_X` evaluates as true. If the enclosed triggers evaluate as false for all scopes in the list, or if the list is empty, `any_X` evaluates as false.

```
any_child = {
   age > 10
}
# true if any child is strictly older than 10
```

The list can be trimmed down using triggers in a `filter` block. Triggers enclosed in the `any_X` list builder will only be checked for scopes for which the `filter` block is evaluated as true.

```
any_child = {
   filter = { is_female = yes }
   age > 10
}
# true if any female child is strictly older than 10
```

`save_temporary_scope_as` can be used to save whatever object first evaluates as true for all enclosed triggers, to be accessed later from the same trigger block.

```
any_child = {
   filter = { is_female = yes }
   age > 10
   save_temporary_scope_as = teenage_daughter
}
```

The `count` parameter can be used to require triggers enclosed within `any_X` to evaluate to true for an arbitrary number of scopes in the list.

```
any_child = {
   condition = { is_female = yes }
   age > 10
   count >= 2
}
# true if at least to female children are strictly older than 10
```

The `percent` parameter can be used to require triggers enclosed within `any_X` to evaluate to true for an arbitrary portion of scopes in the list.

```
any_child = {
   condition = { is_female = yes }
   age > 10
   percent >= 0.5
}
# true if at least half of the female children are strictly older than 10
```

### Saved scope value\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Scopes&veaction=edit&section=18 "Edit section: Saved scope value") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Scopes&action=edit&section=18 "Edit section: Saved scope value")\]

[\[top\]](https://ck3.paradoxwikis.com/Scopes#top)

A saved scope value is an arbitrarily-named pointer to a specific primitive scope, using the syntax `scope:<scope name>`.

Saved scope values can be saved in and provided by code, although it is much rarer than saved scopes. For example, in a [character interaction](https://ck3.paradoxwikis.com/index.php?title=Character_interaction&action=edit&redlink=1 "Character interaction (page does not exist)") that has an interaction option named `option_1`, `scope:option_1` is provided as a boolean scope value, true if the option is selected, false if it isn't.

Saved scope values can also be saved in script using the `save_scope_value_as` effect, which saves the provided scope value with the provided name.

```
save_scope_value_as = {
   name = some_name
   value = <boolean>/<number>/<flag value>
}
```

Similarly, temporary saved scope values can be saved by using the `save_temporary_scope_value_as` trigger or effect.

Saved scope values and temporary saved scope values follow the same rules as saved scopes regarding availability.

## References\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Scopes&veaction=edit&section=19 "Edit section: References") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Scopes&action=edit&section=19 "Edit section: References")\]

**[Modding](https://ck3.paradoxwikis.com/Modding "Modding")**

|     |     |
| --- | --- |
| Documentation | [Scripting](https://ck3.paradoxwikis.com/Scripting "Scripting") • Scopes • [Effects](https://ck3.paradoxwikis.com/Effects "Effects") • [Triggers](https://ck3.paradoxwikis.com/Triggers "Triggers") • [Variables](https://ck3.paradoxwikis.com/Variables "Variables") • [Modifiers](https://ck3.paradoxwikis.com/Modifier_list "Modifier list") |

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

**[Mechanics](https://ck3.paradoxwikis.com/Mechanics "Mechanics")**

|     |     |
| --- | --- |
| Characters | [Characters](https://ck3.paradoxwikis.com/Characters "Characters") • [Attributes](https://ck3.paradoxwikis.com/Attributes "Attributes") • [Traits](https://ck3.paradoxwikis.com/Traits "Traits") • [Resources](https://ck3.paradoxwikis.com/Resources "Resources") • [Modifiers](https://ck3.paradoxwikis.com/Modifiers "Modifiers") • [Lifestyle](https://ck3.paradoxwikis.com/Lifestyle "Lifestyle") • [Family](https://ck3.paradoxwikis.com/Family_(relation) "Family (relation)") • [Dynasty](https://ck3.paradoxwikis.com/Dynasty "Dynasty") • [Schemes](https://ck3.paradoxwikis.com/Schemes "Schemes") • [Hooks](https://ck3.paradoxwikis.com/Hooks "Hooks") • [Activities](https://ck3.paradoxwikis.com/Activity "Activity") • [Artifacts](https://ck3.paradoxwikis.com/Artifacts "Artifacts") • [Interactions](https://ck3.paradoxwikis.com/Interactions "Interactions") • [Travel](https://ck3.paradoxwikis.com/Travel "Travel") • [Adventurers](https://ck3.paradoxwikis.com/Adventurer "Adventurer") • [Prisoners](https://ck3.paradoxwikis.com/Prisoner "Prisoner") |

|     |     |
| --- | --- |
| Realm & Governance | [Council](https://ck3.paradoxwikis.com/Council "Council") • [Court](https://ck3.paradoxwikis.com/Court "Court") • [Power sharing](https://ck3.paradoxwikis.com/Power_sharing "Power sharing") • [Subjects](https://ck3.paradoxwikis.com/Subjects "Subjects") • [Succession](https://ck3.paradoxwikis.com/Succession "Succession") • [Government](https://ck3.paradoxwikis.com/Government "Government") • [Laws](https://ck3.paradoxwikis.com/Laws "Laws") • [Decisions](https://ck3.paradoxwikis.com/Decisions "Decisions") • [Titles](https://ck3.paradoxwikis.com/Titles "Titles") • [Barony](https://ck3.paradoxwikis.com/Barony "Barony") • [County](https://ck3.paradoxwikis.com/County "County") • [Buildings](https://ck3.paradoxwikis.com/Buildings "Buildings") • [Royal court](https://ck3.paradoxwikis.com/Royal_court "Royal court") • [Domiciles](https://ck3.paradoxwikis.com/Domicile "Domicile") • [Great projects](https://ck3.paradoxwikis.com/Great_projects "Great projects") |

|     |     |
| --- | --- |
| Warfare | [Warfare](https://ck3.paradoxwikis.com/Warfare "Warfare") • [Casus belli](https://ck3.paradoxwikis.com/Casus_belli "Casus belli") • [Alliance](https://ck3.paradoxwikis.com/Alliance "Alliance") • [Army](https://ck3.paradoxwikis.com/Army "Army") • [Hired forces](https://ck3.paradoxwikis.com/Hired_forces "Hired forces") • [Knights](https://ck3.paradoxwikis.com/Knight "Knight") • [Duel](https://ck3.paradoxwikis.com/Duel "Duel") • [Situations](https://ck3.paradoxwikis.com/Situation "Situation") |

|     |     |
| --- | --- |
| Culture & Faith | [Culture](https://ck3.paradoxwikis.com/Culture "Culture") • [Traditions](https://ck3.paradoxwikis.com/Traditions "Traditions") • [Innovations](https://ck3.paradoxwikis.com/Innovation "Innovation") • [Form of Address](https://ck3.paradoxwikis.com/Form_of_address "Form of address") • [Faith](https://ck3.paradoxwikis.com/Faith "Faith") • [Doctrines](https://ck3.paradoxwikis.com/Doctrines "Doctrines") • [Tenets](https://ck3.paradoxwikis.com/Tenets "Tenets") • [Holy sites](https://ck3.paradoxwikis.com/Holy_sites "Holy sites") |

|     |     |
| --- | --- |
| Meta | [Modding](https://ck3.paradoxwikis.com/Modding "Modding") • [Patches](https://ck3.paradoxwikis.com/Patches "Patches") • [Downloadable content](https://ck3.paradoxwikis.com/Downloadable_content "Downloadable content") • [Developer diaries](https://ck3.paradoxwikis.com/Developer_diaries "Developer diaries") • [Achievements](https://ck3.paradoxwikis.com/Achievements "Achievements") • [Jargon](https://ck3.paradoxwikis.com/Jargon "Jargon") • [Bookmarks](https://ck3.paradoxwikis.com/Bookmarks "Bookmarks") • [Interesting characters](https://ck3.paradoxwikis.com/Interesting_characters "Interesting characters") • [Ruler Designer](https://ck3.paradoxwikis.com/Ruler_Designer "Ruler Designer") • [Game rules](https://ck3.paradoxwikis.com/Game_rules "Game rules") |

Retrieved from " [https://ck3.paradoxwikis.com/index.php?title=Scopes&oldid=28429](https://ck3.paradoxwikis.com/index.php?title=Scopes&oldid=28429)"

[Categories](https://ck3.paradoxwikis.com/Special:Categories "Special:Categories"):

- [Potentially outdated](https://ck3.paradoxwikis.com/Category:Potentially_outdated "Category:Potentially outdated")
- [1.1](https://ck3.paradoxwikis.com/Category:1.1 "Category:1.1")
- [Modding](https://ck3.paradoxwikis.com/Category:Modding "Category:Modding")