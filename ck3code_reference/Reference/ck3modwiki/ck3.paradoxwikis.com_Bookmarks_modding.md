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

# Bookmarks modding

From CK3 Wiki

[Jump to navigation](https://ck3.paradoxwikis.com/Bookmarks_modding#mw-head) [Jump to search](https://ck3.paradoxwikis.com/Bookmarks_modding#searchInput)

Please help with verifying or updating older sections of this article.

At least some were last verified for [version](https://ck3.paradoxwikis.com/CK3_Wiki:Versioning "CK3 Wiki:Versioning") 1.1.

This article is for the PC version of Crusader Kings 3 only.

Bookmark modding allows the highlighting of new interesting characters and scenarios on the _Select Start Date_ screen.

## Contents

- [1Creating the bookmark](https://ck3.paradoxwikis.com/Bookmarks_modding#Creating_the_bookmark)
- [2Portraits](https://ck3.paradoxwikis.com/Bookmarks_modding#Portraits)
- [3Bookmark Screen](https://ck3.paradoxwikis.com/Bookmarks_modding#Bookmark_Screen)
  - [3.1Designing the Selection Screen Map](https://ck3.paradoxwikis.com/Bookmarks_modding#Designing_the_Selection_Screen_Map)
  - [3.2Bookmark Coat of Arms](https://ck3.paradoxwikis.com/Bookmarks_modding#Bookmark_Coat_of_Arms)
- [4Buttons](https://ck3.paradoxwikis.com/Bookmarks_modding#Buttons)
- [5Localization](https://ck3.paradoxwikis.com/Bookmarks_modding#Localization)
- [6References](https://ck3.paradoxwikis.com/Bookmarks_modding#References)

## Creating the bookmark\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Bookmarks_modding&veaction=edit&section=1 "Edit section: Creating the bookmark") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Bookmarks_modding&action=edit&section=1 "Edit section: Creating the bookmark")\]

Create a new file or edit a already existing one in the folder mods/yourmod/common/bookmarks with a corresponding name of your choice. Make sure the labeling stays coherent and is referenced in other files with the same ID. For example bm\_3000\_wotr.

Make sure to bracket the file lines correctly.

Start by deciding a startdate, which is written in the year.month.day format like start\_date = 3000.5.12 for the 12th of May, year 3000. Next add a is\_playable = yes to indicate that it is, in fact, undoubtly, playable by a human being.

Next you decide on the selectable special characters and start defining him/her. For example:

```
# Halfdan Whiteshirt (York) ID: 163112
	character = {
		name = "bookmark_northmen_halfdan_whiteshirt"      #name has to be localized
		dynasty = 7514                                     #dynasty ID
		dynasty_splendor_level = 1                         #splendor level
		type = male                                        #gender
		birth = 828.1.1                                    #birthdate - defines the age
		title = d_york                                     #held primary title
		government = feudal_government                     #government type
                culture = norse                                    #culture
		religion = norse_pagan                             #religion
		difficulty = "BOOKMARK_CHARACTER_DIFFICULTY_EASY"  #difficulty shown on screen
		history_id = 163112                                #ID
		position = { 765 590 }                             #where it will be located

		animation = disapproval                            #pose

		# Gudfrid, son who became Duke of Frisia, ID: 168336
		character = {                                      #same thing for the son
			name = "bookmark_northmen_halfdan_whiteshirt_alt_gudfrid"
			relation = "BOOKMARK_RELATION_SON"
			dynasty = 7514
                        type = male
			birth = 844.1.1
                 	culture = norse
                        religion = norse_pagan
			history_id = 168336
			animation = personality_greedy
		}

		# Eldest child and favorite, Saga, ID: 306010
		character = {
			name = "bookmark_northmen_halfdan_whiteshirt_alt_saga"
			relation = "BOOKMARK_RELATION_DAUGHTER"
			dynasty = 7514
			type = female
			birth = 845.1.1
			culture = norse
			religion = norse_pagan
			history_id = 306010
        		animation = worry
		}
	}
```

Character stats and traits are found in the history folder.

## Portraits\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Bookmarks_modding&veaction=edit&section=2 "Edit section: Portraits") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Bookmarks_modding&action=edit&section=2 "Edit section: Portraits")\]

Another folder needed will be bookmark\_portraits, which includes the files for the characters selectable in the bookmark screen. They are auto generated files and do not have to be edited.

You use the console via dump\_bookmark\_portraits. They will get dumped to this folder on Windows :

```
C:\Users\USERNAME\Documents\Paradox Interactive\Crusader Kings III\common\bookmark_portraits
```

If you instead intend on creating the characters personally, then check out the character modding page.

## Bookmark Screen\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Bookmarks_modding&veaction=edit&section=3 "Edit section: Bookmark Screen") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Bookmarks_modding&action=edit&section=3 "Edit section: Bookmark Screen")\]

The bookmarks selection screen is not automatically generated but rather an image of the map. They can be found in \\gfx\\interface\\bookmarks. They are .dds and are custom made. The positions part in the bookmark file looks at this file for where to put a character.

You can also trial-and-error test the positions value by going into debug mode and checking how the position of the characters moves after you save your edits. You may have to flip back to the bookmark for it to work properly. This is prone to crashes.

##### Designing the Selection Screen Map\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Bookmarks_modding&veaction=edit&section=4 "Edit section: Designing the Selection Screen Map") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Bookmarks_modding&action=edit&section=4 "Edit section: Designing the Selection Screen Map")\]

What can be done is just screenshotting the map then putting it in a .dds file. Won't be as pretty as what Paradox did but it works\[1\]

If you want to try to mimic Paradox's design, download a blank copy of the CK3 map and paste the provinces.png map (which can be found by searching the CK3 directory) over it. Using a program like Photoshop or Paint.net, you can now use a magic wand tool to select each barony that comprises your character's realm. Fill this space with a color of your choosing, and set the opacity to something around half. Then, you can create a border or other visual effects on it. You will also have to save a version with only the realm of each bookmarked character showing (with a highlight around it) for when you select it in-game. There is a decent video tutorial for this process. [\[4\]](https://www.youtube.com/watch?v=CxoPHmBTPhw)

It will have to be saved as a .dds file with mipmaps and BC3 encoding.

gui\\frontend\_bookmarks.gui
size = { 1920 1200 }

##### Bookmark Coat of Arms\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Bookmarks_modding&veaction=edit&section=5 "Edit section: Bookmark Coat of Arms") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Bookmarks_modding&action=edit&section=5 "Edit section: Bookmark Coat of Arms")\]

If a title has pre-defined coat of arms, it will properly appear in the bookmark selection screen. If your character has blank coat of arms, that means that title has procedurally generated coat of arms every patch.

You will need to add a new coat of arms for that title under common\\coat of arms. An easy way to do this is to just customize the current coat of arms in-game, click copy to clipboard, and paste it into your coat of arms file. Make sure to remove the 'custom' field.

## Buttons\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Bookmarks_modding&veaction=edit&section=6 "Edit section: Buttons") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Bookmarks_modding&action=edit&section=6 "Edit section: Buttons")\]

You will also need a start button under \\gfx\\interface\\bookmarks\\start\_buttons. This is a more minor detail and copying one of the vanilla buttons will probably be acceptable.

There is also the stained glass banner button - these are located in \\gfx\\interface\\icons\\bookmark\_buttons. Aside from copying the vanilla ones, you can try to mash some of the vanilla ones together with rudimentary skill in photoshop or try to make it look differently with color adjustment.[\[1\]](https://ck3.paradoxwikis.com/Bookmarks_modding#cite_note-1)

## Localization\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Bookmarks_modding&veaction=edit&section=7 "Edit section: Localization") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Bookmarks_modding&action=edit&section=7 "Edit section: Localization")\]

A bookmark _will not load_ if it has any character/title history errors.[\[2\]](https://ck3.paradoxwikis.com/Bookmarks_modding#cite_note-2)

## References\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Bookmarks_modding&veaction=edit&section=8 "Edit section: References") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Bookmarks_modding&action=edit&section=8 "Edit section: References")\]

1. [↑](https://ck3.paradoxwikis.com/Bookmarks_modding#cite_ref-1)Baptism of Rus by Meat Plague. [\[1\]](https://steamcommunity.com/sharedfiles/filedetails/?id=3108225018&tscn=1706983331) See gfx\\interface\\icons\\bookmark\_buttons\\bm\_brus\_1066\_rus.dds
2. [↑](https://ck3.paradoxwikis.com/Bookmarks_modding#cite_ref-2)More Bookmarks by Leviathonix [\[2\]](https://steamcommunity.com/sharedfiles/filedetails/?id=2216670956), Credits to Leviathonix [\[3\]](https://steamcommunity.com/sharedfiles/filedetails/?id=2216670956&searchtext=).

**[Modding](https://ck3.paradoxwikis.com/Modding "Modding")**

|     |     |
| --- | --- |
| Documentation | [Scripting](https://ck3.paradoxwikis.com/Scripting "Scripting") • [Scopes](https://ck3.paradoxwikis.com/Scopes "Scopes") • [Effects](https://ck3.paradoxwikis.com/Effects "Effects") • [Triggers](https://ck3.paradoxwikis.com/Triggers "Triggers") • [Variables](https://ck3.paradoxwikis.com/Variables "Variables") • [Modifiers](https://ck3.paradoxwikis.com/Modifier_list "Modifier list") |

|     |     |
| --- | --- |
| Scripting | [AI](https://ck3.paradoxwikis.com/AI_modding "AI modding") • Bookmarks • [Characters](https://ck3.paradoxwikis.com/Characters_modding "Characters modding") • [Commands](https://ck3.paradoxwikis.com/Commands "Commands") • [Council](https://ck3.paradoxwikis.com/Council_modding "Council modding") • [Culture](https://ck3.paradoxwikis.com/Culture_modding "Culture modding") • [Decisions](https://ck3.paradoxwikis.com/Decisions_modding "Decisions modding") • [Dynasties](https://ck3.paradoxwikis.com/Dynasties_modding "Dynasties modding") • [Events](https://ck3.paradoxwikis.com/Event_modding "Event modding") • [Governments](https://ck3.paradoxwikis.com/Governments_modding "Governments modding") • [History](https://ck3.paradoxwikis.com/History_modding "History modding") • [Holdings](https://ck3.paradoxwikis.com/Holdings_modding "Holdings modding") • [Lifestyles](https://ck3.paradoxwikis.com/Lifestyles_modding "Lifestyles modding") • [Regiments](https://ck3.paradoxwikis.com/Regiments_modding "Regiments modding") • [Religions](https://ck3.paradoxwikis.com/Religions_modding "Religions modding") • [Script Values](https://ck3.paradoxwikis.com/Script_values "Script values") • [Story cycles](https://ck3.paradoxwikis.com/Story_cycles_modding "Story cycles modding") • [Struggles](https://ck3.paradoxwikis.com/Struggle_modding "Struggle modding") • [Titles](https://ck3.paradoxwikis.com/Title_modding "Title modding") • [Traits](https://ck3.paradoxwikis.com/Trait_modding "Trait modding") |

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

Retrieved from " [https://ck3.paradoxwikis.com/index.php?title=Bookmarks\_modding&oldid=19306](https://ck3.paradoxwikis.com/index.php?title=Bookmarks_modding&oldid=19306)"

[Categories](https://ck3.paradoxwikis.com/Special:Categories "Special:Categories"):

- [Potentially outdated](https://ck3.paradoxwikis.com/Category:Potentially_outdated "Category:Potentially outdated")
- [1.1](https://ck3.paradoxwikis.com/Category:1.1 "Category:1.1")
- [Modding](https://ck3.paradoxwikis.com/Category:Modding "Category:Modding")