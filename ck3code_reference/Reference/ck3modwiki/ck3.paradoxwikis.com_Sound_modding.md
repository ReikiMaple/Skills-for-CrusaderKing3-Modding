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

# Sound modding

From CK3 Wiki

[Jump to navigation](https://ck3.paradoxwikis.com/Sound_modding#mw-head) [Jump to search](https://ck3.paradoxwikis.com/Sound_modding#searchInput)

Required free tool: [FMOD Studio 1.10.20](https://www.fmod.com/download#fmodstudio)

We recommend this version, as newer ones can cause crashes in CK3 1.16.

On the website, select FMOD Studio, Older, in the dropdown find 1.10.20. It's "unsupported" but it works for us.

What is FMOD?

FMOD lets us mix multiple sounds into events which are then stored in banks and played by the game.

Use [FMOD Bank Tools](https://www.nexusmods.com/rugbyleaguelive3/mods/2?tab=files) to extract wav files from the game's banks. (download requires a Nexus account)

While music can be added directly as wav files, sounds cannot, we have to import them throgh FMOD banks.

We also cannot reload audio files while the game is running, we have to restart.

## Contents

- [1Import sounds](https://ck3.paradoxwikis.com/Sound_modding#Import_sounds)
  - [1.1With a template](https://ck3.paradoxwikis.com/Sound_modding#With_a_template)
  - [1.2Bank name and crashing](https://ck3.paradoxwikis.com/Sound_modding#Bank_name_and_crashing)
  - [1.3Create from scratch](https://ck3.paradoxwikis.com/Sound_modding#Create_from_scratch)
- [2Playing sounds in the game](https://ck3.paradoxwikis.com/Sound_modding#Playing_sounds_in_the_game)
- [3Troubleshooting](https://ck3.paradoxwikis.com/Sound_modding#Troubleshooting)
- [4Random sounds](https://ck3.paradoxwikis.com/Sound_modding#Random_sounds)
- [5Overlapping sounds](https://ck3.paradoxwikis.com/Sound_modding#Overlapping_sounds)
- [63D sound](https://ck3.paradoxwikis.com/Sound_modding#3D_sound)
- [7Sound Parameters](https://ck3.paradoxwikis.com/Sound_modding#Sound_Parameters)
  - [7.1Adding Sound Parameters to Events in FMOD](https://ck3.paradoxwikis.com/Sound_modding#Adding_Sound_Parameters_to_Events_in_FMOD)
  - [7.2Using the Sound Parameters in In-Game GUI](https://ck3.paradoxwikis.com/Sound_modding#Using_the_Sound_Parameters_in_In-Game_GUI)
- [8Best Practice](https://ck3.paradoxwikis.com/Sound_modding#Best_Practice)
  - [8.1Organizing your Events in Folders](https://ck3.paradoxwikis.com/Sound_modding#Organizing_your_Events_in_Folders)

## Import sounds\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Sound_modding&veaction=edit&section=1 "Edit section: Import sounds") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Sound_modding&action=edit&section=1 "Edit section: Import sounds")\]

We have an FMOD template where everything is set up for you. This is the easiest way to do this.

[![screenshot of FMOD, creating an event with Windows XP error sound](https://ck3.paradoxwikis.com/images/thumb/a/a7/FMOD_creating_an_event.png/147px-FMOD_creating_an_event.png)](https://ck3.paradoxwikis.com/File:FMOD_creating_an_event.png)

[Enlarge](https://ck3.paradoxwikis.com/File:FMOD_creating_an_event.png "Enlarge")

Creating an event

[![Screenshot of FMOD, assigning a new Windows XP error event to a Master bank](https://ck3.paradoxwikis.com/images/thumb/2/2c/FMOD_assigning_an_event.png/250px-FMOD_assigning_an_event.png)](https://ck3.paradoxwikis.com/File:FMOD_assigning_an_event.png)

[Enlarge](https://ck3.paradoxwikis.com/File:FMOD_assigning_an_event.png "Enlarge")

Assign an Event to a Bank

[![Screenshot of FMOD, a Windows XP bank with Windows XP error event](https://ck3.paradoxwikis.com/images/thumb/4/43/FMOD_bank.png/250px-FMOD_bank.png)](https://ck3.paradoxwikis.com/File:FMOD_bank.png)

[Enlarge](https://ck3.paradoxwikis.com/File:FMOD_bank.png "Enlarge")

Bank with our event

[![Screenshot of a mod with new sound files, with two banks inside sound/banks folder](https://ck3.paradoxwikis.com/images/thumb/1/1a/Sound_mod_files.png/250px-Sound_mod_files.png)](https://ck3.paradoxwikis.com/File:Sound_mod_files.png)

[Enlarge](https://ck3.paradoxwikis.com/File:Sound_mod_files.png "Enlarge")

Mod file structure

### With a template\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Sound_modding&veaction=edit&section=2 "Edit section: With a template") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Sound_modding&action=edit&section=2 "Edit section: With a template")\]

01. Download this [FMOD project template](https://github.com/Agamidae/1.10-FMOD-CK3-template) from Github.
02. Unzip it, open '1.10 fmod ck3 template.fspro'.
    - If FMOD asks to recover the file, agree. Re-save it as your own project, so you can always reuse the template.
03. Add your sounds to the Assets tab.
    - It accepts wav, mp3, ogg, aiff, wma and flac.
04. Right-click them and create events (any type, pick 2D if unsure).
    - You can rename events by double-clicking and change their volume at the bottom of the screen.
05. Go to Events tab, right-click your events and assign them to the Bank bank.
06. Go to Banks tab and rename the bank to something unique to avoid conflicts with other mods or game files.
    - IMPORTANT! The name of your bank should precede "Master Bank". Try A-L range. See below for details.
07. Go to Window > Mixer Routing (Ctrl+5).
08. Right-click your events and assign them to appropriate VCAs, these are game's volume controls. Without it, our sounds would blast players at full volume.
09. Save and build the project from File > Build (F7). It will create bank files in the project's `Build/banks` folder.
10. Copy the banks to your mod's `/sound/banks` folder. You'll have two files, copy both.

    - Check for typos! That's singular `sound` and plural `banks`.
11. For the future, you can tell FMOD to build right to the mod folder, in Edit -> Preferences -> Build.
    - if you change the name of your bank, you'll need to remove the old bank files manually
12. Launch the game with your mod and test with console command `Audio.PlayEvent event:/myevent`
    - Note, the console can't play events with spaces in them. This is not an issue for script and UI.
    - If you put your events into folders in FMOD, then this path would include folder names, eg: `event:/somefolder/myevent`
    - You do not need to reference the name of the bank here.

### Bank name and crashing\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Sound_modding&veaction=edit&section=3 "Edit section: Bank name and crashing") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Sound_modding&action=edit&section=3 "Edit section: Bank name and crashing")\]

The bank name can cause the game to crash on exit.

We don't know why or the exact way to avoid it.

Try using names that come before "Master Bank" alphabetically to reduce the risk of the crash.

This is the name of the master bank used by the game and something about the load order causes issues.

From tests, these names would crash on exit:

❌ Mazter, New, template

These names work:

✔️ Key, List, Ma

There are more oddities:

'Ar' and 'ar' work, while 'aR' crashes. 'Army fix' works, but 'army\_fix' crashes.

Try avoiding underscores and capital letters after the first one. More testing is welcome.

This crash doesn't doesn't happen during gameplay, only after a player clicks Exit to Desktop.

So it's not critical, but it's still better to avoid it, so it doesn't open the crash reporter and doesn't create log files, which can quickly eat up space on the drive.

### Create from scratch\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Sound_modding&veaction=edit&section=4 "Edit section: Create from scratch") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Sound_modding&action=edit&section=4 "Edit section: Create from scratch")\]

To do this on your own, you'll need to create VCAs and replace all the GUIDs of your project with the ones from the game.

01. Create your project and add new events, following the steps from above.
02. Go to Window > Mixer Routing, VCAs tab. Create a new VCA and name it one of these names, depending on what your sounds are:
    - Ambience, Music, Sound Effects, UI
03. In the Routing tab, expand the Master Bus and assign your sounds to the VCA. This will allow players to adjust their volume.
    - Note, you may need to assign one event to multiple VCAs. UI sounds are also affected by Sound Effects volume, for example.
04. Save your project (don't put it in the mod folder yet).
05. Go to File > Export GUIDs. This will create a text file in your project's Build/ folder.
06. Go to that folder and open GUIDs.txt.
07. Find the line ending with `bus:/` and another with the name of your VCA and copy the ids to another file somewhere. They might look like this:

    - `{767eec3a-3ca8-4ae8-8827-376bf7db4d8f} bus:/`
    - `{72d40a2a-0111-4078-8ba7-e84d415b91a2} vca:/UI`
08. In CK3 folder, open game/sound/GUIDs.txt and find its `bus:/` and vca lines, copy their ids as well. The VCAs are at the bottom. E.g.:

    - `{cb930c67-0464-4d7f-957a-a78b08fc39de} bus:/`
    - `{f8bd5083-a8cc-412b-ada4-cdc08a33ce75} vca:/UI`
09. In your FMOD project folder, search through all the files in the Metadata folder and replace your ids, inside {}, with the ones from the game, for both the bus and vca.
    - In this example, for the bus, we're replacing `767...` with `cb9...`You will likely see at least 4 results.
    - If you don't have a proper text editor, install [VSC](https://code.visualstudio.com/). Drop the Metadata folder into it, right-click > Find in Folder.
10. Go back to FMOD and restart it, reopen your project.
11. Select File > Build. This will create our bank files that will be used by the game.
12. Copy all the bank files created and put them into your mod, in sound/banks folder.

## Playing sounds in the game\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Sound_modding&veaction=edit&section=5 "Edit section: Playing sounds in the game") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Sound_modding&action=edit&section=5 "Edit section: Playing sounds in the game")\]

Sound events can be played from script, UI or from models on the map.

**Script:**

`play_sound_effect = "event:/myevent"`

**UI buttons:**

`clicksound = "event:/myevent"`

`oversound = "event:/myevent"` \- this plays when the cursor hovers over a button

**UI animation states:**

```
state = {
  name = "my_sound"
  start_sound = { soundeffect = "event:/myevent" }
  end_sound = { soundeffect = "event:/myevent" }
  soundparam = { name = parameterName value = 1 }
}
```

end\_sound will play at the end of the animation if it has duration. Otherwise, you can simply use start\_sound to trigger it immediately.

soundparam is optional, used to modify the event using a parameter set in FMOD. See [Sound Parameters](https://ck3.paradoxwikis.com/Sound_modding#Sound_Parameters "Sound modding") below.

Remember that states don't fire by themselves, see [Interface/Animation states](https://ck3.paradoxwikis.com/Interface#Animation_states "Interface")

You can also use a scripted gui that plays the sound in script and fire it from a button's onclick or a state's on\_finish.

**3D models:**

Buildings (common/buildings)

```
asset = {
  ...
  soundeffect = { soundeffect = "event:/eventName" soundparameter = { "parameterName" = 0 } }
}
```

Units (gfx/models/units/infantry)

```
state = {
  ...
  event = {
    time = 0.0
    soundparameter = { "parameterName" = 0.0 }
    sound = { soundeffect = "event:/eventName" }
  }
}
```

## Troubleshooting\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Sound_modding&veaction=edit&section=6 "Edit section: Troubleshooting") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Sound_modding&action=edit&section=6 "Edit section: Troubleshooting")\]

If the error log says it couldn't load a bank, you probably didn't replace the ids correctly or didn't reopen the project afterward.

If it can't find a specific event, double-check the path, the name and that it's assigned to a bank in FMOD.

## Random sounds\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Sound_modding&veaction=edit&section=7 "Edit section: Random sounds") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Sound_modding&action=edit&section=7 "Edit section: Random sounds")\]

You can easily create randomized sounds in FMOD with multi instrument.

Select multiple audio files, right-click > Create Events > Create a new event with one multi instrument.

Select your new event from the Events tab and select the track in the middle of the screen.

At the bottom, under Playlist, there is a dropdown menu, with Shuffle. You can select other modes, to use pure random chance or to play them one by one with Sequential - Global Scope.

Press play to test it, it will pick a new track every time.

This if, for example, how [CK2 Selection Music](https://steamcommunity.com/sharedfiles/filedetails/?id=3391666885) mod works.

## Overlapping sounds\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Sound_modding&veaction=edit&section=8 "Edit section: Overlapping sounds") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Sound_modding&action=edit&section=8 "Edit section: Overlapping sounds")\]

By default, if you play your sound repeatedly, the sounds will overlap and could cause too much noise.

To avoid it, select your event, at the bottom right there is a parameter Max Instances. It's set to infinite by default.

Hold and drag it or press the little triangle to enter 1. (or another number if you want a few instances to play at the same time)

Below it, Stealing option will determine the behavior. "Oldest" will interrupt the previous sounds, while "None" will prevent any new sounds until the first one finished playing. It seems that CK3 uses "None" for things like notifications and army orders.

## 3D sound\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Sound_modding&veaction=edit&section=9 "Edit section: 3D sound") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Sound_modding&action=edit&section=9 "Edit section: 3D sound")\]

[![](https://ck3.paradoxwikis.com/images/thumb/e/eb/FMOD_Distance_Automation.png/300px-FMOD_Distance_Automation.png)](https://ck3.paradoxwikis.com/File:FMOD_Distance_Automation.png)

[Enlarge](https://ck3.paradoxwikis.com/File:FMOD_Distance_Automation.png "Enlarge")

Distance is a built-in parameter in FMOD that can be used to automate sound effects. (EQ, Volume, Reverb, Delay, etc.)

If you're adding sounds to be played on the map, create an event with 3D Action or 3D Timeline type. They allow for distance falloff.

At the bottom right there is a parameter Min & Max Distance. The default distance is fairly small, the sound emitter will only play when it's pretty much in the center of the screen.

In the game, use console command Audio.Debug to see the sizes of sound emitters. They are fairly small, so you may choose to keep yours the same size for consistency.

To automate effects (in this case a Multiband EQ) based on the distance parameter in FMOD do the following in an Event:

1. Add Parameter Sheet by clicking the + view next to Timeline and clicking 'Add Parameter Sheet' > 'New Parameter'.
2. Select 'Built-in: Distance'.
3. Add a Multiband EQ on the instrument.
4. Right click Freq. (A) and modulate it with distance.
5. Draw your curve and test it out live by changing the distance parameter.

## Sound Parameters\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Sound_modding&veaction=edit&section=10 "Edit section: Sound Parameters") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Sound_modding&action=edit&section=10 "Edit section: Sound Parameters")\]

[![](https://ck3.paradoxwikis.com/images/thumb/3/3f/Sound_Parameter.png/300px-Sound_Parameter.png)](https://ck3.paradoxwikis.com/File:Sound_Parameter.png)

[Enlarge](https://ck3.paradoxwikis.com/File:Sound_Parameter.png "Enlarge")

The 'Add Parameter' window in FMOD.

Sound Parameters can be used in script to modify the sound effect. For example, the soundparam CharacterStressLevel is used to intensify the stress outbreaks in-game at higher levels of stress.

_NOTE: Sound Parameters cannot be used in regular script like:_`play_sound_effect = "event:/myevent"`

### Adding Sound Parameters to Events in FMOD\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Sound_modding&veaction=edit&section=11 "Edit section: Adding Sound Parameters to Events in FMOD") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Sound_modding&action=edit&section=11 "Edit section: Adding Sound Parameters to Events in FMOD")\]

To add parameters to an event in FMOD do the following:

1. Select the Event that needs the parameter and enter the Event Editor.
2. Press the '+' next to 'Action' or 'Timeline' then press 'Add Parameter Sheet' then 'New Parameter'.
3. Name your parameter. Use 'User: Discrete' Parameter type, if you want the values in integers otherwise use 'User: Continuous'. Press OK.
4. The parameter can now be used to automate Volume, Effects, etc.
5. Right-click the desired value(s) (Volume, panning, reverb length, etc.) and press 'Add Automation'.
6. Press on 'Add Curve' then 'Browse > ParameterName'.
7. Draw a curve by double-clicking in the graph to make points.
8. The sound can be tested live by changing the parameter in the 'Parameters' pane on the right.

### Using the Sound Parameters in In-Game GUI\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Sound_modding&veaction=edit&section=12 "Edit section: Using the Sound Parameters in In-Game GUI") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Sound_modding&action=edit&section=12 "Edit section: Using the Sound Parameters in In-Game GUI")\]

In GUI you can reference the parameter and use a value to modify the sound effect like this:

```
start_sound = {
    soundeffect = "event:/test_sound"
    soundparam = { name = ParameterName value = 1.5 }
}
```

## Best Practice\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Sound_modding&veaction=edit&section=13 "Edit section: Best Practice") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Sound_modding&action=edit&section=13 "Edit section: Best Practice")\]

[![](https://ck3.paradoxwikis.com/images/thumb/4/46/Event_Folders.png/300px-Event_Folders.png)](https://ck3.paradoxwikis.com/File:Event_Folders.png)

[Enlarge](https://ck3.paradoxwikis.com/File:Event_Folders.png "Enlarge")

Right-click and press 'New Folder' to organize your events.

### Organizing your Events in Folders\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Sound_modding&veaction=edit&section=14 "Edit section: Organizing your Events in Folders") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Sound_modding&action=edit&section=14 "Edit section: Organizing your Events in Folders")\]

Putting all your Events in the root is urorganized, so a folder structure is recommended for bigger mods and mod compatibility.

To make folders simply right-click in the 'Events' tab and press 'New Folder'.

Events can now be referenced like the following:

```
event:/YourModName/SFX/TestSound1
event:/YourModName/SFX/TestSound2
event:/YourModName/Ambiance/Ambiance1
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
| Audio | [Music](https://ck3.paradoxwikis.com/Music_modding "Music modding") • Sound |

|     |     |
| --- | --- |
| Other | [Console commands](https://ck3.paradoxwikis.com/Console_commands "Console commands") • [Checksum](https://ck3.paradoxwikis.com/Checksum "Checksum") • [Mod structure](https://ck3.paradoxwikis.com/Mod_structure "Mod structure") • [Mod compatibility](https://ck3.paradoxwikis.com/Mod_compatibility "Mod compatibility") • [Modding tools](https://ck3.paradoxwikis.com/Modding_tools "Modding tools") • [Troubleshooting](https://ck3.paradoxwikis.com/Mod_troubleshooting "Mod troubleshooting") |

Retrieved from " [https://ck3.paradoxwikis.com/index.php?title=Sound\_modding&oldid=29990](https://ck3.paradoxwikis.com/index.php?title=Sound_modding&oldid=29990)"

[Categories](https://ck3.paradoxwikis.com/Special:Categories "Special:Categories"):

- [Pages with syntax highlighting errors](https://ck3.paradoxwikis.com/index.php?title=Category:Pages_with_syntax_highlighting_errors&action=edit&redlink=1 "Category:Pages with syntax highlighting errors (page does not exist)")
- [Modding](https://ck3.paradoxwikis.com/Category:Modding "Category:Modding")