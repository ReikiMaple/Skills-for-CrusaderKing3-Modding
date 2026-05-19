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

# Dynasties modding

From CK3 Wiki

[Jump to navigation](https://ck3.paradoxwikis.com/Dynasties_modding#mw-head) [Jump to search](https://ck3.paradoxwikis.com/Dynasties_modding#searchInput)

This article is [timeless](https://ck3.paradoxwikis.com/Category:Timeless "Category:Timeless") and should be accurate for any version of the game.

A new feature of Crusader Kings 3 are the improved dynasties, which can be composed by a limitless number of houses. Dynasty modding gives the opportunity to create new dynasties.
It's also possible to change name, coat of arms and houses of any existing dynasty.

## Contents

- [1Creating a new dynasty](https://ck3.paradoxwikis.com/Dynasties_modding#Creating_a_new_dynasty)
- [2Prefixes](https://ck3.paradoxwikis.com/Dynasties_modding#Prefixes)
- [3Coat of arms](https://ck3.paradoxwikis.com/Dynasties_modding#Coat_of_arms)
- [4Motto](https://ck3.paradoxwikis.com/Dynasties_modding#Motto)
- [5House](https://ck3.paradoxwikis.com/Dynasties_modding#House)

## Creating a new dynasty\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Dynasties_modding&veaction=edit&section=1 "Edit section: Creating a new dynasty") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Dynasties_modding&action=edit&section=1 "Edit section: Creating a new dynasty")\]

A new dynasty is created by adding files to four folders.

The first change is applied by adding a new file _example-dynasty.txt_ to the folder _common/dynasties_ of the mod folder. In the file an id is assigned to the new dynasty, for example 2100001. Then lines are added for culture and name. The name line doesn't contain the name, but instead the path in the localisation file. It should look like this when finished:

```
2100001 = {
	prefix = "dynnp_de"
	name = "dynn_Lyon"
	culture = "french"
}
```

The prefix only adds the "de" before the name and is already included in the original localisation files. There are several prefixes for different cultures.

The second change is made in the folder _localization/german/dynasties_ either to a copy of the original _dynasty\_names\_I\_german.yml_ or an empty _example\_dynasty\_names\_german.yml_. The same path applies for other languages, only the name of the file changes as well as the folder following _common/localization_. In this file, the real name of the dynasty is added.

```
dynn_Lyon:0 "Lyon"
```

## Prefixes\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Dynasties_modding&veaction=edit&section=2 "Edit section: Prefixes") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Dynasties_modding&action=edit&section=2 "Edit section: Prefixes")\]

To see a list of existing prefixes, see `localization/english/dynasty_names_l_english.yml` (or the version for your language). They are at the top of the file, starting with `dynnp_`.

To add a new prefix, simply add it to your customised dynasties file, or (if you have a lot), create a new file, such as `dynasty_prefixes_l_english.yml`.

Note that you need to leave a space in the localization string if there is supposed to be a space in the resulting text. For example:

```
# In localization/english/my_dynasty_names_l_english.yml
dynnp_de:0 "de " # Space after de
dynnp_d-:0 "d'" # No space after d'

# In common/dynasties/my_dynasties.txt
200001 = {
  prefix = dynnp_de
  name = dynn_Lyon
}
200002 = {
  prefix = dynnp_d-
  name = dynn_Oeuvre
}
```

Results in:

- **de Lyon**
- **d'Oeuvre**

## Coat of arms\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Dynasties_modding&veaction=edit&section=3 "Edit section: Coat of arms") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Dynasties_modding&action=edit&section=3 "Edit section: Coat of arms")\]

_Main article: [Coat of arms modding](https://ck3.paradoxwikis.com/Coat_of_arms_modding "Coat of arms modding")_

The next change is made in _common/coat\_of\_arms/coat\_of\_arms_ to the _90\_dynasties.txt_ or the empty new file. Here is added the description of the coat of arms. Here any existing or new one can be pasted. The example uses the coat of arms of the county of Saarbrücken in Lotharingia.

```
2100001 = { # Lyon
	pattern = "pattern_solid.dds"
	color1 = "blue"
	color2 = "white"
	colored_emblem = {
		texture = "ce_lion_rampant_crown.dds"
		color1 = "white"
		color2 = "yellow"
		instance = { position = { 0.5 0.5 } scale = { 1.0 1.0 }  }
	}
}
```

## Motto\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Dynasties_modding&veaction=edit&section=4 "Edit section: Motto") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Dynasties_modding&action=edit&section=4 "Edit section: Motto")\]

Mottos can be added to dynasties or to houses (or both):

```
2100001 = {
	prefix = "dynnp_de"
	name = "dynn_Lyon"
	culture = "french"
	motto = "dynn_Lyon_motto"
}
```

You will then need to [localize](https://ck3.paradoxwikis.com/Localization "Localization") the motto.

## House\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Dynasties_modding&veaction=edit&section=5 "Edit section: House") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Dynasties_modding&action=edit&section=5 "Edit section: House")\]

Finally, the founding house can be assigned in a text file in _common/dynasty\_houses_. If you choose not to do this, the game will create a founding house using details from the dynasty.

```
house_lyon = {
	prefix = "dynnp_de"
	name = "dynn_Lyon"
	dynasty = 2100001 #Lyon
}
```

When every step is done, the final result ingame should look like this:

[![Modded Lyon-Dynasty.jpg](https://ck3.paradoxwikis.com/images/thumb/5/50/Modded_Lyon-Dynasty.jpg/300px-Modded_Lyon-Dynasty.jpg)](https://ck3.paradoxwikis.com/File:Modded_Lyon-Dynasty.jpg)

[Enlarge](https://ck3.paradoxwikis.com/File:Modded_Lyon-Dynasty.jpg "Enlarge")

**[Modding](https://ck3.paradoxwikis.com/Modding "Modding")**

|     |     |
| --- | --- |
| Documentation | [Scripting](https://ck3.paradoxwikis.com/Scripting "Scripting") • [Scopes](https://ck3.paradoxwikis.com/Scopes "Scopes") • [Effects](https://ck3.paradoxwikis.com/Effects "Effects") • [Triggers](https://ck3.paradoxwikis.com/Triggers "Triggers") • [Variables](https://ck3.paradoxwikis.com/Variables "Variables") • [Modifiers](https://ck3.paradoxwikis.com/Modifier_list "Modifier list") |

|     |     |
| --- | --- |
| Scripting | [AI](https://ck3.paradoxwikis.com/AI_modding "AI modding") • [Bookmarks](https://ck3.paradoxwikis.com/Bookmarks_modding "Bookmarks modding") • [Characters](https://ck3.paradoxwikis.com/Characters_modding "Characters modding") • [Commands](https://ck3.paradoxwikis.com/Commands "Commands") • [Council](https://ck3.paradoxwikis.com/Council_modding "Council modding") • [Culture](https://ck3.paradoxwikis.com/Culture_modding "Culture modding") • [Decisions](https://ck3.paradoxwikis.com/Decisions_modding "Decisions modding") • Dynasties • [Events](https://ck3.paradoxwikis.com/Event_modding "Event modding") • [Governments](https://ck3.paradoxwikis.com/Governments_modding "Governments modding") • [History](https://ck3.paradoxwikis.com/History_modding "History modding") • [Holdings](https://ck3.paradoxwikis.com/Holdings_modding "Holdings modding") • [Lifestyles](https://ck3.paradoxwikis.com/Lifestyles_modding "Lifestyles modding") • [Regiments](https://ck3.paradoxwikis.com/Regiments_modding "Regiments modding") • [Religions](https://ck3.paradoxwikis.com/Religions_modding "Religions modding") • [Script Values](https://ck3.paradoxwikis.com/Script_values "Script values") • [Story cycles](https://ck3.paradoxwikis.com/Story_cycles_modding "Story cycles modding") • [Struggles](https://ck3.paradoxwikis.com/Struggle_modding "Struggle modding") • [Titles](https://ck3.paradoxwikis.com/Title_modding "Title modding") • [Traits](https://ck3.paradoxwikis.com/Trait_modding "Trait modding") |

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

Retrieved from " [https://ck3.paradoxwikis.com/index.php?title=Dynasties\_modding&oldid=11523](https://ck3.paradoxwikis.com/index.php?title=Dynasties_modding&oldid=11523)"

[Categories](https://ck3.paradoxwikis.com/Special:Categories "Special:Categories"):

- [Timeless](https://ck3.paradoxwikis.com/Category:Timeless "Category:Timeless")
- [Modding](https://ck3.paradoxwikis.com/Category:Modding "Category:Modding")