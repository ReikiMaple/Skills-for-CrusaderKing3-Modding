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

# Terrain modding

From CK3 Wiki

[Jump to navigation](https://ck3.paradoxwikis.com/Terrain_modding#mw-head) [Jump to search](https://ck3.paradoxwikis.com/Terrain_modding#searchInput)

This article is [timeless](https://ck3.paradoxwikis.com/Category:Timeless "Category:Timeless") and should be accurate for any version of the game.

Terrain modding allows for the creation or modification of [terrain](https://ck3.paradoxwikis.com/Terrain "Terrain") on the map

## Contents

- [1Creating a Terrain Type](https://ck3.paradoxwikis.com/Terrain_modding#Creating_a_Terrain_Type)
  - [1.1Scripting](https://ck3.paradoxwikis.com/Terrain_modding#Scripting)
  - [1.2Graphics](https://ck3.paradoxwikis.com/Terrain_modding#Graphics)
  - [1.3Localization](https://ck3.paradoxwikis.com/Terrain_modding#Localization)
- [2Modifiers](https://ck3.paradoxwikis.com/Terrain_modding#Modifiers)
  - [2.1Modifiers used in terrains](https://ck3.paradoxwikis.com/Terrain_modding#Modifiers_used_in_terrains)
  - [2.2Generated modifiers](https://ck3.paradoxwikis.com/Terrain_modding#Generated_modifiers)
- [3Terrain mapping](https://ck3.paradoxwikis.com/Terrain_modding#Terrain_mapping)

## Creating a Terrain Type\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Terrain_modding&veaction=edit&section=1 "Edit section: Creating a Terrain Type") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Terrain_modding&action=edit&section=1 "Edit section: Creating a Terrain Type")\]

### Scripting\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Terrain_modding&veaction=edit&section=2 "Edit section: Scripting") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Terrain_modding&action=edit&section=2 "Edit section: Scripting")\]

Terrain types are defined in `common/terrain_types/`. Below is a list of all keys usable when defining a terrain type.

| Attribute | Type | Description | Example |
| --- | --- | --- | --- |
| movement\_speed | number(mult) | Speed on this type of terrain | ```<br>movement_speed = 0.8<br>``` |
| attacker\_modifier | list<modifiers> | Modifiers for the attackers in a combat.<br>See [modifiers](https://ck3.paradoxwikis.com/Terrain_modding#Modifiers "Terrain modding"). | ```<br>attacker_modifier = {<br>	hard_casualty_modifier = 0.2<br>	retreat_losses = 0.25<br>}<br>``` |
| defender\_modifier | list<modifiers> | Modifiers for the defender in a combat.<br>See [modifiers](https://ck3.paradoxwikis.com/Terrain_modding#Modifiers "Terrain modding"). | ```<br>defender_modifier = {<br>	hard_casualty_modifier = 0.2<br>	retreat_losses = 0.25<br>}<br>``` |
| attacker\_combat\_effects | <combat effect> | Combat effect for the attackers. Look for `common/combat_effects/_combat_effects.info` for more information on how script this one. | ```<br>attacker_combat_effects = {<br>	name = combat_wetlands<br>	image = defender_wetlands<br>	advantage = 5<br>}<br>``` |
| defender\_combat\_effects | <combat effect> | Combat effect for the defenders. Look for `common/combat_effects/_combat_effects.info` for more information on how script this one. | ```<br>defender_combat_effects = {<br>	name = combat_forest<br>	image = defender_forest<br>	advantage = 3<br>}<br>``` |
| color | color | Terrain color for the terrain type map mode | ```<br>color = hsv { 0.3 0.75 0.7 } #50 255 25<br>``` |
| combat\_width | number(mult) | Multiplier on the combat width | ```<br>combat_width = 0.9<br>``` |
| audio\_parameter | number | Used to check the audio to play | ```<br>audio_parameter = 4.0<br>``` |
| province\_modifier | list<modifiers> | Modifier applied to the province.<br>See [modifiers](https://ck3.paradoxwikis.com/Terrain_modding#Modifiers "Terrain modding"). | ```<br>province_modifier = {<br>	supply_limit_mult = -0.1<br>	travel_danger = 45<br>	county_fertility_growth_add = 0.15<br>}<br>``` |
| county\_capital\_modifier | list<modifiers> | Modifier applied to the province if it is the county capital.<br>See [modifiers](https://ck3.paradoxwikis.com/Terrain_modding#Modifiers "Terrain modding"). | ```<br>county_capital_modifier = {<br>	development_growth_factor = -0.05<br>}<br>``` |
| travel\_danger\_score | number | The amount of danger this terrain provides when travelling over it. | ```<br>travel_danger_score = 45<br>``` |
| travel\_danger\_color | color | Terrain color for the travel planner map mode if the danger score is higher than the player's safety. | ```<br>travel_danger_color = hsv { 0.37 0.8 0.5 }<br>``` |
| provision\_cost | number | The amount of provison cost for this terrain type when moving your domicile (landless rulers). | ```<br>provision_cost = 50<br>``` |
| county\_fertility | number | The amount of Fertility contributed by this terrain type. Used to calculate Base County Fertility for relevant counties | ```<br>county_fertility = 15<br>``` |
| entity | string | Environmental graphical asset shown in this terrain. | ```<br>entity = "forest_birds_01"<br>``` |

Terrain type keys
Expand

The `number(mult)` types are decimals (ex. -1 (**-100%**), 0.5 (**+50%**) or 2 (**+200%**)).

Here is a complete example:

```
forest = {
	color = hsv { 0.3 0.75 0.7 } #50 255 25
	travel_danger_color = hsv { 0.37 0.8 0.5 }
	travel_danger_score = forest_danger_value
	provision_cost = @provisions_cost_light
	county_fertility = 15

	province_modifier = {
		supply_limit_mult = -0.1
		travel_danger = forest_danger_value
		county_fertility_growth_add = forest_county_fertility_value
	}

	defender_combat_effects = {
		name = combat_forest
		image = defender_forest
		advantage = 3
	}

	movement_speed = 0.8
	combat_width = 0.9

	audio_parameter = 4.0

	entity = "forest_birds_01"
}
```

### Graphics\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Terrain_modding&veaction=edit&section=3 "Edit section: Graphics") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Terrain_modding&action=edit&section=3 "Edit section: Graphics")\]

Terrain type icons are put in `gfx/interface/icons/terrain_types` in the `.dds` format, with the name `<TERRAIN TYPE KEY>.dds`. (ex. `forest.dds`)

### Localization\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Terrain_modding&veaction=edit&section=4 "Edit section: Localization") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Terrain_modding&action=edit&section=4 "Edit section: Localization")\]

Vanilla localization files are located at `localization/<language>/terrains_l_<language>.yml`.

| Localization key | Description | Example |
| --- | --- | --- |
| <TERRAIN> | The name of the terrain. | `forest:0 "Forest"` |
| combat\_<TERRAIN> | Text used for combat advantages when the terrain have combat modifiers. | `combat_forest:0 "Defending in Forest"` |

Localization keys

## Modifiers\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Terrain_modding&veaction=edit&section=5 "Edit section: Modifiers") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Terrain_modding&action=edit&section=5 "Edit section: Modifiers")\]

### Modifiers used in terrains\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Terrain_modding&veaction=edit&section=6 "Edit section: Modifiers used in terrains") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Terrain_modding&action=edit&section=6 "Edit section: Modifiers used in terrains")\]

Modifiers can be used in a terrain in the following fields : `attacker_modifier`, `defender_modifier`, `province_modifier`, `county_capital_modifier`.

Modifiers referenced by a terrain object can be only generic (hardcoded) modifiers, or modifiers generated from the following databases:

- schemes
- [holdings](https://ck3.paradoxwikis.com/Holdings_modding "Holdings modding")
- lifestyles
- regions

Other generated modifiers are _not_ allowed, such as those from other terrains, men\_at\_arms\_types, cultures, or governments.

### Generated modifiers\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Terrain_modding&veaction=edit&section=7 "Edit section: Generated modifiers") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Terrain_modding&action=edit&section=7 "Edit section: Generated modifiers")\]

Below is a list of modifiers generated for each terrain types:

| Attribute | Type | Description | Example |
| --- | --- | --- | --- |
| attrition\_mult | number(mult) | Attrition multiplier for armies. | ```<br>attrition_mult = 0<br>``` |
| cancel\_negative\_supply | boolean | Discards supply penalties from the terrain type | ```<br>cancel_negative_supply = yes<br>``` |
| advantage | number | Advantage during the combat | ```<br>advantage = 0<br>``` |
| development\_growth | number | Development growth if capital of a county is this terrain | ```<br>development_growth = 1<br>``` |
| development\_growth\_factor | number(mult) | Development growth factor if capital of a county is this terrain | ```<br>development_growth_factor = 0.2<br>``` |
| construction\_gold\_cost | number(mult) | Construction cost in gold of buildings. | ```<br>construction_gold_cost = 0.2<br>``` |
| holding\_construction\_gold\_cost | number(mult) | Construction cost in gold of holdings. | ```<br>holding_construction_gold_cost = 0.2<br>``` |
| construction\_piety\_cost | number(mult) | Construction cost in piety of buildings. | ```<br>construction_piety_cost = 0.2<br>``` |
| holding\_construction\_piety\_cost | number(mult) | Construction cost in piety of holdings. | ```<br>holding_construction_piety_cost = 0.2<br>``` |
| construction\_prestige\_cost | number(mult) | Construction cost in prestige of buildings. | ```<br>construction_prestige_cost = 0.2<br>``` |
| holding\_construction\_prestige\_cost | number(mult) | Construction cost in prestige of holdings. | ```<br>holding_construction_prestige_cost = 0.2<br>``` |
| supply\_limit | number | Changes the army supply limit. | ```<br>supply_limit = 200<br>``` |
| supply\_limit\_mult | number(mult) | Changes the army supply limit factor. | ```<br>supply_limit_mult = 0.2<br>``` |
| tax\_mult | number(mult) | Gold tax multipliers for buildings. | ```<br>tax_mult = 0.2<br>``` |
| levy\_size | number(mult) | Changes the levy size. | ```<br>levy_size = 0.2<br>``` |
| min\_combat\_roll | number | Sets the minimal combat roll. | ```<br>min_combat_roll = 5<br>``` |
| max\_combat\_roll | number | Sets the maximal combat roll. | ```<br>max_combat_roll = 5<br>``` |
| travel\_danger | number | Changes travel danger. | ```<br>travel_danger = 35<br>``` |
| provision\_use\_mult | number(mult) | Provision use for landless characters. | ```<br>provision_use_mult = 0.2<br>``` |

Generated modifiers
Expand

The `number(mult)` types are decimals (ex. -1 (**-100%**), 0.5 (**+50%**) or 2 (**+200%**)).

Generated modifiers can then be used anywhere (traits, struggles...) with the name `<TERRAIN TYPE KEY>_<MODIFIER ATTRIBUTE NAME>`.

For example, writing the following in a trait will add a **+2** advantage in the `forest` terrain.

```
forest_advantage = 2
```

They can also be used in the terrain itself, without the terrain key before. For example, writing the following in a terrain will put a **+2** defender advantage.

```
defender_combat_effects = {
	advantage = 5
}
```

## Terrain mapping\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Terrain_modding&veaction=edit&section=8 "Edit section: Terrain mapping") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Terrain_modding&action=edit&section=8 "Edit section: Terrain mapping")\]

Terrain mapping is defined in `common/province_terrain/00_province_terrain.txt`. Each province needs a defined terrain. More information on provinces are on the [map modding page](https://ck3.paradoxwikis.com/Map_modding#Defining_baronies "Map modding").

**Example**

```
1=biger_plains   #
2=taiga          #
3=plains         #
4=mountains      #
5=hills          #
```

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
| Map | [Map](https://ck3.paradoxwikis.com/Map_modding "Map modding") • Terrain |

|     |     |
| --- | --- |
| Graphics | [3D models](https://ck3.paradoxwikis.com/3D_models "3D models") • [Exporters](https://ck3.paradoxwikis.com/Exporters "Exporters") • [Coat of arms](https://ck3.paradoxwikis.com/Coat_of_arms_modding "Coat of arms modding") • [Graphical assets](https://ck3.paradoxwikis.com/Graphical_assets "Graphical assets") • [Fonts](https://ck3.paradoxwikis.com/Fonts "Fonts") • [Particles](https://ck3.paradoxwikis.com/index.php?title=Particles&action=edit&redlink=1 "Particles (page does not exist)") • [Shaders](https://ck3.paradoxwikis.com/index.php?title=Shaders&action=edit&redlink=1 "Shaders (page does not exist)") • [Unit models](https://ck3.paradoxwikis.com/index.php?title=Unit_models&action=edit&redlink=1 "Unit models (page does not exist)") |

|     |     |
| --- | --- |
| Audio | [Music](https://ck3.paradoxwikis.com/Music_modding "Music modding") • [Sound](https://ck3.paradoxwikis.com/Sound_modding "Sound modding") |

|     |     |
| --- | --- |
| Other | [Console commands](https://ck3.paradoxwikis.com/Console_commands "Console commands") • [Checksum](https://ck3.paradoxwikis.com/Checksum "Checksum") • [Mod structure](https://ck3.paradoxwikis.com/Mod_structure "Mod structure") • [Mod compatibility](https://ck3.paradoxwikis.com/Mod_compatibility "Mod compatibility") • [Modding tools](https://ck3.paradoxwikis.com/Modding_tools "Modding tools") • [Troubleshooting](https://ck3.paradoxwikis.com/Mod_troubleshooting "Mod troubleshooting") |

Retrieved from " [https://ck3.paradoxwikis.com/index.php?title=Terrain\_modding&oldid=30475](https://ck3.paradoxwikis.com/index.php?title=Terrain_modding&oldid=30475)"

[Categories](https://ck3.paradoxwikis.com/Special:Categories "Special:Categories"):

- [Pages with syntax highlighting errors](https://ck3.paradoxwikis.com/index.php?title=Category:Pages_with_syntax_highlighting_errors&action=edit&redlink=1 "Category:Pages with syntax highlighting errors (page does not exist)")
- [Timeless](https://ck3.paradoxwikis.com/Category:Timeless "Category:Timeless")
- [Modding](https://ck3.paradoxwikis.com/Category:Modding "Category:Modding")