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

# Title modding

From CK3 Wiki

[Jump to navigation](https://ck3.paradoxwikis.com/Title_modding#mw-head) [Jump to search](https://ck3.paradoxwikis.com/Title_modding#searchInput)

Please help with verifying or updating older sections of this article.

At least some were last verified for [version](https://ck3.paradoxwikis.com/CK3_Wiki:Versioning "CK3 Wiki:Versioning") 1.1.

This article is for the PC version of Crusader Kings 3 only.

|     |     |
| --- | --- |
| ![Wiki letter w.png](https://central.paradoxwikis.com/images/6/6a/Wiki_letter_w.png) | Please help improve this article or section by [**expanding it**](https://ck3.paradoxwikis.com/index.php?title=Title_modding&action=edit) with: examples. |

Titles are defined in the _/common/landed\_titles/_ folder

## Contents

- [1Basic Titular Title](https://ck3.paradoxwikis.com/Title_modding#Basic_Titular_Title)
- [2Localization](https://ck3.paradoxwikis.com/Title_modding#Localization)
- [3Coat of Arms](https://ck3.paradoxwikis.com/Title_modding#Coat_of_Arms)
- [4List of attributes](https://ck3.paradoxwikis.com/Title_modding#List_of_attributes)
- [5Duchy Capital Building](https://ck3.paradoxwikis.com/Title_modding#Duchy_Capital_Building)
- [6History](https://ck3.paradoxwikis.com/Title_modding#History)
- [7Defining Cultural Names](https://ck3.paradoxwikis.com/Title_modding#Defining_Cultural_Names)

## Basic Titular Title\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Title_modding&veaction=edit&section=1 "Edit section: Basic Titular Title") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Title_modding&action=edit&section=1 "Edit section: Basic Titular Title")\]

A simple titular title can be created with very little difficulty. The title prefix defines the tier.

| Prefix | Tier |
| --- | --- |
| b\_ | Barony (cannot be titular) |
| c\_ | County (cannot be titular) |
| d\_ | Duchy |
| k\_ | Kingdom |
| e\_ | Empire |
| h\_ | Hegemony |

Decide on a name for the title, which is to be added on to the prefix. Then, you must select a color. Colors are defined in RGB. The title can take two color modifiers color and color2, which is optional. The color2 modifier changes the secondary color of your border.:

(As of game version 1.18, color2 is unused and unsupported by the game engine anymore.)

```
k_titular_kingdom_name = {
	color = { 100 255 200 }
}
```

This is the bare minimum required to create a title, and it can now be granted through the console. However, it will lack localization, meaning that it will appear as "k\_titular\_kingdom\_name" in-game.
Please notice that you cannot add titular barony or county titles, since baronies and counties are more linked to the game map itself (like province id for baronies and duchy capital building for counties). As the result, you cannot add county outside the scope of a defined duchy, nor can you add a barony outside the scope of a defined county. Further more, in the scope of any given county, at least 1 barony needs to be defined there, and in the scope of any given barony, the province id must be assigned. See examples below:

```
# all colors will be assigned white just to save typing time

# this works
h_my_hegemony = {
	color = "white"
}
# this works
e_my_empire = {
	color = "white"
}

# this works
k_my_kingdom = {
	color = "white"
}

# this works
d_my_duchy = {
	color = "white"
}

# this does not work
# counties must be defined within the scope of duchies and be assigned with at least 1 barony
c_my_county = {
	color = "white"
}

# this does not work
# baronies must be defined within the scope of counties and be assigned with a province id
b_my_barony = {
	color = "white"
}

# this works
# it's ok to put counties in an orphan duchy/kingdom
d_my_another_duchy = {
	color = "white"
	c_my_another_county = {
		color = "white"
		b_my_another_barony = {
			color = "white"
			province = 12345 # the province id defined in map_data
		}
	}
}
```

## Localization\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Title_modding&veaction=edit&section=2 "Edit section: Localization") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Title_modding&action=edit&section=2 "Edit section: Localization")\]

A title requires two localization keys to be defined.

- <title\_name>
- <title\_name>\_adj

Additionally, a title can have a unique article. For example Byzantium is 'the ' Byzantine Empire.

- <title\_name>\_article

Vanilla title localization can be found in _/localization/<language>/titles\_l\_<language>.yml_.

## Coat of Arms\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Title_modding&veaction=edit&section=3 "Edit section: Coat of Arms") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Title_modding&action=edit&section=3 "Edit section: Coat of Arms")\]

[Coat of Arms modding](https://ck3.paradoxwikis.com/Coat_of_arms_modding "Coat of arms modding")

## List of attributes\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Title_modding&veaction=edit&section=4 "Edit section: List of attributes") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Title_modding&action=edit&section=4 "Edit section: List of attributes")\]

Below is a list of attributes that can be applied to a title.

| Attribute | Type | Description | Example |
| --- | --- | --- | --- |
| color | rgb | The color of the title displayed on the map | color = { 100 255 200 } |
| color2 | rgb | Changes the secondary color of your border | color2 = { 150 240 200 } |
| definite\_form | boolean | If yes, the title prefix (e.g. "Kingdom of" or "Duchy of" will not be used) It most often used when the type of title is included in the name already, in order to avoid "Empire of the Byzantine Empire", for example. | definite\_form = yes |
| ruler\_uses\_title\_name | boolean |  | ruler\_uses\_title\_name = no |
| landless | boolean | If yes, the title will always exist once it has been made. This allows, for example, religious heads to continue to exist even when unlanded. | landless = yes |
| capital | title | The preferred (de jure?) capital of the title | capital = c\_roma |
| ai\_primary\_priority | clause | Determines how likely AI is to make this title their primary title. Conditions can be used to alter the primary score. | ai\_primary\_priority = {<br>if = {<br>limit = {<br>culture = culture:greek<br>}<br>add = @correct\_culture\_primary\_score<br>}<br>if = {<br>limit = {<br>NOT = { culture = culture:greek }<br>culture\_group = culture\_group:byzantine\_group<br>}<br>add = @better\_than\_the\_alternatives\_score<br>}<br>} |
| destroy\_if\_invalid\_heir |  | Destroys the title if the heir (having just inherited the title?) is invalid. (To prevent a character of the wrong religion holding a religious head title, for example) | destroy\_if\_invalid\_heir = yes |
| no\_automatic\_claims | boolean |  | no\_automatic\_claims = yes |
| always\_follows\_primary\_heir | boolean | The title will always go to the holder's primary heir | always\_follows\_primary\_heir = yes |
| de\_jure\_drift\_disabled | boolean | Prevents the title from de jure drifting into a kingdom or empire | de\_jure\_drift\_disabled = yes |
| male\_names/female\_names | list<string> | A list of names that can be adopted by the title holder. For example, this allows the Pope to gain a Papal name upon his election. | male\_names = { Alexander Anastasius Benedictus Caelestinus Callistus Clemens Eugenius Leo Gregorius Hadrianus Honorius Innocentius Ioannes Lucius Marinus Martinus Nicolaus Sergius Silvester Stephanus Urbanus Victor } |
| name\_list | clause | If the title is held by somebody with culture X, the title name will use the Y localization key and the adjective will use Y\_adj | name\_list = { name\_list\_X = Y} |
| province | ID | The province ID of a barony | province = 3699 |

## Duchy Capital Building\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Title_modding&veaction=edit&section=5 "Edit section: Duchy Capital Building") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Title_modding&action=edit&section=5 "Edit section: Duchy Capital Building")\]

To locate the duchy capital building in the defined de jure duchy capital, list the capital as the first county defined under the duchy title. The special duchy building is placed in the first listed barony of the first listed county, even if a different county is defined as the capital. - doesn't seem correct anymore

## History\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Title_modding&veaction=edit&section=6 "Edit section: History") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Title_modding&action=edit&section=6 "Edit section: History")\]

The history is definded with textfiles located at: <Mod\_root>\\history\\titles\\<filename>.txt

Some important attributes can only be set via the history of the titles.

- **Holder**: The holder is a reference to a char ID (which does not have to be a number in CK3, but can also be a string) - the holder should also be alive, otherwise there is a risk of an error or a crash. Depending on the government or title, errors can also occur - for example, a Muslim cannot be the Catholic Pope. If set to 0 the title is destroyed. This doesn't work for contries or baronies.
- **Government**: This allows the form of government to be set. Without setting the variables, the government will determine the holding (castle, church, city or tribal). Warning! If you work improperly with history and a person has many titles at different times, strange and undesirable cross effects can happen. If, for example, a few years later a feudal emperor gets a county that was historically a republic, it could happen that the feudal empire becomes a republic. One should work with the government as cautiously.
- **Liege**: The liege refers to a higher title. If this value is set, this title is a vassal of the other title until the value is reset. This can lead to strange events if you work improperly. If the history of a county states that it is a vassal of an emperor but that county is later conquered by an independent king, this can lead to the king being interpreted as a vassal of the emperor at the start of the game. The liege can be solved by setting it to 0. This corresponds to independence.
- **De jure Liege**: With this attribute you can carry out a de jure shift of a title. Also works for Counties and results in critical errors if done with Barony. You can also set it to 0 - then the title no longer has a de jure master.
- **Development**: The development of an area can be stopped here. If the value is applied to a high title (e.g. Kingdom), this is also transferred to titles below it. CK3 reads and executes these commands in the order they appear in the text files. That's why you should do big titles first and then small ones. So you can then set all of Italy to 8 but then Rome to 12. Conversely, Rome would be overwritten by Italy, assuming that time is equal, of course.
- **Succession Law(s)**: Special succession laws for a title are also set via the title history. Since a title can have several such laws (e.g. only men and elective monarchy), they must be in a {} block.
- **Court Language**: If you have Royal Court active as DLC, a rank 4 (Kingdom) or 5 (Empire) title can have a court language, although the default is always the language corresponding to the culture of the title holder, so you will probably only need this very rarely. Points to the ID of the language. It is recommended to put a DLC check block in front of it.

  - Note it is also possible to reduce the royal court requirement in 00\_defines.txt, and all ranks can have royal courts if modified in defines.
- **Capital County**: You may wish for a title's de jure capital to vary with different start dates. This can be done using the effect with set\_capital\_county in the title history. There is an example of this in the main game - the capital of England is Winchester at the 867 start and London in subsequent start dates. This effect can also move the duchy capital, but doing so will not move the special building slot, so its primary use is cosmetic. You also cannot use this effect to make another barony the capital of a county.

The following code box demonstrates the more important attributes.

```
d_NAME={
	YYYY.MM.DD={
		holder = <historical_char_id> # 0 if title should no longer exists
		government = <feudal/theocracy/clan/republican/holy_order>_government
		liege = k_NAME # Musst be a higher tier or 0 if independent now
		de_jure_liege = k_OTHER # de jure part of
		change_development_level = INT #
		succession_laws = { <NAME>_succession_law }

		set_court_language = language_NAME # consider a has_dlc_feature = royal_court block before

		effect = {
			set_capital_county = title:c_<NAME> # Relocate capital province - like Winchester to London
		}
	}
}
```

You should have an entry for each title at least for the start date. If a title does not have a starting entry, the game will do the following:

If county

-Does a valid (also living & existing) dujure carrier exist?

--If so, take the bottom one and give this county to him

--If not, create a random character according to the current culture and beliefs of the county capital and create an independent 1-province county

If Barony

-Create a random character according to culture and beliefs and become a vassal of the county owner.

Otherwise

-Title is not created

One should be very careful with the barony. It is possible to create an independent barony or a barony, which can already lead to big mistakes. It is therefore recommended, if possible, not to define barony in the title or, if so, to always add "liege" according to the county in order to avoid possible sources of error. If not set development is 0.

## Defining Cultural Names\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Title_modding&veaction=edit&section=7 "Edit section: Defining Cultural Names") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Title_modding&action=edit&section=7 "Edit section: Defining Cultural Names")\]

In common\\landed\_titles\\landed\_titles.txt, the cultural name (A title with variant names according to the culture of the wielder) of your title may be defined using the following code.

```
k_titular_kingdom_name = {
	color = { 100 255 200 }
	cultural_names = {
		name_list_culture_name = cn_kingdom_name
	}
}
```

Localization for cn\_kingdom\_name would be found at localization\\localization\\<language>\\custom\_titles\_cultural\_names\_I\_<language>.txt and code for the data of name\_list\_culture\_name would be found at common\\culture\\cultures\\custom\_culture\_name.txt

**[Modding](https://ck3.paradoxwikis.com/Modding "Modding")**

|     |     |
| --- | --- |
| Documentation | [Scripting](https://ck3.paradoxwikis.com/Scripting "Scripting") • [Scopes](https://ck3.paradoxwikis.com/Scopes "Scopes") • [Effects](https://ck3.paradoxwikis.com/Effects "Effects") • [Triggers](https://ck3.paradoxwikis.com/Triggers "Triggers") • [Variables](https://ck3.paradoxwikis.com/Variables "Variables") • [Modifiers](https://ck3.paradoxwikis.com/Modifier_list "Modifier list") |

|     |     |
| --- | --- |
| Scripting | [AI](https://ck3.paradoxwikis.com/AI_modding "AI modding") • [Bookmarks](https://ck3.paradoxwikis.com/Bookmarks_modding "Bookmarks modding") • [Characters](https://ck3.paradoxwikis.com/Characters_modding "Characters modding") • [Commands](https://ck3.paradoxwikis.com/Commands "Commands") • [Council](https://ck3.paradoxwikis.com/Council_modding "Council modding") • [Culture](https://ck3.paradoxwikis.com/Culture_modding "Culture modding") • [Decisions](https://ck3.paradoxwikis.com/Decisions_modding "Decisions modding") • [Dynasties](https://ck3.paradoxwikis.com/Dynasties_modding "Dynasties modding") • [Events](https://ck3.paradoxwikis.com/Event_modding "Event modding") • [Governments](https://ck3.paradoxwikis.com/Governments_modding "Governments modding") • [History](https://ck3.paradoxwikis.com/History_modding "History modding") • [Holdings](https://ck3.paradoxwikis.com/Holdings_modding "Holdings modding") • [Lifestyles](https://ck3.paradoxwikis.com/Lifestyles_modding "Lifestyles modding") • [Regiments](https://ck3.paradoxwikis.com/Regiments_modding "Regiments modding") • [Religions](https://ck3.paradoxwikis.com/Religions_modding "Religions modding") • [Script Values](https://ck3.paradoxwikis.com/Script_values "Script values") • [Story cycles](https://ck3.paradoxwikis.com/Story_cycles_modding "Story cycles modding") • [Struggles](https://ck3.paradoxwikis.com/Struggle_modding "Struggle modding") • Titles • [Traits](https://ck3.paradoxwikis.com/Trait_modding "Trait modding") |

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

Retrieved from " [https://ck3.paradoxwikis.com/index.php?title=Title\_modding&oldid=32469](https://ck3.paradoxwikis.com/index.php?title=Title_modding&oldid=32469)"

[Categories](https://ck3.paradoxwikis.com/Special:Categories "Special:Categories"):

- [Potentially outdated](https://ck3.paradoxwikis.com/Category:Potentially_outdated "Category:Potentially outdated")
- [1.1](https://ck3.paradoxwikis.com/Category:1.1 "Category:1.1")
- [Expand](https://ck3.paradoxwikis.com/Category:Expand "Category:Expand")
- [Modding](https://ck3.paradoxwikis.com/Category:Modding "Category:Modding")