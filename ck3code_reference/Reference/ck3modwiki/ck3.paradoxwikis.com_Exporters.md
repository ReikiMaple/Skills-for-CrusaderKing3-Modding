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

# Exporters

From CK3 Wiki

[Jump to navigation](https://ck3.paradoxwikis.com/Exporters#mw-head) [Jump to search](https://ck3.paradoxwikis.com/Exporters#searchInput)

This article is [timeless](https://ck3.paradoxwikis.com/Category:Timeless "Category:Timeless") and should be accurate for any version of the game.

Modders can use the **exporter tools** that Paradox provides 'as-is'. These can be used to export textures from Photoshop and meshes/animations from Maya.

The Maya exporter is only used internally with Maya 2018, though it may also work on other versions. It will not work with Maya LT, which has limitations on plugin usage.

## Contents

- [1Setup](https://ck3.paradoxwikis.com/Exporters#Setup)
  - [1.1Installation](https://ck3.paradoxwikis.com/Exporters#Installation)
  - [1.2Photoshop Setup](https://ck3.paradoxwikis.com/Exporters#Photoshop_Setup)
  - [1.3Maya Setup](https://ck3.paradoxwikis.com/Exporters#Maya_Setup)
- [2Forum](https://ck3.paradoxwikis.com/Exporters#Forum)

## Setup\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Exporters&veaction=edit&section=1 "Edit section: Setup") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Exporters&action=edit&section=1 "Edit section: Setup")\]

### Installation\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Exporters&veaction=edit&section=2 "Edit section: Installation") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Exporters&action=edit&section=2 "Edit section: Installation")\]

The exporter can be downloaded from here (requires Paradox account):

[Paradox Plaza - Downloads](https://accounts.paradoxplaza.com/profile/downloads)

1. Close Photoshop and Maya
2. Download the exe called "Clausewitz Maya Exporter" (this also includes the Photoshop exporter)
3. Run the Maya Exporter Deploy Wizard, filename 'PdxExporterInstall.exe'. Default settings should be fine
4. Run ExporterInstaller.exe (it should run automatically).
5. You should now have the plugins deployed in the correct places, and a settings file
6. Open the newly-created settings file: 'Documents\\Paradox Interactive\\PdxExporter\\settings\\clausewitz.settings'
7. Replace the contents with the following:

```
   {
       "projects": [{\
           "name":         "CrusaderKingsIII",\
           "path":         "C:/Program Files (x86)/Steam/steamapps/common/Crusader Kings III/game/tools/",\
           "export_path":  "C:/Program Files (x86)/Steam/steamapps/common/Crusader Kings III/game/",\
           "target_exe":   "C:/Program Files (x86)/Steam/steamapps/common/Crusader Kings III/binaries/ck3.exe"\
       }],

       "mergetool": "C:/Program Files (x86)/Meld/Meld.exe $1 $2"
   }
```

Make sure it actually pointing to the correct directory where your game has installed.

When you make any changes, run it through a [JSON Validator](https://jsonlint.com/) to catch any errors early.

### Photoshop Setup\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Exporters&veaction=edit&section=3 "Edit section: Photoshop Setup") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Exporters&action=edit&section=3 "Edit section: Photoshop Setup")\]

TextureExporter 2.0 should now appear in Photoshop > File > Scripts > TextureExporter 2.0

Assign a hotkey to this as you might end up using it a lot – PDS artists use F7.

In the Exporter, click the 'Texture' Asset Type radio button, and then press Generate Missing Layers.

The layer groups will generate before your eyes. You can place any texture you need within these Layer Groups.

When you are ready to export, hit Export. All the layers will be packed into DDS files and sent into the game.

### Maya Setup\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Exporters&veaction=edit&section=4 "Edit section: Maya Setup") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Exporters&action=edit&section=4 "Edit section: Maya Setup")\]

First download and install [Meld](https://meldmerge.org/) as it will make re-exporting a little more painless.

After starting Maya, you go into Plug-in Manager, and activate pdx\_exporter.mll

To open the exporter, run the following MEL script:

```
   rehash; source pdx_export_ui.mel;
   showPdxExport;
```

You can add this to your shelf using the following process:

[Maya - Make a shelf button for a script](https://knowledge.autodesk.com/support/maya/learn-explore/caas/CloudHelp/cloudhelp/2016/ENU/Maya/files/GUID-527023AE-9FB5-4D01-8D29-075B1E6C4754-htm.html)

If the window opens and you see the list of shaders in the Output window, then you are good to go!

## Forum\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Exporters&veaction=edit&section=5 "Edit section: Forum") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Exporters&action=edit&section=5 "Edit section: Forum")\]

Join the discussion on the [Clausewitz Maya Exporter (modding tool)](https://forum.paradoxplaza.com/forum/forums/clausewitz-maya-exporter-modding-tool.935/) subforum!

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
| Graphics | [3D models](https://ck3.paradoxwikis.com/3D_models "3D models") • Exporters • [Coat of arms](https://ck3.paradoxwikis.com/Coat_of_arms_modding "Coat of arms modding") • [Graphical assets](https://ck3.paradoxwikis.com/Graphical_assets "Graphical assets") • [Fonts](https://ck3.paradoxwikis.com/Fonts "Fonts") • [Particles](https://ck3.paradoxwikis.com/index.php?title=Particles&action=edit&redlink=1 "Particles (page does not exist)") • [Shaders](https://ck3.paradoxwikis.com/index.php?title=Shaders&action=edit&redlink=1 "Shaders (page does not exist)") • [Unit models](https://ck3.paradoxwikis.com/index.php?title=Unit_models&action=edit&redlink=1 "Unit models (page does not exist)") |

|     |     |
| --- | --- |
| Audio | [Music](https://ck3.paradoxwikis.com/Music_modding "Music modding") • [Sound](https://ck3.paradoxwikis.com/Sound_modding "Sound modding") |

|     |     |
| --- | --- |
| Other | [Console commands](https://ck3.paradoxwikis.com/Console_commands "Console commands") • [Checksum](https://ck3.paradoxwikis.com/Checksum "Checksum") • [Mod structure](https://ck3.paradoxwikis.com/Mod_structure "Mod structure") • [Mod compatibility](https://ck3.paradoxwikis.com/Mod_compatibility "Mod compatibility") • [Modding tools](https://ck3.paradoxwikis.com/Modding_tools "Modding tools") • [Troubleshooting](https://ck3.paradoxwikis.com/Mod_troubleshooting "Mod troubleshooting") |

Retrieved from " [https://ck3.paradoxwikis.com/index.php?title=Exporters&oldid=8918](https://ck3.paradoxwikis.com/index.php?title=Exporters&oldid=8918)"

[Categories](https://ck3.paradoxwikis.com/Special:Categories "Special:Categories"):

- [Timeless](https://ck3.paradoxwikis.com/Category:Timeless "Category:Timeless")
- [Modding](https://ck3.paradoxwikis.com/Category:Modding "Category:Modding")