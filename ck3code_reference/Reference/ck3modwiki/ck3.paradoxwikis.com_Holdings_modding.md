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

# Holdings modding

From CK3 Wiki

[Jump to navigation](https://ck3.paradoxwikis.com/Holdings_modding#mw-head) [Jump to search](https://ck3.paradoxwikis.com/Holdings_modding#searchInput)

Please help with verifying or updating older sections of this article.

At least some were last verified for [version](https://ck3.paradoxwikis.com/CK3_Wiki:Versioning "CK3 Wiki:Versioning") 1.3.

This article is for the PC version of Crusader Kings 3 only.

## Contents

- [1Creating a Holding](https://ck3.paradoxwikis.com/Holdings_modding#Creating_a_Holding)
- [2Variables](https://ck3.paradoxwikis.com/Holdings_modding#Variables)
- [3Game Concept](https://ck3.paradoxwikis.com/Holdings_modding#Game_Concept)
- [4Modifiers](https://ck3.paradoxwikis.com/Holdings_modding#Modifiers)
  - [4.1List of generated modifiers](https://ck3.paradoxwikis.com/Holdings_modding#List_of_generated_modifiers)
- [5Localization](https://ck3.paradoxwikis.com/Holdings_modding#Localization)
- [6Adding more buildings](https://ck3.paradoxwikis.com/Holdings_modding#Adding_more_buildings)

### Creating a Holding\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Holdings_modding&veaction=edit&section=1 "Edit section: Creating a Holding") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Holdings_modding&action=edit&section=1 "Edit section: Creating a Holding")\]

Holdings are defined in /Crusader Kings III/game/common/holdings

**Example**

```
my_holding = {
	primary_building = my_01

	buildings = {
		mychurch_01
		mycastle_01
		myarmoury_01
	}

	flag = myflag
}
```

### Variables\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Holdings_modding&veaction=edit&section=2 "Edit section: Variables") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Holdings_modding&action=edit&section=2 "Edit section: Variables")\]

| Variable | Type | Description | Example |
| --- | --- | --- | --- |
| primary\_building | string | The key of the building that is generated at the start. | primary\_building = tribe\_01 |
| buildings | block | Assign what buildings are available for this holding type | buildings = {<br>palisades\_01<br>war\_camps\_01<br>longhouses\_01<br>market\_villages\_01<br>} |
| flag | string | Optional flags that are assigned to the holding type | flag = tribal |
| can\_be\_inherited | bool | Can the holding type be inherited. | can\_be\_inherited = yes |

### Game Concept\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Holdings_modding&veaction=edit&section=3 "Edit section: Game Concept") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Holdings_modding&action=edit&section=3 "Edit section: Game Concept")\]

You can also add .dds icon for your holding in /Crusader Kings III/game/game/common/game\_concepts

```
my_holding = {
	alias = { my mine mine_holding }
	parent = holding_type
	texture = "gfx/interface/icons/my_holding_icon.dds"
}
```

### Modifiers\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Holdings_modding&veaction=edit&section=4 "Edit section: Modifiers") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Holdings_modding&action=edit&section=4 "Edit section: Modifiers")\]

Upon loading holding types, modifiers are automatically generated.
You can then modify them in /Crusader Kings III/game/game/common/modifiers (they are not declared there)

If you want your mod to have a modifier that modifies build speed then it's as simple as:

```
my_modifier = {
	icon = my_icon
	my_holding_build_speed = -0.25
}
```

##### List of generated modifiers\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Holdings_modding&veaction=edit&section=5 "Edit section: List of generated modifiers") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Holdings_modding&action=edit&section=5 "Edit section: List of generated modifiers")\]

- <holding\_type>\_build\_speed
- <holding\_type>\_build\_gold\_cost
- <holding\_type>\_build\_piety\_cost
- <holding\_type>\_build\_prestige\_cost
- <holding\_type>\_holding\_build\_speed
- <holding\_type>\_holding\_build\_gold\_cost
- <holding\_type>\_holding\_build\_piety\_cost
- <holding\_type>\_holding\_build\_prestige\_cost

### Localization\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Holdings_modding&veaction=edit&section=6 "Edit section: Localization") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Holdings_modding&action=edit&section=6 "Edit section: Localization")\]

Example:

```
my_holding:0 "Holding"
my_holding_concept_key:0 "[mine|E]"
```

### Adding more buildings\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Holdings_modding&veaction=edit&section=7 "Edit section: Adding more buildings") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Holdings_modding&action=edit&section=7 "Edit section: Adding more buildings")\]

Buildings are defined in /Crusader Kings III/game/game/common/buildings

**Building Structure**

```
name_of_the_building = {

	# How many levies does the building give
	levy = 200

	# How much garrison does the building give
	max_garrison = 100

	# How much garrison regains a percentage of its maximal garrison equal to the garrison reinforcement rate
	garrison_reinforcement_factor = 0.01

	# How long does it take to construct the building
	construction_time = 720

	type = regular/special/duchy_capital	# Specifies whether this is a regular building, a special building, or a duchy capital building. Regular by default

	# Which asset does the building use
	asset = {
		# 'pdxmesh' or 'entity', specifies wheter to use a mesh or an entity. Meshes are more performant and should be preferred.
		type = pdxmesh
		# The name of the mesh or the entity
		name = "western_castle_01_level_03_mesh"
		# To randomize between multiple meshes/entities. Note that they must all be entities, or all be meshes:
		names = { "western_castle_01_level_03a_mesh" "western_castle_01_level_03b_mesh" "western_castle_01_level_03c_mesh" }
		# Path to illustration shown in the county view, texture can be accessed in GUI: "[Holding.GetIllustration]"
		illustration = "path/to/image.dds"
		# Associated sound effect and an optional parameter, can also be just soundeffect = "event:..." if no parameter is needed
		soundeffect = { soundeffect = "event:/SFX/Ambience/3DMapEmitters/Holdings/Generic/sfx_amb_3d_holdings_generic_castle" soundparameter = { "Tier" = 2.0 } }
		# Graphical cultures that prefer this asset to be shown
		graphical_cultures = { arabicgfx muslimgfx }
		# Graphical faiths that prefer this asset to be shown (priority is faith > religion > family, so Catholic graphical_faith overrides Abrahamic graphical_faith)
		graphical_faiths = { catholic_gfx orthodox_gfx }
		# Graphical regions in which this asset is preferred, this is the most important criterion when selecting the asset, with the exception of government and province
		graphical_regions = { western mena }
		# Province IDs in which this asset is preferred. Has a higher priority than graphical region.
		provinces = { 496 1000 }
		# Governments that prefer this asset to be shown
		governments = { tribal_government }
	}

	# Is the building enabled? Else won't give any effects to holder, and not be constructible (see can_construct* below).
	# If is_graphical_background = yes, this controls whether the building can be shown in the province.
	# scopes: root is the province; scope:holder is the holder of the province; county is the county title the province belongs to
	is_enabled = {}

	# Can the building be constructed.
	# Use this instead of is_enabled if you want to allow rulers to "use" the building after getting the holding, but to disallow that they construct it.
	# can_construct_potential controls whether the building appears in the build menu. For upgrades it is identical to can_construct_showing_failures_only.
	# Note that is_enabled (see above) is added to can_construct_potential.
	# Not used if is_graphical_background = yes
	# scopes: root is the province; scope:holder is the holder of the province; county is the county title the province belongs to
	can_construct_potential = {}
	can_construct_showing_failures_only = {}
	can_construct = {}
	show_disabled = yes/no	# if set to yes, the building will show in the build menu even if disabled (will still use can_construct_potential). No by default
	# Remember that the building also has to be listed under any holding that is meant to be able to construct it, as described earlier in this page

	# How much cost does the building cost
	cost = { gold = 500 ... }

	# The next building in chain unlocked by this building
	next_building = castle_02

	# Custom description for effects indirectly provided by building.
	# The scope root refers to the buildings province.
	effect_desc = <loc key>

	# A modifier applied to the owner of the holding
	character_modifier = {
	}
	# Applied if the character's culture has the parameter
	character_culture_modifier = {
		parameter = culture param
	}
	# Applied if the character's faith has the parameter
	character_faith_modifier = {
		parameter = faith param
	}

	# A modifier applied if the holder's dynasty of the county has a specific perk
	characer_dynasty_modifier = {
		county_holder_dynasty_perk = fp2_urbanism_legacy_1 # The name of the perk
		# The effect
		monthly_prestige_gain_mult = 0.2
	}

	# A modifier applied to the province
	province_modifier = {
	}
	province_culture_modifier = {
		parameter = culture param
	}
	province_faith_modifier = {
		parameter = faith param
	}
	province_terrain_modifier = {
		parameter = required culture param (optional)
		terrain = required province terrain (optional, default is all terrain types)
		is_coastal = whether this modifier is applied on coastal or non-coastal provinces (optional, default is both coastal and non-coastal)
		is_riverside = whether this modifier is only applied on provinces that are next to a big river or not (optional, default is both riverside and not)
	}

	# A modifier applied if the holder's dynasty of the county has a specific perk
	province_dynasty_modifier = {
		county_holder_dynasty_perk = fp2_urbanism_legacy_1 # The name of the perk
		# The effect
		monthly_income = 0.2
	}

	# A modifier applied to the county
	county_modifier = {
	}
	county_culture_modifier = {
		parameter = culture param
	}
	county_faith_modifier = {
		parameter = faith param
	}

	# A modifier applied to every de jure county in the duchy (if the county has the same de facto liege as this building's county). Can only be used (and only works) for duchy capital buildings.
	duchy_capital_county_modifier = {
	}
	duchy_capital_county_culture_modifier = {
		parameter = culture param
	}
	duchy_capital_county_faith_modifier = {
		parameter = faith param
	}

	# A special modifier applied to every holding of specified type in the county
	county_holding_modifier = {
		holding = castle_holding
		income_mult = 1
	}

	# A modifier applied if the holder's dynasty of the county has a specific perk
	county_dynasty_modifier = {
		county_holder_dynasty_perk = fp2_urbanism_legacy_1 # The name of the perk
		# The effect
		development_growth_factor = 0.2
	}

	# A modifier applied to the county holder
	county_holder_character_modifier = {

	}

	# Building flags
	flag = castle

	# Effects applied on building completion
	# scopes: root refers to the buildings province
	on_complete = {
		<effects>
	}

	# How desirable is the building for the AI
	ai_value = {
		base = 100
	}

	# If this is set to yes, the building will be used for figuring out which background asset (walls/no walls etc) should be shown
	is_graphical_background = no

	### Brief: on_start/on_cancelled/on_complete
	# Effects that happen when construction of the building
	# starts/cancels/finishes.
	#
	# Supported scopes:
	# 		root (Province)
	#			The province the construction took place in.
	#		character
				The character that paid for the construction, if available
	on_start = { ... }
	on_cancelled = { ... }
	on_complete = { ... }
}
```

**Example**

```
 my_building = {

 	construction_time = 720

 	cost_gold =150

 	type = regular/special/duchy_capital

 	can_construct_potential = {
 		#define the requirements for the building to be shown. They are locared in game/common/scripted_triggers
 	}

 	can_construct = { #the requirements for the building to be constructed.
 		building_requirement_castle_city_church = { LEVEL = 01 }
 	}

 	can_construct_showing_failures_only = {
 		building_requirement_tribal = no
 	}

	levy = 100 # The augment of levy this building adds

 	province_modifier = { # add province modifiers here
		stationed_archer_cavalry_toughness_mult = normal_maa_toughness_tier_1
		stationed_archer_cavalry_damage_mult = normal_maa_damage_tier_1
		stationed_archer_cavalry_screen_mult = normal_maa_screen_tier_1
		stationed_archer_cavalry_pursuit_mult = normal_maa_pursuit_tier_1
		travel_danger = -1
	}

	ai_value = { # The priority to build the building
		base = 8
		ai_general_building_modifier = yes
	}
 }
```

**[Modding](https://ck3.paradoxwikis.com/Modding "Modding")**

|     |     |
| --- | --- |
| Documentation | [Scripting](https://ck3.paradoxwikis.com/Scripting "Scripting") • [Scopes](https://ck3.paradoxwikis.com/Scopes "Scopes") • [Effects](https://ck3.paradoxwikis.com/Effects "Effects") • [Triggers](https://ck3.paradoxwikis.com/Triggers "Triggers") • [Variables](https://ck3.paradoxwikis.com/Variables "Variables") • [Modifiers](https://ck3.paradoxwikis.com/Modifier_list "Modifier list") |

|     |     |
| --- | --- |
| Scripting | [AI](https://ck3.paradoxwikis.com/AI_modding "AI modding") • [Bookmarks](https://ck3.paradoxwikis.com/Bookmarks_modding "Bookmarks modding") • [Characters](https://ck3.paradoxwikis.com/Characters_modding "Characters modding") • [Commands](https://ck3.paradoxwikis.com/Commands "Commands") • [Council](https://ck3.paradoxwikis.com/Council_modding "Council modding") • [Culture](https://ck3.paradoxwikis.com/Culture_modding "Culture modding") • [Decisions](https://ck3.paradoxwikis.com/Decisions_modding "Decisions modding") • [Dynasties](https://ck3.paradoxwikis.com/Dynasties_modding "Dynasties modding") • [Events](https://ck3.paradoxwikis.com/Event_modding "Event modding") • [Governments](https://ck3.paradoxwikis.com/Governments_modding "Governments modding") • [History](https://ck3.paradoxwikis.com/History_modding "History modding") • Holdings • [Lifestyles](https://ck3.paradoxwikis.com/Lifestyles_modding "Lifestyles modding") • [Regiments](https://ck3.paradoxwikis.com/Regiments_modding "Regiments modding") • [Religions](https://ck3.paradoxwikis.com/Religions_modding "Religions modding") • [Script Values](https://ck3.paradoxwikis.com/Script_values "Script values") • [Story cycles](https://ck3.paradoxwikis.com/Story_cycles_modding "Story cycles modding") • [Struggles](https://ck3.paradoxwikis.com/Struggle_modding "Struggle modding") • [Titles](https://ck3.paradoxwikis.com/Title_modding "Title modding") • [Traits](https://ck3.paradoxwikis.com/Trait_modding "Trait modding") |

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

Retrieved from " [https://ck3.paradoxwikis.com/index.php?title=Holdings\_modding&oldid=33465](https://ck3.paradoxwikis.com/index.php?title=Holdings_modding&oldid=33465)"

[Categories](https://ck3.paradoxwikis.com/Special:Categories "Special:Categories"):

- [Potentially outdated](https://ck3.paradoxwikis.com/Category:Potentially_outdated "Category:Potentially outdated")
- [1.3](https://ck3.paradoxwikis.com/Category:1.3 "Category:1.3")
- [Modding](https://ck3.paradoxwikis.com/Category:Modding "Category:Modding")