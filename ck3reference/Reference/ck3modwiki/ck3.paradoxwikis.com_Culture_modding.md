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

# Culture modding

From CK3 Wiki

[Jump to navigation](https://ck3.paradoxwikis.com/Culture_modding#mw-head) [Jump to search](https://ck3.paradoxwikis.com/Culture_modding#searchInput)

Please help with verifying or updating older sections of this article.

At least some were last verified for [version](https://ck3.paradoxwikis.com/CK3_Wiki:Versioning "CK3 Wiki:Versioning") 1.4.

This article is for the PC version of Crusader Kings 3 only.

New cultures, innovations and eras can easily be added into the game using the highly modular design which the game offers.
This article covers every subfolder of _common/culture_.

## Contents

- [1Culture Groups](https://ck3.paradoxwikis.com/Culture_modding#Culture_Groups)
- [2Cultures](https://ck3.paradoxwikis.com/Culture_modding#Cultures)
- [3Culture group ID](https://ck3.paradoxwikis.com/Culture_modding#Culture_group_ID)
- [4Culture ID](https://ck3.paradoxwikis.com/Culture_modding#Culture_ID)

## Culture Groups\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Culture_modding&veaction=edit&section=1 "Edit section: Culture Groups") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Culture_modding&action=edit&section=1 "Edit section: Culture Groups")\]

Each culture belongs to a culture group.

```
name_of_culture_group = {
	graphical_cultures = {
		first_culture_group_coa_gfx
		second_culture_group_coa_gfx
		culture_group_building_gfx
		culture_group_clothing_gfx
		culture_group_unit_gfx
	}
	mercenary_names = {
		{ name = "mercenary_company_name1" coat_of_arms = "mercenary_company_coa1" }
		{ name = "mercenary_company_name2" coat_of_arms = "mercenary_company_coa2" }
		...
	}
	first_culture = {
		...
	}
	second_culture = {
		...
	}
}
```

Below is a list of all parameters that can be set for culture groups.

| Attribute | Type | Description | Example |
| --- | --- | --- | --- |
| name | List<culturegfx> | List of graphical cultures used for coat of arms, buildings, clothings and units. It's possible to give more than one from each type, then all of them will be used. | graphical\_cultures = { steppe\_coa\_gfx } |
| mercenary\_names | List<complex> | List of names and CoAs that can be used by mercenaries of this culture group.

| Parameter | Type | Description |
| --- | --- | --- |
| name | localization key | Localization key for the name of the mercenary. |
| coat\_of\_arms | coat of arm | Optional. Coat of Arm for the name of the mercenary. | | ```<br>mercenary_names = {<br>	{ name = "mercenary_company_ghilman" coat_of_arms = "mc_ghilman" }<br>}<br>``` |

## Cultures\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Culture_modding&veaction=edit&section=2 "Edit section: Cultures") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Culture_modding&action=edit&section=2 "Edit section: Cultures")\]

Each culture belongs to a culture group.

```
name_of_culture_group = {
		...

	first_culture = {
		# graphical_cultures = { ... }

		mercenary_names = {			# Names and CoAs that can be used by mercenaries of this culture
			{ name = "mercenary_company_name1" coat_of_arms = "mercenary_company_coa1" }
			{ name = "mercenary_company_name2" coat_of_arms = "mercenary_company_coa2" }
			...
		}

		color = { 1 0.5 0.2 }	# The color of the culture, used e.g. on the map

                heritage = heritage_name # Name of the heritage the culture belongs to, used to group cultures

		character_modifier = {	# Modifier effects on all characters of the culture
			diplomacy = 1
		}

		male_names = {
			10 = {	// The weight for this group of names, the higher, the more common the name is
				commonNameA commonNameB_baseA commonNameC commonNameD_baseA	// A list of names, nameX_baseY means that nameX is a variant of a base name baseY (e.g. John_John Jan_John Ian_John)
			}
			1 = {
				rareNameA rareNameB
			}
		}

		female_names = {	// Names can also be defined as a single list with no weights
			nameA_baseB nameB nameC_baseB
		}

		dynasty_names = {	// Dynasty name list, similar to male_names/female_names, just without weights
			{ dynnp_von dynn_Pommern }	// but it supports defining prefixes in addition to base names. The {} are required then
			{ dynn_Orsini }	// prefixes are optional
			dynn_Fournier	// and so are the {} when not using a prefix
		}
		dynasty_of_location_prefix = "dynnp_von" // when generating a dynasty name based on a title, add this prefix

		# Chance of male children being named after their paternal or maternal grandfather, or their father. Sum must not exceed 100.
		pat_grf_name_chance = 50
		mat_grf_name_chance = 5
		father_name_chance = 10

		# Chance of female children being named after their paternal or maternal grandmother, or their mother. Sum must not exceed 100.
		pat_grm_name_chance = 10
		mat_grm_name_chance = 50
		mother_name_chance = 5

		# Patronyms. Names after the primary parent. Can use both prefix and suffix together ("McDavidson"). _vowel is used for when the parent's name starts with a vowel.
		patronym_prefix_male = "dynnpat_pre_mac"
		patronym_prefix_male_vowel = "dynnpat_pre_vow_mag"
		patronym_prefix_female = "dynnpat_pre_nic"
		patronym_prefix_female_vowel = "dynnpat_pre_vow_nig"

		patronym_suffix_male = "dynnpat_suf_son"
		patronym_suffix_female = "dynnpat_suf_sdaughter"

		# Patronyms will display in names if:
		# - the Character's culture has "always_use_patronym = yes", or
		# - the Character's government has "always_use_patronym = yes", or
		# - the Character's Liege's government has "always_use_patronym = yes"
		# Default is no.
		always_use_patronym = yes

		ethnicities = {
			10 = german		// The weight says how common the ethnicity is within the culture
			10 = caucasian
		}
	}

	second_culture = {
		...
	}
}
```

Below is a list of all parameters that can be set for cultures.

| Attribute | Type | Description | Example |
| --- | --- | --- | --- |
| mercenary\_names | List<complex> | List of names and CoAs that can be used by mercenaries of this culture.

| Parameter | Type | Description |
| --- | --- | --- |
| name | localization key | Localization key for the name of the mercenary. |
| coat\_of\_arms | coat of arm | Optional. Coat of Arm for the name of the mercenary. | | ```<br>mercenary_names = {<br>	{ name = "mercenary_company_1" coat_of_arms = "coa_1" }<br>}<br>``` |
| graphical\_cultures | List<culturegfx> | List of graphical cultures used for coat of arms, buildings, clothings and units. It's possible to give more than one from each type, then all of them will be used. | graphical\_cultures = { english\_coa\_gfx } |
| Color | Decimal RGB Values | Color of the culture. | color = { 0.1 0.75 0.1 } |
| character\_modifier | List<character\_modifiers> | Modifier effects on all characters of the culture. | ```<br>character_modifier = {<br>     diplomacy = 1<br>}<br>``` |
| cadet\_dynasty\_names | List<localization> | List of names for cadet dynasties. | ```<br>cadet_dynasty_names = {<br>     "dynasty_loc"<br>     "dynasty2_loc"<br>}<br>``` |
| dynasty\_names | List<localization> | List of names for dynasties. | ```<br>dynasty_names = {<br>     "dynasty_loc"<br>     "dynasty2_loc"<br>}<br>``` |
| male\_names | List<localization> | List of cultural names for male characters. Names with spaces need enclosing quotation marks. ("Name name2")

| Parameter | Type | Description |
| --- | --- | --- |
| # | name group weight | The weight for this group of names, the higher, the more common the name is. | | ```<br>male_names = {<br>     male_name_1 male-name-2 maleName3 "Male Name 4"<br>}<br>``` |
| female\_names | List<localization> | List of cultural names for male characters. Names with spaces need enclosing quotation marks. ("Name name2")

| Parameter | Type | Description |
| --- | --- | --- |
| # | name group weight | The weight for this group of names, the higher, the more common the name is. | | ```<br>female_names = {<br>     female_name_1 female-name-2 femaleName3 "Female Name 4"<br>}<br>``` |
| dynasty\_of\_location\_prefix | Localization | Cultural equivalent of 'of', when followed by a placename, e.g - Geoffrey 'of' Monmouth, Chrétien 'de' Troyes (Christian 'of' Troyes) | dynasty\_of\_location\_prefix = "prefix" |
| bastard\_dynasty\_prefix | Localization | Optional, Prefix for bastard dynasties | bastard\_dynasty\_prefix = "snow" |
| Male Ancestor Name Chance | Integer | Chance of male children being named after their paternal or maternal grandfather, or their father. Sum must not exceed 100.

| Parameter | Type | Description |
| --- | --- | --- |
| pat\_grf\_name\_chance | integer | Chance of male being named after Paternal Grandfather. |
| mat\_grf\_name\_chance | integer | Chance of male being named after Maternal Grandfather. |
| father\_name\_chance | integer | Chance of male being named after their father. | | ```<br>pat_grf_name_chance = 50 #50% chance of being named after Paternal Grandfather<br>mat_grf_name_chance = 5  #5% chance of being named after Maternal Grandfather<br>father_name_chance = 10  #10% chance of being named after Father<br>``` |
| Female Ancestor Name Chance | Integer | Chance of female children being named after their paternal or maternal grandmother, or their mother. Sum must not exceed 100.

| Parameter | Type | Description |
| --- | --- | --- |
| pat\_grm\_name\_chance | integer | Chance of male being named after Paternal Grandmother. |
| mat\_grm\_name\_chance | integer | Chance of male being named after Maternal Grandmother. |
| mother\_name\_chance | integer | Chance of female being named after their mother. | | ```<br>pat_grm_name_chance = 10 #10% chance of being named after Paternal Grandmother<br>mat_grm_name_chance = 50 #50% chance of being named after Maternal Grandmother<br>mother_name_chance = 5   #5% chance of being named after Mother<br>``` |
| patronym\_prefix\_male | Localization | Names after the primary male parent | patronym\_prefix\_male= "patronym" |
| patronym\_prefix\_male\_vowel | Localization | Names after the primary male parent whose name starts with a vowel | patronym\_prefix\_male\_vowel = "v\_patronym" |
| patronym\_suffix\_male | Localization | Names after the primary male parent but adds a suffix, e.g- Erik _sson_ | patronym\_suffix\_male = "patronym\_s" |
| patronym\_prefix\_female | Localization | Names after the primary female parent | patronym\_prefix\_female = "f\_patronym" |
| patronym\_prefix\_female\_vowel | Localization | Names after the primary female parent whose name starts with a vowel | patronym\_prefix\_female\_vowel = "fv\_patronym" |
| patronym\_suffix\_female | Localization | Names after the primary female parent but adds a suffix, e.g- Ayla _sdaughter_ | patronym\_suffix\_female = "f\_patronym\_s" |
| always\_use\_patronym | Boolean | Optional (default is no), whether or not a culture always displays Patronyms. (Patronyms can also be turned on from government/liege's government) | always\_use\_patronym = yes |
| ethnicities | List<ethnicities> | List of ethnicities common within the culture

| Parameter | Type | Description |
| --- | --- | --- |
| # | ethnicity weight | The weight says how common the ethnicity is within the culture. | | ```<br>ethnicities = {<br>     10 = ethnicity_1<br>      5 = ethnicity_2 #Half as common as ethnicity 1<br>}<br>``` |
| dynasty\_title\_names | Boolean | Optional (default is no), uses dynasty name rather than title name when appropriate | dynasty\_title\_names = yes |
| founder\_named\_dynasties | Boolean | Optional (default is no), uses dynasty name rather than title name when appropriate | founder\_named\_dynasties = yes |
| dynasty\_name\_first | Boolean | Optional (default is no), dynasty name comes before given name (Far-East Style) | dynasty\_name\_first = yes |  |
| heritage | ID | The heritage group that the culture will belong to. | heritage = heritage\_north\_germanic |

## Culture group ID\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Culture_modding&veaction=edit&section=3 "Edit section: Culture group ID") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Culture_modding&action=edit&section=3 "Edit section: Culture group ID")\]

Culture groups have an internal ID used within the game files. To get a culture group's ID from its in-game name:

1. Turn all letters into lowercase (`A...Z->a...z`).
2. Replace spaces (``) and hyphens (`-`) with underscores (`_`).
3. Add `_group` to the end.

Groups that do not follow the convention above have been listed in this table:

| Culture group | Internal ID |
| --- | --- |
| Horn African | somalian\_group |
| Guinean Uplander | west\_african\_group |

## Culture ID\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Culture_modding&veaction=edit&section=4 "Edit section: Culture ID") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Culture_modding&action=edit&section=4 "Edit section: Culture ID")\]

Similar to the above, each culture has an internal ID. To get a culture's ID from its in-game name:

1. Turn all letters into lowercase (`A...Z->a...z`).
2. Remove any diacritics from letters, including accents (`á->a`) and umlauts/diaereses (`ü->u`).

Cultures that do not fit this pattern have been listed below:

| Culture | Internal ID |
| --- | --- |
| Qaw | gaw |
| Permian | komi |
| Ostyak | khanty |
| Bjarmian | samoyed |
| Scots | scottish |
| Pomeranian | pommeranian |
| Oghuz | turkish |
| Mashriqi | levantine |
| Syriac | assyrian |
| Kannauji | hindustani |
| Kamrupi | assamese |
| Rajasthani | rajput |

**[Modding](https://ck3.paradoxwikis.com/Modding "Modding")**

|     |     |
| --- | --- |
| Documentation | [Scripting](https://ck3.paradoxwikis.com/Scripting "Scripting") • [Scopes](https://ck3.paradoxwikis.com/Scopes "Scopes") • [Effects](https://ck3.paradoxwikis.com/Effects "Effects") • [Triggers](https://ck3.paradoxwikis.com/Triggers "Triggers") • [Variables](https://ck3.paradoxwikis.com/Variables "Variables") • [Modifiers](https://ck3.paradoxwikis.com/Modifier_list "Modifier list") |

|     |     |
| --- | --- |
| Scripting | [AI](https://ck3.paradoxwikis.com/AI_modding "AI modding") • [Bookmarks](https://ck3.paradoxwikis.com/Bookmarks_modding "Bookmarks modding") • [Characters](https://ck3.paradoxwikis.com/Characters_modding "Characters modding") • [Commands](https://ck3.paradoxwikis.com/Commands "Commands") • [Council](https://ck3.paradoxwikis.com/Council_modding "Council modding") • Culture • [Decisions](https://ck3.paradoxwikis.com/Decisions_modding "Decisions modding") • [Dynasties](https://ck3.paradoxwikis.com/Dynasties_modding "Dynasties modding") • [Events](https://ck3.paradoxwikis.com/Event_modding "Event modding") • [Governments](https://ck3.paradoxwikis.com/Governments_modding "Governments modding") • [History](https://ck3.paradoxwikis.com/History_modding "History modding") • [Holdings](https://ck3.paradoxwikis.com/Holdings_modding "Holdings modding") • [Lifestyles](https://ck3.paradoxwikis.com/Lifestyles_modding "Lifestyles modding") • [Regiments](https://ck3.paradoxwikis.com/Regiments_modding "Regiments modding") • [Religions](https://ck3.paradoxwikis.com/Religions_modding "Religions modding") • [Script Values](https://ck3.paradoxwikis.com/Script_values "Script values") • [Story cycles](https://ck3.paradoxwikis.com/Story_cycles_modding "Story cycles modding") • [Struggles](https://ck3.paradoxwikis.com/Struggle_modding "Struggle modding") • [Titles](https://ck3.paradoxwikis.com/Title_modding "Title modding") • [Traits](https://ck3.paradoxwikis.com/Trait_modding "Trait modding") |

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

Retrieved from " [https://ck3.paradoxwikis.com/index.php?title=Culture\_modding&oldid=15428](https://ck3.paradoxwikis.com/index.php?title=Culture_modding&oldid=15428)"

[Categories](https://ck3.paradoxwikis.com/Special:Categories "Special:Categories"):

- [Potentially outdated](https://ck3.paradoxwikis.com/Category:Potentially_outdated "Category:Potentially outdated")
- [1.4](https://ck3.paradoxwikis.com/Category:1.4 "Category:1.4")
- [Modding](https://ck3.paradoxwikis.com/Category:Modding "Category:Modding")