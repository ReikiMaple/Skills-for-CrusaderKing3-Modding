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

# Council modding

From CK3 Wiki

[Jump to navigation](https://ck3.paradoxwikis.com/Council_modding#mw-head) [Jump to search](https://ck3.paradoxwikis.com/Council_modding#searchInput)

Councillors are defined in the _/common/council\_positions/_ folder.
Council tasks are defined in the _/common/council\_tasks/_ folder.

Please note that newly created councillor type will only appear and work in new games. For any councillor type, at least 1 council task has to be defined for the councillor type, or the game will crash when loading.

## Council Positions Structure\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Council_modding&veaction=edit&section=1 "Edit section: Council Positions Structure") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Council_modding&action=edit&section=1 "Edit section: Council Positions Structure")\]

New council positions can be added via the following format:

```
name_of_the_position = {
	# Main skill to look into the character list. If none the best sumk of all the skills will be at the top.
	skill = diplomacy
	special_council_position = yes # Can be held in addition to regular council positions. E.G., the Spouse council position
	auto_fill = yes/no/{ <triggers> } # Will automatically be filled, without the player being able to select who takes the position. Trigger scope: council owner character. Default: no. An empty trigger is treated as 'no'.
	inherit = yes/no/{ <triggers> } #  Position will be inherited by the primary heir if that character is valid to hold the position. Trigger scope: council owner character. Default: no. An empty trigger is treated as 'no'.
	can_fire = yes/no/{ <triggers> } # The councillor can be fired. Trigger scope: council owner character. Default: yes. An empty trigger is treated as 'yes'.
	can_reassign = yes/no/{ <triggers> } # The councillor can be reassigned. Trigger scope: council owner character. Default: yes. An empty trigger is treated as 'yes'.
	can_change_once  = yes/no/{ <triggers> } # The councillor can be assigned, but not reassigned/fired in their lifetime after the assignment. Trigger scope: council owner character. Default: no. An empty trigger is treated as 'no'.

	name = loc_key # What name to use. Be aware that when a position is unfilled, name_of_the_position is used instead
	name = { # Alternatively, you can use triggered loc. SCOPE is the character, event target 'councillor_liege' is the council owner. If no character is provided, we fall back to the key of the position rather than going through triggered loc
		first_valid = { ... }
	}
	# You also need to define the loc key post-fixed with "_possessive" if "special_council_position = yes" is not set (special council positions do not support possessive versions at this time). If you're combining two or more strings using the dynamic description system, only the last key needs "_possessive" defined

	# Modifier applied to the character in this position. Can take a "scale" parameter to scale by (a script value; see _script_values.info). Up to 5 of these can be defined if more than one scale is necessary
	modifier = {
	}

	# Modifier applied to the liege of the character in this position. Can take a "scale" parameter to scale by (a script value; see _script_values.info). Up to 5 of these can be defined if more than one scale is necessary
	council_owner_modifier = {
	}

	# Is this an available position for this council [SCOPE is the CHARACTER owner of the council]
	valid_position = {

	}

	# Is this a valid position for a character. [SCOPE is the character applying to the position]
	valid_character = {

	}

	# Effect applied when a character gets this position. [SCOPE is the character applying to the position]
	on_get_position = {

	}

	# Effect applied when a character lose the position. [SCOPE is the character in the position]
	on_lose_position = {

	}

	# Effect applied when a character is fired from the position. [SCOPE is the character in the position]
	on_fired_from_position = {

	}

	# Max number of positions for this type. For modders. Default 1. Infinite 0 or negative.
	max_amount = 2

	use_for_scheme_power = yes/no
	use_for_scheme_resistance = yes/no

	# Which portrait animation should councillors of this type use in the council window
	portrait_animation = X
}
```

Note that the council\_positions folder does not include court physician.

**[Modding](https://ck3.paradoxwikis.com/Modding "Modding")**

|     |     |
| --- | --- |
| Documentation | [Scripting](https://ck3.paradoxwikis.com/Scripting "Scripting") • [Scopes](https://ck3.paradoxwikis.com/Scopes "Scopes") • [Effects](https://ck3.paradoxwikis.com/Effects "Effects") • [Triggers](https://ck3.paradoxwikis.com/Triggers "Triggers") • [Variables](https://ck3.paradoxwikis.com/Variables "Variables") • [Modifiers](https://ck3.paradoxwikis.com/Modifier_list "Modifier list") |

|     |     |
| --- | --- |
| Scripting | [AI](https://ck3.paradoxwikis.com/AI_modding "AI modding") • [Bookmarks](https://ck3.paradoxwikis.com/Bookmarks_modding "Bookmarks modding") • [Characters](https://ck3.paradoxwikis.com/Characters_modding "Characters modding") • [Commands](https://ck3.paradoxwikis.com/Commands "Commands") • Council • [Culture](https://ck3.paradoxwikis.com/Culture_modding "Culture modding") • [Decisions](https://ck3.paradoxwikis.com/Decisions_modding "Decisions modding") • [Dynasties](https://ck3.paradoxwikis.com/Dynasties_modding "Dynasties modding") • [Events](https://ck3.paradoxwikis.com/Event_modding "Event modding") • [Governments](https://ck3.paradoxwikis.com/Governments_modding "Governments modding") • [History](https://ck3.paradoxwikis.com/History_modding "History modding") • [Holdings](https://ck3.paradoxwikis.com/Holdings_modding "Holdings modding") • [Lifestyles](https://ck3.paradoxwikis.com/Lifestyles_modding "Lifestyles modding") • [Regiments](https://ck3.paradoxwikis.com/Regiments_modding "Regiments modding") • [Religions](https://ck3.paradoxwikis.com/Religions_modding "Religions modding") • [Script Values](https://ck3.paradoxwikis.com/Script_values "Script values") • [Story cycles](https://ck3.paradoxwikis.com/Story_cycles_modding "Story cycles modding") • [Struggles](https://ck3.paradoxwikis.com/Struggle_modding "Struggle modding") • [Titles](https://ck3.paradoxwikis.com/Title_modding "Title modding") • [Traits](https://ck3.paradoxwikis.com/Trait_modding "Trait modding") |

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

Retrieved from " [https://ck3.paradoxwikis.com/index.php?title=Council\_modding&oldid=33854](https://ck3.paradoxwikis.com/index.php?title=Council_modding&oldid=33854)"

[Category](https://ck3.paradoxwikis.com/Special:Categories "Special:Categories"):

- [Modding](https://ck3.paradoxwikis.com/Category:Modding "Category:Modding")