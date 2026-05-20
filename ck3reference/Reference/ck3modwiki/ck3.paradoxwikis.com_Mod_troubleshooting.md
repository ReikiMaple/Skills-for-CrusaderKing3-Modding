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

# Mod troubleshooting

From CK3 Wiki

[Jump to navigation](https://ck3.paradoxwikis.com/Mod_troubleshooting#mw-head) [Jump to search](https://ck3.paradoxwikis.com/Mod_troubleshooting#searchInput)

## Contents

- [1Basics of the Developer Console & Enabling Debugging](https://ck3.paradoxwikis.com/Mod_troubleshooting#Basics_of_the_Developer_Console_&_Enabling_Debugging)
  - [1.1Getting Access to the Debug Tools](https://ck3.paradoxwikis.com/Mod_troubleshooting#Getting_Access_to_the_Debug_Tools)
  - [1.2The Basics of the Developer Console](https://ck3.paradoxwikis.com/Mod_troubleshooting#The_Basics_of_the_Developer_Console)
- [2The Art of Debugging](https://ck3.paradoxwikis.com/Mod_troubleshooting#The_Art_of_Debugging)
  - [2.1Localization Debugging](https://ck3.paradoxwikis.com/Mod_troubleshooting#Localization_Debugging)
  - [2.2Error Spam: Debugging Dynamic Loc and Trigger Conditions](https://ck3.paradoxwikis.com/Mod_troubleshooting#Error_Spam:_Debugging_Dynamic_Loc_and_Trigger_Conditions)
  - [2.3Scope Debugging](https://ck3.paradoxwikis.com/Mod_troubleshooting#Scope_Debugging)
  - [2.4Hot-loading](https://ck3.paradoxwikis.com/Mod_troubleshooting#Hot-loading)
- [3Automating the Debug Process Through Run Scripts](https://ck3.paradoxwikis.com/Mod_troubleshooting#Automating_the_Debug_Process_Through_Run_Scripts)

## Basics of the Developer Console & Enabling Debugging\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Mod_troubleshooting&veaction=edit&section=1 "Edit section: Basics of the Developer Console & Enabling Debugging") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Mod_troubleshooting&action=edit&section=1 "Edit section: Basics of the Developer Console & Enabling Debugging")\]

[![This is Errorhoof, he is here to tell you that your scripts are broken.](https://ck3.paradoxwikis.com/images/b/b1/Errorhoof.jpg)](https://ck3.paradoxwikis.com/File:Errorhoof.jpg "This is Errorhoof, he is here to tell you that your scripts are broken.")

Debugging is easy! [\[Citation Needed](https://en.wikipedia.org/wiki/Wikipedia:Citation_needed)\] This page will help you understand how to debug and fix issues with your script.

[![](https://ck3.paradoxwikis.com/images/thumb/3/3a/Ck3_debug_shortcut_example.jpg/335px-Ck3_debug_shortcut_example.jpg)](https://ck3.paradoxwikis.com/File:Ck3_debug_shortcut_example.jpg)

[Enlarge](https://ck3.paradoxwikis.com/File:Ck3_debug_shortcut_example.jpg "Enlarge")

A screenshot of a shortcut created from the CK3 steam build binary.

Note: if you are using the Steam version of the game, you can right click on the title in your library, click "properties" and add `-debug_mode startup` to your launch options.

### Getting Access to the Debug Tools\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Mod_troubleshooting&veaction=edit&section=2 "Edit section: Getting Access to the Debug Tools") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Mod_troubleshooting&action=edit&section=2 "Edit section: Getting Access to the Debug Tools")\]

The first thing you want to do is enable debug on your game, to do this you must find your game's .exe file (eg: `C:\Program Files (x86)\Steam\steamapps\common\Crusader Kings III\binaries`) and create a shortcut with the `-debug_mode` parameter at the end. View the image on the right for an example. Once this has been done, you will be able to access the developer console in-game via the ````` key; Known as the ["grave accent"](https://en.wikipedia.org/wiki/Grave_accent) key, which is usually located at the top left of a keyboard. This will also allow you to get messages from Errorhoof warning you of any script errors: the game will automatically open a notepad window with a list of any errors at it finds startup, but clicking error hoof will allow you to create a new notepad window with all the latest and greatest of your mistakes.

### The Basics of the Developer Console\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Mod_troubleshooting&veaction=edit&section=3 "Edit section: The Basics of the Developer Console") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Mod_troubleshooting&action=edit&section=3 "Edit section: The Basics of the Developer Console")\]

Below is an image explaining what each button in the debug UI does:

[![Layout of Debugger](https://ck3.paradoxwikis.com/images/thumb/0/07/Debugger_ui_2021.jpeg/696px-Debugger_ui_2021.jpeg)](https://ck3.paradoxwikis.com/File:Debugger_ui_2021.jpeg "Layout of Debugger")

To test your event, simply type `event name.id` into the command input window and press enter (examples: `event diplomacy_foreign.1074` and `event central_asia.0011`).

This is the primary way of testing events that have not yet been added to a pulse or otherwise connected to the game in any way a player could naturally encounter. You can also use that same window to execute effects such as `add_gold = 999999` and `add_trait = lunatic_genetic` to help meet the conditions necessary to properly run the event you are testing.

## The Art of Debugging\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Mod_troubleshooting&veaction=edit&section=4 "Edit section: The Art of Debugging") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Mod_troubleshooting&action=edit&section=4 "Edit section: The Art of Debugging")\]

Confused by an error? _Great!_ The first step is to _remain calm_ and read the error again while taking the text as literally as possible. If an error says it does not recognize a loc key, then it probably means exactly that.

Below is some general advice that will help solve your issue 80% of the time, for the remaining 20%, reach out to other members of the CK3 modding community. Modders are (mostly) friendly folk ready to lend a hand to beginners and they are sure to answer your many questions.

Note: Newer error logs are at the top, while older logs will be at the bottom. Be sure to clear your console to remove old errors.

### Localization Debugging\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Mod_troubleshooting&veaction=edit&section=5 "Edit section: Localization Debugging") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Mod_troubleshooting&action=edit&section=5 "Edit section: Localization Debugging")\]

Localization has improved a lot since the epoch of Crusader Kings 2 and it is now easier than ever, but that does not mean it is fool-proof.

The first thing you must make sure of is that your loc file is encoded correctly (the game will tell you if it is not), you should use `utf8bom`. Here is how you save your loc file with the correct encoding:

- **Sublime Text**: File → "Save With Encoding..." → "UTF8 with BOM"
- **Visual Studio Code**: At the bottom of the window (bottom-most right) is the encoding and syntax highlight tab, select UTF8 (or whatever else it is set to) → "Save with Encoding" → "UTF8 with BOM"
- **Notepad++**: Encoding → "UTF8 with BOM"

You may also encounter issues with missing keys, unrecognized keys or duplicate hashes:

- **Missing Key**: You probably misspelled the loc key or forgot to save (it happens to the best of us), make sure to save, double-check and re-type your loc key.
- **Unrecognized Key**: Same solution as above, but this also happens when you use a string in your script (using "my text here" instead of a loc key). To solve the issue simply make a key with the contents of your string.
- **Duplicate Key or Hash**: Somewhere either in or outside your file there is a key with the same name or content as another key. Search and destroy/replace.

### Error Spam: Debugging Dynamic Loc and Trigger Conditions\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Mod_troubleshooting&veaction=edit&section=6 "Edit section: Error Spam: Debugging Dynamic Loc and Trigger Conditions") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Mod_troubleshooting&action=edit&section=6 "Edit section: Error Spam: Debugging Dynamic Loc and Trigger Conditions")\]

Are you getting thousands of errors every second you run your event? _Don't panic!_

The first thing you want to do is check your dynamic loc, make sure you did not make a mistake when writing it. Here are some common mistakes:

- Writing `[ROOT.GetSomething]` when you meant to do `[ROOT.Char.GetSomething]`
- Misspelled a name, it happens. A lot.
- Used `[scope:mysavedscopecharacter.GetFirstName]` instead of `[mysavedscopecharacter.GetFirstName]`, saved scopes do not need `scope:` when using them in dynamic loc.
- You did not actually save the character you referenced in the scope of the dynamic loc.
- The name of the scoped character was changed in the script and you forgot to update it in the loc.

If you did everything correctly but are still getting issues with dynamic loc, then that must be that **you did not meet the conditions for the event fired.**

When launching an event via the debug console, the event itself will trigger even if you do not meet all of the specified conditions. This means that it might have failed to save a character that could not be scoped into because the trigger failed.

To find out whether or not you meet the conditions of the event fired via the debug console, hover over the ✔ or ✖ icon at the top right of your event window. This will show you a detailed view of the conditions of your event and whether or not they were met.

[![An image depicting a brave content designer investigating why the console is generating 8 gigabytes of debug log spam.](https://ck3.paradoxwikis.com/images/thumb/e/e3/Event_conditions_debug.jpg/1038px-Event_conditions_debug.jpg)](https://ck3.paradoxwikis.com/File:Event_conditions_debug.jpg "An image depicting a brave content designer investigating why the console is generating 8 gigabytes of debug log spam.")

### Scope Debugging\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Mod_troubleshooting&veaction=edit&section=7 "Edit section: Scope Debugging") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Mod_troubleshooting&action=edit&section=7 "Edit section: Scope Debugging")\]

It is possible to generate a folder containing every trigger, effect, modifier and runtime log that is recognized by code by typing `script_docs` into the developer console. The resulting files will then be dumped at `C:\Users\YOURUSERNAME\Documents\Paradox Interactive\Crusader Kings III\logs` and can be read using notepad or an IDE of choice.

These `.log` can be opened with notepad and are very useful for debugging a variety of issues, as well as
Here is an overview of the most useful files and their contents:

| File | Description |
| --- | --- |
| Effects.log | Contains a list of all non-scripted (hardcoded) effects, how they should be used and what their potential [arguments](https://en.wikipedia.org/wiki/Parameter_(computer_programming)) are. |
| Triggers.log | Contains a list of every non-scripted trigger found in the game and what scopes and targets they support. |
| Modifiers.log | List of every modifier that can be used in scripted modifiers and lists what types they can be used in. |
| event\_scopes.log | Every valid scope type. Keep in mind that you should not directly reference a type. |
| event\_targets.log | Every possible event target as recognized by the script. Very useful for crawling up or down from one scope to another via [parent-child relations](https://en.wikipedia.org/wiki/Inheritance_(object-oriented_programming)). |

### Hot-loading\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Mod_troubleshooting&veaction=edit&section=8 "Edit section: Hot-loading") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Mod_troubleshooting&action=edit&section=8 "Edit section: Hot-loading")\]

Hot-loading, in the context of CK3, is the act of updating scripts _while the game is still running_.

This means you can test minor changes in your script and debug it in real-time without the need to restart the game each time.

However, one should be careful with hot-loading, as making sizable changes can lead to the game behaving unexpectedly. If you make a large set changes (or one that interacts with elements outside of the updated script), it is adviced that you re-start the game to avoid spending hours debugging an error that only exists because the changes were hot-loaded improperly.

**Tips For Hot-loading Safety:**

1. If possible, have the event closed when you hot-load a change.
2. Otherwise, you can press the \[⟳\] icon on the event debug options. Be warned that this will not update saved scopes.
3. Localization can be updated at any time. But new localization keys will usually not hot-load.
4. Use hot-loading to debug and tweak, not to test if the script has any start-up errors.

## Automating the Debug Process Through Run Scripts\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Mod_troubleshooting&veaction=edit&section=9 "Edit section: Automating the Debug Process Through Run Scripts") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Mod_troubleshooting&action=edit&section=9 "Edit section: Automating the Debug Process Through Run Scripts")\]

When testing more complex features and/or content, a great deal of time can be saved by automating the repetitive actions needed to meet the conditions necessary to access the target feature/content. Run Scripts execute effects in the same way as an events `immediate` block would, meaning that it can be used to store a large chain of effects meant to skip over the aforementioned repetitive manual work.

From a technical perspective, Run Scripts are `.txt` files stored in `..\Documents\Paradox Interactive\Crusader Kings III\run` which immediately execute any effects scripted inside them when fired through the following console command: `run run_script_name_here.txt`

Here is an example of what the contents of a run script look like:

```
# Run Script to set up the conditions for restoring the HRE. Recommended to start as King Luis (867).
title:c_cologne = { add_to_list = target_titles }
title:c_mainz = { add_to_list = target_titles }
title:c_trier = { add_to_list = target_titles }
title:d_bohemia = { add_to_list = target_titles }
title:d_east_franconia = { add_to_list = target_titles }
title:d_ostfalen = { add_to_list = target_titles }
title:d_ostmark = { add_to_list = target_titles }
title:k_lotharingia = { add_to_list = target_titles }
title:k_italy = { add_to_list = target_titles }
title:k_east_francia = { add_to_list = target_titles }

create_title_and_vassal_change = {
	type = conquest
	save_scope_as = change
}

every_in_list = {
	list = target_titles
	limit = { NOT = { holder = root } }
	every_in_de_jure_hierarchy =  {
		change_title_holder = {
			holder = root
			change = scope:change
		}
	}
}
resolve_title_and_vassal_change = scope:change

add_hook = {
	target = faith.religious_head
	type = strong_test_hook
}

root = {
	add_prestige = 4000
	add_gold = 500
	add_piety = 200
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
| Other | [Console commands](https://ck3.paradoxwikis.com/Console_commands "Console commands") • [Checksum](https://ck3.paradoxwikis.com/Checksum "Checksum") • [Mod structure](https://ck3.paradoxwikis.com/Mod_structure "Mod structure") • [Mod compatibility](https://ck3.paradoxwikis.com/Mod_compatibility "Mod compatibility") • [Modding tools](https://ck3.paradoxwikis.com/Modding_tools "Modding tools") • Troubleshooting |

Retrieved from " [https://ck3.paradoxwikis.com/index.php?title=Mod\_troubleshooting&oldid=31655](https://ck3.paradoxwikis.com/index.php?title=Mod_troubleshooting&oldid=31655)"

[Categories](https://ck3.paradoxwikis.com/Special:Categories "Special:Categories"):

- [Pages using deprecated enclose attributes](https://ck3.paradoxwikis.com/index.php?title=Category:Pages_using_deprecated_enclose_attributes&action=edit&redlink=1 "Category:Pages using deprecated enclose attributes (page does not exist)")
- [Modding](https://ck3.paradoxwikis.com/Category:Modding "Category:Modding")