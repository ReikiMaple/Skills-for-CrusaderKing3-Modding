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

# Weight modifier

From CK3 Wiki

[Jump to navigation](https://ck3.paradoxwikis.com/Weight_modifier#mw-head) [Jump to search](https://ck3.paradoxwikis.com/Weight_modifier#searchInput)

Weight modifiers are conditional modifiers to a base value, used in:

- events' `weight_modifier` blocks
- some effects such as `random` and `random_list`
- AI logic blocks such as `ai_will_do`

For legacy reasons, they are sometimes referred to as MTTH syntax, by opposition to [script math](https://ck3.paradoxwikis.com/index.php?title=Script_math&action=edit&redlink=1 "Script math (page does not exist)") syntax.

## Contents

- [1Syntax](https://ck3.paradoxwikis.com/Weight_modifier#Syntax)
- [2scripted\_modifiers](https://ck3.paradoxwikis.com/Weight_modifier#scripted_modifiers)
  - [2.1Simple form](https://ck3.paradoxwikis.com/Weight_modifier#Simple_form)
  - [2.2Complex form](https://ck3.paradoxwikis.com/Weight_modifier#Complex_form)
- [3References](https://ck3.paradoxwikis.com/Weight_modifier#References)

## Syntax\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Weight_modifier&veaction=edit&section=1 "Edit section: Syntax") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Weight_modifier&action=edit&section=1 "Edit section: Syntax")\]

Weight modifiers are script blocks used to sequentially modify a base value.
They contain:

- a mathematical operator, either `add` or `factor`
- triggers, which determine when the weight modifier should apply
- an optional `desc` parameter, which specifies the localization key used in the tooltip, where applicable

```
base = 10
modifier = {
   add = 10
}
# total value is 20
```

The `base` is always an integer.
The `add` and factor parameters, on the other hand, accept any type of numerical values: numbers, script math, script\_values, saved scope values.

Weight modifiers are applied in the order they are listed.

```
base = 10
modifier = {
   add = 10
}
modifier = {
   factor = 2
}
# total value is 40
```

A weight modifier that contains a set of triggers applies if the set of triggers is evaluated as true.

```
base = 10
modifier = {
   is_adult = yes
   add = 10
}
modifier = {
   is_male = yes
   add = 20
}
# total value for a male adult is 40
# total value for a male child is 30
# total value for a female adult is 20
# total value for a female child is 10
```

## scripted\_modifiers\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Weight_modifier&veaction=edit&section=2 "Edit section: scripted modifiers") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Weight_modifier&action=edit&section=2 "Edit section: scripted modifiers")\]

Scripted\_modifiers are macros that enable replacing a set of weight\_modifiers with a single statement, to make script more legible and avoid repetition.

They are defined in /Crusader Kings III/game/common/scripted\_modifiers, and can be used anywhere weight modifiers are allowed.

### Simple form\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Weight_modifier&veaction=edit&section=3 "Edit section: Simple form") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Weight_modifier&action=edit&section=3 "Edit section: Simple form")\]

If a set of weight modifiers are repeatedly used together, they can be defined as a scripted\_modifier:

```
age_and_gender_modifier = {
   modifier = {
      is_adult = yes
      add = 10
   }
   modifier = {
      is_male = yes
      add = 20
   }
}
```

Wherever that set of weight modifiers should apply, it can be replaced by the scripted\_modifier:

```
base = 10
age_and_gender_modifier = yes
```

### Complex form\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Weight_modifier&veaction=edit&section=4 "Edit section: Complex form") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Weight_modifier&action=edit&section=4 "Edit section: Complex form")\]

Scripted\_modifiers also have a complex form that handles literal text replacement, allowing to pass arguments.

For example, if the following weight modifier applies when a character is vassal to the King of France, and has more than 1000 gold:

```
modifier = {
   add = 10
   is_vassal_of = title:k_france.holder
   gold >= 1000
}
```

It can be defined in a scripted\_modifier, replacing specific scopes or values with capitalized arguments between two `$` signs:

```
rich_vassal_modifier = {
   modifier = {
      add = 10
      is_vassal_of = $TARGET$
      gold >= $VALUE$
   }
}
```

When used, the complex form of the scripted\_modifier specifies what the expected arguments are, by using the same name but without the $ signs:

```
base = 10
rich_vassal_modifier = { TARGET = title:k_france.holder VALUE = 1000 }
```

With that form, every occurrence of $TARGET$ and $VALUE$ in the scripted\_modifier will be _literally_ replaced with the argument provided: the text replacement happens _before_ the scripted\_modifier is evaluated.

## References\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Weight_modifier&veaction=edit&section=5 "Edit section: References") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Weight_modifier&action=edit&section=5 "Edit section: References")\]

**[Modding](https://ck3.paradoxwikis.com/Modding "Modding")**

|     |     |
| --- | --- |
| Documentation | [Scripting](https://ck3.paradoxwikis.com/Scripting "Scripting") • [Scopes](https://ck3.paradoxwikis.com/Scopes "Scopes") • [Effects](https://ck3.paradoxwikis.com/Effects "Effects") • [Triggers](https://ck3.paradoxwikis.com/Triggers "Triggers") • [Variables](https://ck3.paradoxwikis.com/Variables "Variables") • [Modifiers](https://ck3.paradoxwikis.com/Modifier_list "Modifier list") |

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

Retrieved from " [https://ck3.paradoxwikis.com/index.php?title=Weight\_modifier&oldid=20105](https://ck3.paradoxwikis.com/index.php?title=Weight_modifier&oldid=20105)"

[Category](https://ck3.paradoxwikis.com/Special:Categories "Special:Categories"):

- [Modding](https://ck3.paradoxwikis.com/Category:Modding "Category:Modding")