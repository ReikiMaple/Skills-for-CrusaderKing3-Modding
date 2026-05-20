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

# Artifact modding

From CK3 Wiki

[Jump to navigation](https://ck3.paradoxwikis.com/Artifact_modding#mw-head) [Jump to search](https://ck3.paradoxwikis.com/Artifact_modding#searchInput)

Please help with verifying or updating older sections of this article.

At least some were last verified for [version](https://ck3.paradoxwikis.com/CK3_Wiki:Versioning "CK3 Wiki:Versioning") 1.8.

This article is for the PC version of Crusader Kings 3 only.

|     |     |
| --- | --- |
| ![Wiki letter w.png](https://central.paradoxwikis.com/images/6/6a/Wiki_letter_w.png) | Please help improve this article or section by [**expanding it**](https://ck3.paradoxwikis.com/index.php?title=Artifact_modding&action=edit) with: examples, advanced uses. |

[Artifacts](https://ck3.paradoxwikis.com/Artifacts "Artifacts") can be modded into the game.

## Contents

- [1Location](https://ck3.paradoxwikis.com/Artifact_modding#Location)
  - [1.1Templates](https://ck3.paradoxwikis.com/Artifact_modding#Templates)
    - [1.1.1Structure](https://ck3.paradoxwikis.com/Artifact_modding#Structure)
  - [1.2Visuals](https://ck3.paradoxwikis.com/Artifact_modding#Visuals)
    - [1.2.1Structure](https://ck3.paradoxwikis.com/Artifact_modding#Structure_2)
  - [1.3Creation Effect](https://ck3.paradoxwikis.com/Artifact_modding#Creation_Effect)
  - [1.4Creating starting Artifacts](https://ck3.paradoxwikis.com/Artifact_modding#Creating_starting_Artifacts)

## Location\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Artifact_modding&veaction=edit&section=1 "Edit section: Location") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Artifact_modding&action=edit&section=1 "Edit section: Location")\]

The code for the artifacts is spread over several scripts. Most are in the common/artifacts folder. In contrast to titles, artefacts do not exist at the beginning of the game and generally have no history of their own. Artifacts are created exclusively by a creation effect - for historical artifacts, said effect is performed at the beginning of the game.

### Templates\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Artifact_modding&veaction=edit&section=2 "Edit section: Templates") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Artifact_modding&action=edit&section=2 "Edit section: Templates")\]

Templates provide information about the possible uses of an artifact. Here you set for an artifact whether it can be equipped, whether there are usage requirements and a possible replacement effect if the inert does not meet the requirements.

All templates must be in a text file with any name in the folder "common/artifacts/templates" so that the game can find the data.

#### Structure\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Artifact_modding&veaction=edit&section=3 "Edit section: Structure") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Artifact_modding&action=edit&section=3 "Edit section: Structure")\]

```
example_template = {

	# can this character equip this artifact?
	can_equip = {
		always = yes
	}

	# can this character benefit from the full modifiers of the artifact?
	can_benefit = {
		is_christian_trigger = yes
	}

	# can this character reforge this artifact (turn this artifact into another)
	can_reforge = {
		is_christian_trigger = yes
	}

	# can this character repair this artifact (restore its durability)
	can_repair = {
		always = no
	}

	# if a given character does not pass the "can_benefit" trigger then this modifier will be applied instead.
	fallback = {
		monthly_prestige = 0.3
	}

	# Adds the final value to the AI equipping score, note the can_benefit takes precedence over the score when AI equipping
	# artifact_ai_will_equip_score in game/common/script_values/00_artifact_values.txt also effect the final score
	ai_score = {
		value = 100
	}

	# Artifacts with this templates show as unique, default = no
	unique = yes
}
```

For the can\_benefit clause, for example, the following checks can be made for the carry char using **and**, **or**, **not** or **nor**:

- has\_faith = faith:<faith\_key>
- culture = culture:<culture\_key>
  - has\_culture = culture:<culture\_key> # is also working correctly but the cultures loc cannot be loaded on this way so using this is not recommended
- culture = { any\_parent\_culture = { this = culture:<culture\_key> } }
- culture = { has\_cultural\_pillar = <heritage\_key> }
- culture = { has\_cultural\_tradition = <tradition\_key>}
- has\_title = title:<title\_key>
- has\_trait = <trait\_key>
- has\_religion = religion:<religion\_key>
- dynasty = dynasty:<dynasty\_key>

Warning: Using 'has\_dynasty' doesn't appera wrong at the error log but doesn't work ingame

### Visuals\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Artifact_modding&veaction=edit&section=4 "Edit section: Visuals") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Artifact_modding&action=edit&section=4 "Edit section: Visuals")\]

The visuals bundle the 2d and - if available - 3d references for an artifact. A visual entry is accordingly quite simple and usually consists of 2 to three entries. The first entry is a reference to the icon. The icon is a 240px² dds file located in the folder '<modroot>/gfx/interface/icons/artifact'.

For optical reasons, you should keep about 30 pixels of purely transparent space in each direction from the actual object. For example, if you want to insert a bag as an icon, you should first crop the said bag with an image editing program without borders or surroundings. Then the image of the cut object is set in such a way that the larger value of height and width of the image has the value 180px, and the other is scaled accordingly. Then you increase the image size from the center to 240px for height and width. This can be done relatively easily with the image editing program paint.NET, for example. If you don't keep a 30px border in each direction, the icon of the artefact in the in-game artefact shop would overflow the frame of the icon. This has no effect on the gameplay, but it looks bad.

The 3D representation of an artefact is controlled via the asset entry.

[![](https://ck3.paradoxwikis.com/images/thumb/9/93/Modding_artifact_unique_lance_of_longius.png/300px-Modding_artifact_unique_lance_of_longius.png)](https://ck3.paradoxwikis.com/File:Modding_artifact_unique_lance_of_longius.png)

[Enlarge](https://ck3.paradoxwikis.com/File:Modding_artifact_unique_lance_of_longius.png "Enlarge")

The original "artifact\_unique\_lance\_of\_longius.dds" file from CK3 open in paint.net

#### Structure\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Artifact_modding&veaction=edit&section=5 "Edit section: Structure") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Artifact_modding&action=edit&section=5 "Edit section: Structure")\]

```
example = {
	icon = "icon_name.dds"
	asset = "asset_name"

	# optional field with no gameplay effect. Only needed for automatic test artifact generation
	default_type = type_key

	icon = {
		trigger = {
			<trigger>
			#root scope is the owner
			#scope:artifact is the artifact being made
			#scope:artifact.creator is how to access the creator when different from the owner
		}
		reference = "icon_name.dds"
	}
	asset = {
		trigger = {
			<trigger>
		}
		reference = "asset_name"
	}
}
```

### Creation Effect\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Artifact_modding&veaction=edit&section=6 "Edit section: Creation Effect") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Artifact_modding&action=edit&section=6 "Edit section: Creation Effect")\]

Artifacts are only created via an effect. The corresponding scripts are located in the "<mod\_root>\\common\\scripted\_effects\\" folder. The two files of the original game can be used as templates. These are "00\_ep1\_artifact\_creation\_effects.txt" & "01\_exp1\_historical\_artifacts\_creation\_effect.txt".

The actual build effect consists of at least two script blocks.

The first block starts with the "create\_artifact = {...}" keyword. The necessary attributes of the new artefact are set here. In the case of non-historical artefacts, the creation of a generic artefact for different creation cases and quality values is differentiated via large if branching blocks.

The following attributes must be set in the first block:

- name (loc\_ref)
- description (loc\_ref)
- type (artifact type - this decides what kind of artifact it is - e.g. weapon or armor)
- template (see above)
- visuals (see above)
- wealth
- quality
- (initial) history
- modifier (an artifact modifier !)
- save\_scope\_as = newly\_created\_artifact (needed for the second block)

The boolean attribute decaying can also be set - the default value is yes,

The second block has a different function for historical and non-historical artifacts, but always starts with "scope:newly\_created\_artifact = {...}". In the case of historical artefacts, the historical information (i.e. former owners) is submitted here. In the case of a generic artifact, the name and description are set here.

The following example shows the original code for creating the papal crown (historical artifact).

```
create_artifact_papal_tiara_effect = {
	# Get the character the artifact is being made for.
	$OWNER$ = { save_scope_as = owner }
	set_artifact_rarity_illustrious = yes

	# Create the artifact
	create_artifact = {
		name = papal_tiara_name
		description = papal_tiara_description
		template = papal_tiara_template
		type = helmet
		visuals = pope_tiara
		wealth = scope:wealth
		quality = scope:quality
		history = {
			type = created
			date = 800.1.1
			recipient = character:7862 #Leo III - fictitious date, probably somewhere between the 8th and 9th centuries
			location = province:2575 #Rome
		}
		modifier = artifact_monthly_piety_4_modifier
		save_scope_as = newly_created_artifact
		decaying = no
	}

	scope:newly_created_artifact = {
		set_variable = { name = historical_unique_artifact value = yes }
		set_variable = {
			name = relic
			value = flag:christian
		}
		set_variable = {
			name = artifact_succession_title
			value = title:k_papal_state
		}
		set_variable = {
			name = pope_hat
			value = yes
		}
		add_artifact_title_history = {
			target = title:k_papal_state
			date = 816.6.12
		}
		add_artifact_modifier = artifact_monthly_learning_lifestyle_xp_2_modifier
	}
}
```

### Creating starting Artifacts\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Artifact_modding&veaction=edit&section=7 "Edit section: Creating starting Artifacts") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Artifact_modding&action=edit&section=7 "Edit section: Creating starting Artifacts")\]

To create your own starting artifacts, you must either write your own starting code or modify the game's original. The original file for this is the "game\_start.txt" which is in the on\_action directory in the common folder. If you don't want to touch the file, you can also add your own text file (in the same place in the mod directory) and enter the following code, for example.

```
on_game_start = {
    events = {
        special_art_gen.1
    }
}
```

This code then calls the event special\_art\_gen.1 at the beginning of the game. Finally, in the corresponding creation effect, the creation effect for the corresponding effect must be built up. It should also be checked at this point whether the player has the Royal Court DLC, since this brings the first artifact into the game. The following code shows a possible structure to give an historical artifact to an owner of any title.

```
special_art_gen.1 = {
	scope = none
	hidden = yes
	immediate = {
		if = {
			limit = {
				has_dlc_feature = royal_court # DON'T FORGET THIS!
				exists = title:<title>.holder # if you want to give this artefact to a title owner
				current_date > <yyyy/mm/dd>   # If you want to set a min/max startign date for this
			}
			title:<title>.holder = { #other ways to determine a char are possible - this is just an example to do this by an existing (as checked before) title
				create_my_historical_artifact_effect = { OWNER = this }
			}
		}
	}
}
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

Retrieved from " [https://ck3.paradoxwikis.com/index.php?title=Artifact\_modding&oldid=33020](https://ck3.paradoxwikis.com/index.php?title=Artifact_modding&oldid=33020)"

[Categories](https://ck3.paradoxwikis.com/Special:Categories "Special:Categories"):

- [Potentially outdated](https://ck3.paradoxwikis.com/Category:Potentially_outdated "Category:Potentially outdated")
- [1.8](https://ck3.paradoxwikis.com/Category:1.8 "Category:1.8")
- [Expand](https://ck3.paradoxwikis.com/Category:Expand "Category:Expand")
- [Modding](https://ck3.paradoxwikis.com/Category:Modding "Category:Modding")