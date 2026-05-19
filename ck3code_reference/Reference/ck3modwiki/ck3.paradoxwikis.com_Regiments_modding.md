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

# Regiments modding

From CK3 Wiki

[Jump to navigation](https://ck3.paradoxwikis.com/Regiments_modding#mw-head) [Jump to search](https://ck3.paradoxwikis.com/Regiments_modding#searchInput)

Please help with verifying or updating older sections of this article.

At least some were last verified for [version](https://ck3.paradoxwikis.com/CK3_Wiki:Versioning "CK3 Wiki:Versioning") 1.3.

This article is for the PC version of Crusader Kings 3 only.

## Contents

- [1Creating a Regiment](https://ck3.paradoxwikis.com/Regiments_modding#Creating_a_Regiment)
- [2Variables](https://ck3.paradoxwikis.com/Regiments_modding#Variables)
  - [2.1Regiments in Innovations](https://ck3.paradoxwikis.com/Regiments_modding#Regiments_in_Innovations)
  - [2.2Regiments in Traditions](https://ck3.paradoxwikis.com/Regiments_modding#Regiments_in_Traditions)
  - [2.3Localization](https://ck3.paradoxwikis.com/Regiments_modding#Localization)

### Creating a Regiment\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Regiments_modding&veaction=edit&section=1 "Edit section: Creating a Regiment") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Regiments_modding&action=edit&section=1 "Edit section: Creating a Regiment")\]

Regiments are defined in /Crusader Kings III/game/game/common/men\_at\_arms\_types

For best compatibility, use unique file names.

**Example:**

```
example_maa = { # maa = Men at arms
	type = # Men at arms type of my_maa

	damage = # damage value of unit
	toughness = # toughness value of unit
	pursuit = # pursuit value of unit
	screen = # screen value of unit

	terrain_bonus = { # Terrain bonus
		forest = { # bonus values, i.e, damage = 10 }
	}

	counters = {
		# what type of men at arms this counters for example archers
	}

	buy_cost = { # cost of a unit }
	low_maintenance_cost = { # unraised maintenance cost of a unit }
	high_maintenance_cost = { # raised maintenance cost of a unit }

	stack = # Men in one unit
	ai_quality = { # ai weight value }
	icon = # name of icon without .dds
}
```

### Variables\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Regiments_modding&veaction=edit&section=2 "Edit section: Variables") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Regiments_modding&action=edit&section=2 "Edit section: Variables")\]

| Variable | Type | Description | Example |
| --- | --- | --- | --- |
| type | string | Unit type | type = skirmishers |
| can\_recruit | block | Optional [trigger](https://ck3.paradoxwikis.com/Triggers "Triggers") (in character scope) for whether or not one can recruit this MaA unit. If not specified (or if specified with an empty block), unit is always recruitable. See "Regiments in Traditions" below. | can\_recruit = { always = no } # Never recruitable |
| damage | int | Unit's damage value | damage = 10 |
| toughness | int | Unit's toughness value | toughness = 10 |
| pursuit | int | Unit's pursuit value | pursuit = 10 |
| screen | int | Unit's screen value | screen = 10 |
| terrain\_bonus | block | Terain bonus | terrain\_bonus = {<br>forest = { damage = 3 screen = 3 } <br>} |
| counters | block | What unit types counters this unit. Can counter multiple units. | counters = {<br>heavy\_infantry = 1<br>} |
| buy\_cost | block | Cost of one unit | buy\_cost = { gold = 150 } |
| low\_maintenance\_cost | block | Low maintenance costs | low\_maintenance\_cost = { gold = 1 } |
| high\_maintenance\_cost | block | High maintenance costs | high\_maintenance\_cost = { gold = 5 } |
| mercenary\_fallback | bool |  | mercenary\_fallback = yes |
| holy\_order\_fallback | bool |  | holy\_order\_fallback = yes |
| stack | int | Amount of units per one stack | stack = 100 |
| max\_sub\_regiments | int |  | max\_sub\_regiments = 5 |
| fallback\_in\_hired\_troops\_if\_unlocked | bool | Mercs/holy orders won't have a preference towards this MaA if it is unlocked | fallback\_in\_hired\_troops\_if\_unlocked = yes |
| allowed\_in\_hired\_troops | bool |  | allowed\_in\_hired\_troops = no |
| fights\_in\_main\_phase | bool | If set, only affects the pursuit phase. Handy for siege weapons | fights\_in\_main\_phase = no |
| siege\_tier | int | How good it is at countering forts | siege\_tier = 1 |
| ai\_quality | Variable | AI weight which is determined in _\\common\\script\_values\\00\_men\_at\_arms\_values_ | value = culture\_ai\_weight\_pikemen |
| icon | string | Name of the .dds icon file to represent this MaA type. If you use custom icon then it should be placed in _\\gfx\\interface\\icons\\regimenttypes\_ | icon = skirmishers |
| hired\_stack\_size | int | Size of sub-regiment for the purpose of hired troops. If not set, this will be the same as the "stack" value | hired\_stack\_size = 25 |
| winter\_bonus | block | Starting from game version 1.3.0, MaA can include Winter Bonus. Can include one or both bonuses (harsh or normal winter) | winter\_bonus = {<br>normal\_winter = { <br>damage = -10 <br>toughness = -5 <br>}<br>harsh\_winter = { <br>damage = -20 <br>toughness = -10 <br>}<br>} |

#### Regiments in Innovations\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Regiments_modding&veaction=edit&section=3 "Edit section: Regiments in Innovations") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Regiments_modding&action=edit&section=3 "Edit section: Regiments in Innovations")\]

If you want your custom Innovation to unlock your custom MaA unit.

```
unlock_maa = my_maa # Use the key of maa unit
```

Or you can also provide bonuses to the regiment.

**Example** (given by CK3 devs):

```
maa_upgrade = {
	type = cavalry
	damage = 0.1
	toughness = 0.1
	pursue = 0.1
	screen = 0.1
	siege_value = 0.1
	max_size = 1
}
```

#### Regiments in Traditions\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Regiments_modding&veaction=edit&section=4 "Edit section: Regiments in Traditions") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Regiments_modding&action=edit&section=4 "Edit section: Regiments in Traditions")\]

If you want your custom cultural tradition to unlock your custom MaA unit.

In the tradition (e.g. `common/culture/traditions/my_traditions.txt`):

```
tradition_example = {
# ...
	parameters = {
		# ...
		unlock_my_maa = yes
		# ...
	}
# ...
}
```

And in the MaA (e.g. `common/men_at_arms_types/my_maa_types.txt`):

```
my_maa = {
# ...
	can_recruit = {
		culture = { has_cultural_parameter = unlock_my_maa }
	}
# ...
}
```

#### Localization\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Regiments_modding&veaction=edit&section=5 "Edit section: Localization") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Regiments_modding&action=edit&section=5 "Edit section: Localization")\]

Example:

```
my_maa_name:0 "My Men at Arms"
my_maa_name_flavor:0 "#F My Men at Arms are better than yours.#!"
```

Note that 'my\_maa\_flavor' is the regiment's description.

**[Modding](https://ck3.paradoxwikis.com/Modding "Modding")**

|     |     |
| --- | --- |
| Documentation | [Scripting](https://ck3.paradoxwikis.com/Scripting "Scripting") • [Scopes](https://ck3.paradoxwikis.com/Scopes "Scopes") • [Effects](https://ck3.paradoxwikis.com/Effects "Effects") • [Triggers](https://ck3.paradoxwikis.com/Triggers "Triggers") • [Variables](https://ck3.paradoxwikis.com/Variables "Variables") • [Modifiers](https://ck3.paradoxwikis.com/Modifier_list "Modifier list") |

|     |     |
| --- | --- |
| Scripting | [AI](https://ck3.paradoxwikis.com/AI_modding "AI modding") • [Bookmarks](https://ck3.paradoxwikis.com/Bookmarks_modding "Bookmarks modding") • [Characters](https://ck3.paradoxwikis.com/Characters_modding "Characters modding") • [Commands](https://ck3.paradoxwikis.com/Commands "Commands") • [Council](https://ck3.paradoxwikis.com/Council_modding "Council modding") • [Culture](https://ck3.paradoxwikis.com/Culture_modding "Culture modding") • [Decisions](https://ck3.paradoxwikis.com/Decisions_modding "Decisions modding") • [Dynasties](https://ck3.paradoxwikis.com/Dynasties_modding "Dynasties modding") • [Events](https://ck3.paradoxwikis.com/Event_modding "Event modding") • [Governments](https://ck3.paradoxwikis.com/Governments_modding "Governments modding") • [History](https://ck3.paradoxwikis.com/History_modding "History modding") • [Holdings](https://ck3.paradoxwikis.com/Holdings_modding "Holdings modding") • [Lifestyles](https://ck3.paradoxwikis.com/Lifestyles_modding "Lifestyles modding") • Regiments • [Religions](https://ck3.paradoxwikis.com/Religions_modding "Religions modding") • [Script Values](https://ck3.paradoxwikis.com/Script_values "Script values") • [Story cycles](https://ck3.paradoxwikis.com/Story_cycles_modding "Story cycles modding") • [Struggles](https://ck3.paradoxwikis.com/Struggle_modding "Struggle modding") • [Titles](https://ck3.paradoxwikis.com/Title_modding "Title modding") • [Traits](https://ck3.paradoxwikis.com/Trait_modding "Trait modding") |

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

Retrieved from " [https://ck3.paradoxwikis.com/index.php?title=Regiments\_modding&oldid=16675](https://ck3.paradoxwikis.com/index.php?title=Regiments_modding&oldid=16675)"

[Categories](https://ck3.paradoxwikis.com/Special:Categories "Special:Categories"):

- [Potentially outdated](https://ck3.paradoxwikis.com/Category:Potentially_outdated "Category:Potentially outdated")
- [1.3](https://ck3.paradoxwikis.com/Category:1.3 "Category:1.3")
- [Modding](https://ck3.paradoxwikis.com/Category:Modding "Category:Modding")