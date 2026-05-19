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

# Mod structure

From CK3 Wiki

[Jump to navigation](https://ck3.paradoxwikis.com/Mod_structure#mw-head) [Jump to search](https://ck3.paradoxwikis.com/Mod_structure#searchInput)

Please help with verifying or updating older sections of this article.

At least some were last verified for [version](https://ck3.paradoxwikis.com/CK3_Wiki:Versioning "CK3 Wiki:Versioning") 1.1.

This article is for the PC version of Crusader Kings 3 only.

Mods are located in the folder _~\\Paradox Interactive\\Crusader Kings III\\mod_:

- Default on Windows: `%USERPROFILE%\Documents\Paradox Interactive\Crusader Kings III\mod`
- Default on Linux: `~/.local/share/Paradox Interactive/Crusader Kings III/mod`

Each mod requires two parts. Both must be located in the folder above and share the same name, barring file extensions; otherwise, the game launcher will _not_ recognise the mod. Note that folder and file names are case sensitive on Mac and Linux.

- A .mod file, a plain text file with metadata required to use the mod.
- A mod folder containing files specific to modding the game, such as events, images, decisions and characters. It may also be a .zip file instead.

## Contents

- [1Creating initial files](https://ck3.paradoxwikis.com/Mod_structure#Creating_initial_files)
- [2The .mod files](https://ck3.paradoxwikis.com/Mod_structure#The_.mod_files)
  - [2.1Syntax](https://ck3.paradoxwikis.com/Mod_structure#Syntax)
  - [2.2Keys](https://ck3.paradoxwikis.com/Mod_structure#Keys)
  - [2.3Basic example](https://ck3.paradoxwikis.com/Mod_structure#Basic_example)
- [3Mod folder](https://ck3.paradoxwikis.com/Mod_structure#Mod_folder)
- [4Tips](https://ck3.paradoxwikis.com/Mod_structure#Tips)

## Creating initial files\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Mod_structure&veaction=edit&section=1 "Edit section: Creating initial files") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Mod_structure&action=edit&section=1 "Edit section: Creating initial files")\]

It is recommended to generate the initial mod files through the game launcher in the interests of speed and avoiding human error.

1. Open the game launcher.
2. Go to All Installed Mods on the left.
3. Press Upload Mod in the top right.
4. Press Create a Mod.
5. Enter a name, version of the mod (not the game), directory (the launcher will create it) and at least one tag. All of these must be completed before you can press Create at the bottom.
   - (Name must be at least 3 symbols long. DIrectory can include spaces, but cannot end with one.)
   - (Directory cannot include non English characters. If your Windows account name have such characters you must use a directory outside your Documents folder.)

The tags offered by the launcher include:

|     |     |
| --- | --- |
| Alternative History | Historical |
| Balance | [Map](https://ck3.paradoxwikis.com/Map_modding "Map modding") |
| [Bookmarks](https://ck3.paradoxwikis.com/Bookmarks_modding "Bookmarks modding") | Portraits |
| Character Focuses | [Religion](https://ck3.paradoxwikis.com/Religion_modding "Religion modding") |
| Character Interactions | Schemes |
| [Culture](https://ck3.paradoxwikis.com/Culture_modding "Culture modding") | [Sound](https://ck3.paradoxwikis.com/Sound_modding "Sound modding") |
| [Decisions](https://ck3.paradoxwikis.com/Decision_modding "Decision modding") | Total Conversion |
| [Events](https://ck3.paradoxwikis.com/Event_modding "Event modding") | [Translation](https://ck3.paradoxwikis.com/Localization "Localization") |
| Fixes | Utilities |
| Gameplay | Warfare |
| Graphics |

This process will create the following:

- The mod folder, named after your mod.
- A _descriptor.mod_ file, contained within the mod folder.
- Another .mod file, this one named after the mod, located alongside the mod folder.

When [uploading](https://ck3.paradoxwikis.com/Modding#Uploading/updating_a_mod "Modding"), you will be able to change the suggested game version, add thumbnail for Paradox Mods and description.

## The .mod files\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Mod_structure&veaction=edit&section=2 "Edit section: The .mod files") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Mod_structure&action=edit&section=2 "Edit section: The .mod files")\]

The .mod files used by the game are plain text files that contain metadata about their corresponding mod. There are two .mod files for every mod:

- _(modname).mod_, located _alongside_ the mod's folder. This one is required; without it, the launcher will not recognise the mod.
- _descriptor.mod_, located _within_ the mod folder. It is recommended to keep this file consistent with the other one, excluding the line containing the _path_ key which is not needed in the descriptor file.

### Syntax\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Mod_structure&veaction=edit&section=3 "Edit section: Syntax") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Mod_structure&action=edit&section=3 "Edit section: Syntax")\]

Similar to other game files, single-line comments can be started using hash (`#`). To set a value to a key, use the format `key="value"` for single values; alternatively, use the following structure for lists:

```
list={
	"element0"
	"element1"
	"element2"
}
```

### Keys\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Mod_structure&veaction=edit&section=4 "Edit section: Keys") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Mod_structure&action=edit&section=4 "Edit section: Keys")\]

The table below describes the keys available for use within the .mod file.

| Keys | Required? | Description | Example |
| --- | --- | --- | --- |
| version | Yes | Allows you to define a version of your mod, defined as a string. | version="0.0.1" |
| tags | No | Sets the tags that mod is considered part of. Correlates with Steam Workshop categories. | ```<br>tags={<br>	"Culture"<br>	"Decisions"<br>	"Fixes"<br>}<br>``` |
| name | Yes | Determines the name that shows up in the launcher. | name="My Mod" |
| supported\_version | Required for file alongside mod folder; not required for descriptor.mod | Defines the latest game version the mod supports; launcher will show a warning if a mod is outdated. The game uses semantic versioning (MAJOR.MINOR.PATCH). Wildcards (`*`) may be used to define a range of versions. | supported\_version="1.1.3" |
| path | Yes | Sets which folder is the mod's folder. Note that it is no longer relative to the main _Crusader Kings III_ folder, but rather to the Crusader Kings III user folder (described above). Alternatively, one can use the entire path. | - `path="C:/Users/Example/Documents/Paradox Interactive/Crusader Kings III/mod/my_mod"` (Windows)<br>- `path="/home/example/.local/share/Paradox Interactive/Crusader Kings III/mod/my_mod"` (Linux)<br>- `path="mod/my_mod"` (Relative, any OS) |
| remote\_file\_id | Required if uploading and updating your own Steam Workshop mod. Set automatically when mod is uploaded. | Must match the Steam Workshop ID of the mod. Can be found at the end of a Steam Workshop URL, such as "2220762808" in [https://steamcommunity.com/sharedfiles/filedetails/?id=2220762808](https://steamcommunity.com/sharedfiles/filedetails/?id=2220762808). | remote\_file\_id="2220762808" |
| picture | No | The picture shown for your mod in the search view and on the mod's page. Steam ignores this key and always looks for thumbnail.png | picture="thumbnail.png" |
| replace\_path | No | Doesn't load vanilla files for the specified path. | replace\_path="history/characters" |

### Basic example\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Mod_structure&veaction=edit&section=5 "Edit section: Basic example") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Mod_structure&action=edit&section=5 "Edit section: Basic example")\]

The example below displays the basic contents of a .mod file. Feel free to copy and paste it for your own .mod file, remembering to change specific details to match your own mod and game version. Note that the descriptor.mod file does _not_ require the `path` key.

```
version="0.0.1"
tags={
	"Culture"
	"Decisions"
	"Fixes"
}
name="My Mod"
supported_version="1.1.3"
path="mod/my_mod"
```

## Mod folder\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Mod_structure&veaction=edit&section=6 "Edit section: Mod folder") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Mod_structure&action=edit&section=6 "Edit section: Mod folder")\]

Files that edit the game must be put inside the mod folder and are then subsequently loaded by the game. Files often have to be put into specific folders, otherwise they may not be loaded by the game. Some general ones have been listed below:

| Type | Folder |
| --- | --- |
| Events | events |
| Decisions | common\\decisions |
| Defines | common\\defines |
| Traits | common\\traits |

For specifics, either consult the relevant modding page using the navigation box at the bottom of this page, or look in the game files (Windows/Steam: `C:/Program Files (x86)/Steam/steamapps/common/Crusader Kings III/game`) and copy the folder structure for a given file up to (and not including) the `game` folder.

## Tips\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Mod_structure&veaction=edit&section=7 "Edit section: Tips") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Mod_structure&action=edit&section=7 "Edit section: Tips")\]

- When editing your mod folder and .mod file(s), you can reload mods in the launcher to update them without restarting it. In the "Mods" section, press "Manage all mods", then "Reload installed mods". Try this if your mod is not showing up.
- Once you have created your initial mod structure, it is highly recommended to use some form of backup system (as simple as copying your files to someplace else), or source control such as Git / Github. This will greatly help if you lose your mod files or somehow break your mod and you want to go back to an old version.
- When creating your .mod file, ensure that you follow the syntax rules correctly, otherwise your mod may not show up at all. For instance, pay attention to using quotation marks (`"`) where needed, especially around values like paths and names.
- Check spelling everywhere, including the contents and names of files and folders. Even the simplest of errors cause the greatest problems.

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
| Other | [Console commands](https://ck3.paradoxwikis.com/Console_commands "Console commands") • [Checksum](https://ck3.paradoxwikis.com/Checksum "Checksum") • Mod structure • [Mod compatibility](https://ck3.paradoxwikis.com/Mod_compatibility "Mod compatibility") • [Modding tools](https://ck3.paradoxwikis.com/Modding_tools "Modding tools") • [Troubleshooting](https://ck3.paradoxwikis.com/Mod_troubleshooting "Mod troubleshooting") |

Retrieved from " [https://ck3.paradoxwikis.com/index.php?title=Mod\_structure&oldid=18579](https://ck3.paradoxwikis.com/index.php?title=Mod_structure&oldid=18579)"

[Categories](https://ck3.paradoxwikis.com/Special:Categories "Special:Categories"):

- [Potentially outdated](https://ck3.paradoxwikis.com/Category:Potentially_outdated "Category:Potentially outdated")
- [1.1](https://ck3.paradoxwikis.com/Category:1.1 "Category:1.1")
- [Modding](https://ck3.paradoxwikis.com/Category:Modding "Category:Modding")