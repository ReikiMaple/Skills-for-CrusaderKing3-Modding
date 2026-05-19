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

# History modding

From CK3 Wiki

[Jump to navigation](https://ck3.paradoxwikis.com/History_modding#mw-head) [Jump to search](https://ck3.paradoxwikis.com/History_modding#searchInput)

Please help with verifying or updating older sections of this article.

At least some were last verified for [version](https://ck3.paradoxwikis.com/CK3_Wiki:Versioning "CK3 Wiki:Versioning") 1.1.

This article is for the PC version of Crusader Kings 3 only.

History modding is about applying changes to the data stored at the path _game/history_. The history folder contains subfolders for characters, cultures, provice mapping, provinces, titles and wars.
[Character](https://ck3.paradoxwikis.com/Characters_modding "Characters modding") modding is explained on a dedicated article. Except for characters, where history (birth and death) and other data like name and traits are definded, history modding is only about changing the history not the existence of for example a title.

## Contents

- [1Title history modding](https://ck3.paradoxwikis.com/History_modding#Title_history_modding)
- [2Culture history modding](https://ck3.paradoxwikis.com/History_modding#Culture_history_modding)
- [3Effects](https://ck3.paradoxwikis.com/History_modding#Effects)

## Title history modding\[ [edit](https://ck3.paradoxwikis.com/index.php?title=History_modding&veaction=edit&section=1 "Edit section: Title history modding") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=History_modding&action=edit&section=1 "Edit section: Title history modding")\]

Modding title history means to make changes about the holder history of landed titles and it's affiliation to a specific liege. The files for every existing dejure kingdom can be found at _game/history/titles_. The file contains the data for the kingdom, as well as all of it's dejure duchies and counties. For example the county of Lyon in the file _k\_burgundy.txt_ looks like this:

```
c_lyon = {
	867.1.1 = { change_development_level = 8 }
	1066.1.1 = { change_development_level = 10 }

	765.1.1 = {
		liege = "k_lotharingia"
		holder = 91491 #VUODO, historical count as placeholder
	}
	855.8.23 = {
		liege = "k_burgundy"
		holder = 144998
	}
	863.1.1 = {
		holder = 168238  #Guilhem I de Forez
	}
	863.1.25 = {
		liege = d_dauphine
	}
	871.1.1 = {
		holder = 168239  #Guilhem II de Forez
	}
	925.8.27 = {
		holder = 168240  #Artaud I de Forez
	}
	933.1.1 = {
		liege = k_burgundy
	}
	960.1.1 = {
		holder = 168241  #Geraud I de Forez
	}
	993.1.1 = {
		holder = 168242  #Artaud II de Forez
	}
	1000.10.11 = {
		holder = 168243  #Artaud III de Forez
	}
	1017.1.1 = {
		holder = 10028
	}
	1032.1.1 = {
		liege = e_hre
	}
	1058.1.1 = {
		holder = 20290
	}
	1079.12.1 = {
		holder = 212806
	}
	1097.6.1 = {
		holder = 212807
	}
	1107.1.1 = {
		holder = 205681 #Guy d'Albon
	}
	1138.10.27 = {
		holder = 205680 #Guigues d'Albon
	}
	1163.1.1 = {
		liege = "k_france"
	}
	1187.1.1 = {
		liege = "d_burgundy"
	}
	1193.1.1 = { #Guigues III should hold Lyon from 1193 to his death, after which his brother Archbishop Renaud holds it.
		holder = 205684
	}
	1202.11.28 = {
		holder = 205685 #Archbishop Renaud d'Albon
	}
	1226.10.21 = {
		holder = 138427 #ArchBishop Robert d'Auvergne
	}
	1234.1.1 = {
		holder = 138425 #ArchBishop Raoul I de La Roche-Aymon
	}
	1236.1.1 = {
		holder = 138437 #Bishop Aimery de Rives
	}
	1245.1.1 = {
		holder = 70913 #ArchBishop Philippe I de Savoie
	}
	1267.1.1 = {
		holder = 138438	#Bishop Guy II
	}
	1268.1.1 = {
		holder = 71827 #ArchBishop Pierre II de Tarentaise/future Pope Innocent IV
	}
	1273.1.1 = {
		holder = 138439	#ArchBishop Aymar de Roussillon
	}
	1283.1.1 = {
		holder = 138453 #ArchBishop Raoul II de la Tourette
	}
	1288.1.1 = {
		holder = 138404 #ArchBishop Bérard de Got brother of Pope Clement V
	}
	1294.1.1 = {
		holder = 138440 #ArchBishop Henri I de Villars
	}
	1301.1.1 = {
		holder = 138441	#ArchBishop Louis de Villars
	}
	1308.1.1 = {
		holder = 70926 #ArchBishop Pierre de Savoie
	}
	1312.4.10 = {
		liege = "k_france"
	}
	1332.11.1 = {
		holder = 138442 #ArchBishop Guillaume I de Sure
	}

}
```

Every title needs his id, like here c\_lyon. The Duchy of Viennois for example, it's dejure liege, would have the id d\_dauphine. The second step determines the development of Lyon at the two starting dates. In 867 the county has a development of 8 and in 1066 a development of 10. The following lines set holder and liege at a specific date. It's possible to change the holder by inserting the id of another character. If no other liege or holder is added, they will be identical to the previous entry. A completely missing liege will result in an independent holder. For example Guilhelm de Forez becomes holder of the county with the king of burgundy as his liege on the 1.1.863 and gets transferred as a vassal to the Dauphin of Viennois in 863. He looses the title in 871 to his heir Guilhem II. As there are no changes between 863 and 867 Guilhelm I de Forez will be the Count of Lyon starting at the early bookmark.

In the textfile the lines look like this:

```
855.8.23 = {
		liege = "k_burgundy"
		holder = 144998
	}
	863.1.1 = {
		holder = 168238  #Guilhem I de Forez
	}
	863.1.25 = {
		liege = d_dauphine
	}
	871.1.1 = {
		holder = 168239  #Guilhem II de Forez
	}
	925.8.27 = {
		holder = 168240  #Artaud I de Forez
```

To change a liege at a certain date the line _liege = "x"_ needs to be added inside the brackets of _year.month.day = { }_. This doesn't change the dejure liege, only which kingdom or duchy controls the county. The same can be done with the holder by inserting _holder = id_. Character ids can be found in the one of the _culture.txt_ in _game/history/characters_. In order to make a title independent, use the line _liege = 0_.

To change a title's government type utilize the line _government = "x"_ where x is the government type you wish to enable for this holding at the given time. Please be aware that special government types may require different holdings to be eligible.

```
	866.1.1 = {
		government = theocracy_government #Change to theocratic government
	}
	867.1.1 = {
		government = republic_government #Change to republic government
	}
	868.1.1 = {
		government = feudal_government #Change to feudal government
	}
	869.1.1 = {
		government = clan_government #Change to clan government
	}
	870.1.1 = {
		government = tribal_government #Change to tribal government
	}
	871.1.1 = {
		government = mercenary_government #Change to mercenary government
	}
	872.1.1 = {
		government = holy_order_government #Change to holy order government
	}
```

If modding titles, it is advised to adjust the living dates to those of the assigned holder. For example if an newly added character is assigned as Count of Lyon his death should be identical to the date when a successor takes over the title. If forgotten the mod will keep working, but in the dynasty tree the predecessor won't be Count X of Lyon but instead X of Dynasty Y because he will have lost the title before his death.

## Culture history modding\[ [edit](https://ck3.paradoxwikis.com/index.php?title=History_modding&veaction=edit&section=2 "Edit section: Culture history modding") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=History_modding&action=edit&section=2 "Edit section: Culture history modding")\]

The folder _game/history/cultures_ contains the culture files for all culture groups. For example the frankish culture groups file looks like this:

```
# Frankish
# French
# Occitan
# Outremer

# Norman in separate file

867.1.1 = {
	discover_innovation = innovation_bannus
	discover_innovation = innovation_catapult
	discover_innovation = innovation_quilted_armor
	#
	discover_innovation = innovation_development_01
	discover_innovation = innovation_gavelkind
	discover_innovation = innovation_currency_01
	discover_innovation = innovation_crop_rotation
	discover_innovation = innovation_ledger
}

950.1.1 = {
	discover_innovation = innovation_motte
	discover_innovation = innovation_barracks
	discover_innovation = innovation_mustering_grounds
	#
	discover_innovation = innovation_city_planning
	discover_innovation = innovation_plenary_assemblies
	discover_innovation = innovation_casus_belli
	#
	join_era = culture_era_early_medieval
}

1066 = {
	discover_innovation = innovation_horseshoes
	discover_innovation = innovation_mangonel
	discover_innovation = innovation_arched_saddle
	#
	discover_innovation = innovation_hereditary_rule
	discover_innovation = innovation_royal_prerogative
	discover_innovation = innovation_manorialism
	discover_innovation = innovation_currency_02
}
```

It only contains the innovations discovered at a certain date. The lines are only true for the specific starting date. For example starting in 867 catapults are already discovered, but the date of discovery of the innovation barracks now depends on the cultural heads fascination and not on the year mentionned in the file (which is 950). If starting at a newly created bookmark in 950, every mentioned innovation as well as the past ones from 867 will have been discovered at game start.

Any existing innovation can be added here at a specific date. For example primogenitur can already exist in year 1000:

```
1000.1.1 = {
	discover_innovation = innovation_primogenitur
}
```

Innovation ids can be found in _game/common/culture/innovations_. Which culture is part of which culture group is defined by the associated file in _game/common/culture/cultures_. See also [culture modding](https://ck3.paradoxwikis.com/Culture_modding "Culture modding").

## Effects\[ [edit](https://ck3.paradoxwikis.com/index.php?title=History_modding&veaction=edit&section=3 "Edit section: Effects") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=History_modding&action=edit&section=3 "Edit section: Effects")\]

It is also possible to call effects in history scripts like other dynamic scripts. The ROOT for called effects depends on the type of history. For example, vanilla script has effects called for k\_england:

```
k_england = {
...
	1066.1.5 = {
		holder = 122 # Harold Godwinson
		effect = { # Should technically be the capital after William wins, but London was already quite important, so we'll have it be the capital at game start 1066.
			set_capital_county = title:c_middlesex
		}
	}
...
}
```

**[Modding](https://ck3.paradoxwikis.com/Modding "Modding")**

|     |     |
| --- | --- |
| Documentation | [Scripting](https://ck3.paradoxwikis.com/Scripting "Scripting") • [Scopes](https://ck3.paradoxwikis.com/Scopes "Scopes") • [Effects](https://ck3.paradoxwikis.com/Effects "Effects") • [Triggers](https://ck3.paradoxwikis.com/Triggers "Triggers") • [Variables](https://ck3.paradoxwikis.com/Variables "Variables") • [Modifiers](https://ck3.paradoxwikis.com/Modifier_list "Modifier list") |

|     |     |
| --- | --- |
| Scripting | [AI](https://ck3.paradoxwikis.com/AI_modding "AI modding") • [Bookmarks](https://ck3.paradoxwikis.com/Bookmarks_modding "Bookmarks modding") • [Characters](https://ck3.paradoxwikis.com/Characters_modding "Characters modding") • [Commands](https://ck3.paradoxwikis.com/Commands "Commands") • [Council](https://ck3.paradoxwikis.com/Council_modding "Council modding") • [Culture](https://ck3.paradoxwikis.com/Culture_modding "Culture modding") • [Decisions](https://ck3.paradoxwikis.com/Decisions_modding "Decisions modding") • [Dynasties](https://ck3.paradoxwikis.com/Dynasties_modding "Dynasties modding") • [Events](https://ck3.paradoxwikis.com/Event_modding "Event modding") • [Governments](https://ck3.paradoxwikis.com/Governments_modding "Governments modding") • History • [Holdings](https://ck3.paradoxwikis.com/Holdings_modding "Holdings modding") • [Lifestyles](https://ck3.paradoxwikis.com/Lifestyles_modding "Lifestyles modding") • [Regiments](https://ck3.paradoxwikis.com/Regiments_modding "Regiments modding") • [Religions](https://ck3.paradoxwikis.com/Religions_modding "Religions modding") • [Script Values](https://ck3.paradoxwikis.com/Script_values "Script values") • [Story cycles](https://ck3.paradoxwikis.com/Story_cycles_modding "Story cycles modding") • [Struggles](https://ck3.paradoxwikis.com/Struggle_modding "Struggle modding") • [Titles](https://ck3.paradoxwikis.com/Title_modding "Title modding") • [Traits](https://ck3.paradoxwikis.com/Trait_modding "Trait modding") |

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

Retrieved from " [https://ck3.paradoxwikis.com/index.php?title=History\_modding&oldid=17535](https://ck3.paradoxwikis.com/index.php?title=History_modding&oldid=17535)"

[Categories](https://ck3.paradoxwikis.com/Special:Categories "Special:Categories"):

- [Potentially outdated](https://ck3.paradoxwikis.com/Category:Potentially_outdated "Category:Potentially outdated")
- [1.1](https://ck3.paradoxwikis.com/Category:1.1 "Category:1.1")
- [Modding](https://ck3.paradoxwikis.com/Category:Modding "Category:Modding")