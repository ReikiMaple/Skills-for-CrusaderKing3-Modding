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

# Variables

From CK3 Wiki

[Jump to navigation](https://ck3.paradoxwikis.com/Variables#mw-head) [Jump to search](https://ck3.paradoxwikis.com/Variables#searchInput)

Variables store information permanently until removed.

## Contents

- [1Setting a variable](https://ck3.paradoxwikis.com/Variables#Setting_a_variable)
- [2Modifying a variable](https://ck3.paradoxwikis.com/Variables#Modifying_a_variable)
- [3Removing a variable](https://ck3.paradoxwikis.com/Variables#Removing_a_variable)
- [4Accessing a variable](https://ck3.paradoxwikis.com/Variables#Accessing_a_variable)
- [5Global variables](https://ck3.paradoxwikis.com/Variables#Global_variables)
- [6Local variables](https://ck3.paradoxwikis.com/Variables#Local_variables)
- [7References](https://ck3.paradoxwikis.com/Variables#References)

## Setting a variable\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Variables&veaction=edit&section=1 "Edit section: Setting a variable") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Variables&action=edit&section=1 "Edit section: Setting a variable")\]

A variable is set using the `set_variable` [effect](https://ck3.paradoxwikis.com/Effect "Effect"), on the [scope](https://ck3.paradoxwikis.com/Scope "Scope") in the context of which the [effect](https://ck3.paradoxwikis.com/Effect "Effect") is executed.

```
set_variable = {
   name = X
   value = Y
}
```

The name of the variable is a string that can be chosen arbitrarily: setting a variable defines it, and there is no list of existing or predefined variables in the game.

The value of a variable can be:

- a boolean

The `set_variable` effect also has a simple form that sets a boolean value.

```
set_variable = X
```

is the same thing as

```
set_variable = {
   name = X
   value = yes
}
```

When used in a character [scope](https://ck3.paradoxwikis.com/Scope "Scope"), it is also the same thing as using the confusingly named `add_character_flag` effect:

```
add_character_flag = X
```

- a number

Variables can be set to an arbitrary decimal value:

```
set_variable = {
   name = test
   value = 2.37
}
```

The value can also be calculated dynamically using a [script math](https://ck3.paradoxwikis.com/index.php?title=Script_math&action=edit&redlink=1 "Script math (page does not exist)") block:

```
set_variable = {
   name = test
   value = {
      value = 5
      add = 2
      multiply = 3
   }
}
```

... or set to a [script value](https://ck3.paradoxwikis.com/Script_values "Script values") directly

```
set_variable = {
   name = test
   value = some_script_value
}
```

Recall that most [triggers](https://ck3.paradoxwikis.com/Triggers "Triggers") that compare against a number (i.e. support the <, <=, =, !=, >, >= operators) can also be used as script values:

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

- a flag value

Variables can store flag values:

```
set_variable = {
   name = test
   value = flag:some_flag
}
```

- a [scope](https://ck3.paradoxwikis.com/Scope#database_scopes "Scope")

Variables can store scopes:

```
set_variable = {
   name = test
   value = scope:some_scope
}
```

This example uses a saved scope, but any means of accessing a scope can be used to feed into the value parameter: database access, event targets, etc.

_Main article: [Scopes](https://ck3.paradoxwikis.com/Scopes "Scopes")_

The variable doesn't store a copy of the scope, it rather acts as a pointer to that scope.

## Modifying a variable\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Variables&veaction=edit&section=2 "Edit section: Modifying a variable") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Variables&action=edit&section=2 "Edit section: Modifying a variable")\]

If a variable is already set on a scope, setting a new variable with the same name replaces the existing variable, even if it stores a value of a different nature.

If a variable stores a numerical value, it can be changed using the `change_variable` effect to either add to its value, or multiply it.

```
change_variable = {
   name = X
   add/multiply = Y
}
```

## Removing a variable\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Variables&veaction=edit&section=3 "Edit section: Removing a variable") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Variables&action=edit&section=3 "Edit section: Removing a variable")\]

Once set on a scope, a variable remains there until either:

- it is manually removed in script
- the scope it is stored on is destroyed
- if stored on a character, when the character dies

To avoid savegame bloat, amongst other thing, variables should be removed when no longer useful by using the `remove_variable` effect.

```
remove_variable = X
```

## Accessing a variable\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Variables&veaction=edit&section=4 "Edit section: Accessing a variable") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Variables&action=edit&section=4 "Edit section: Accessing a variable")\]

Because variables are set on a specific scope, they can only be accessed from that same scope, using the syntax `var:<variable name>`.

A variable can only be accessed if it has been set, which can be verified from the scope the variable was supposedly set on by using the `has_variable` trigger.

Like event targets, a variable can be chained to the scope it is stored on:

```
scope:some_scope.var:some_var
```

If the variable stores a scope, valid event targets can be chained off of it:

```
# if var:some_var
scope:some_scope.var:some_var.father
```

Likewise, if the variable stores a scope, on which another variable is set, the 2nd variable can be chained as well:

```
scope:some_scope.var:some_var.var:other_var
```

## Global variables\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Variables&veaction=edit&section=5 "Edit section: Global variables") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Variables&action=edit&section=5 "Edit section: Global variables")\]

While variables are set on a scope, and accessible from that scope, global variables are set on the gamestate itself, and as such are accessible from any context.

Aside from that, a global variable works in every respect like a variable:

- it is set using the `set_global_variable`effect
- if it has a numerical value, it can be changed with the `change_global_variable` effect
- it is removed with the `remove_global_variable` effect
- it is accessed using `global_var:some_global_var`

## Local variables\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Variables&veaction=edit&section=6 "Edit section: Local variables") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Variables&action=edit&section=6 "Edit section: Local variables")\]

While variables are set on a scope, and accessible from that scope, local variables are set on a top scope, and as such are accessible from any context within that same top scope.
In practice, because top scopes are temporary in nature, it means that local variables are much less permanent than regular variables, and in most cases, using a saved scope or a saved scope value achieves is more practical.

_Main article: [Saved scope](https://ck3.paradoxwikis.com/Saved_scope "Saved scope")_

Aside from that, a local variable works in every respect like a variable:

- it is set using the `set_local_variable` effect
- if it has a numerical value, it can be changed with the `change_local_variable` effect
- it is removed with the `remove_local_variable` effect
- it is accessed using `local_var:some_local_var`

## References\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Variables&veaction=edit&section=7 "Edit section: References") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Variables&action=edit&section=7 "Edit section: References")\]

**[Modding](https://ck3.paradoxwikis.com/Modding "Modding")**

|     |     |
| --- | --- |
| Documentation | [Scripting](https://ck3.paradoxwikis.com/Scripting "Scripting") • [Scopes](https://ck3.paradoxwikis.com/Scopes "Scopes") • [Effects](https://ck3.paradoxwikis.com/Effects "Effects") • [Triggers](https://ck3.paradoxwikis.com/Triggers "Triggers") • Variables • [Modifiers](https://ck3.paradoxwikis.com/Modifier_list "Modifier list") |

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

Retrieved from " [https://ck3.paradoxwikis.com/index.php?title=Variables&oldid=30166](https://ck3.paradoxwikis.com/index.php?title=Variables&oldid=30166)"

[Category](https://ck3.paradoxwikis.com/Special:Categories "Special:Categories"):

- [Modding](https://ck3.paradoxwikis.com/Category:Modding "Category:Modding")