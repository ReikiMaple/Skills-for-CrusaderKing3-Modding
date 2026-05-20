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

# Mod compatibility

From CK3 Wiki

[Jump to navigation](https://ck3.paradoxwikis.com/Mod_compatibility#mw-head) [Jump to search](https://ck3.paradoxwikis.com/Mod_compatibility#searchInput)

Mod compatibility is the measure of how well different mods work together. Maximising compatibility is done with simple practices that should be followed whenever possible, advanced techniques where necessary, and finally a compatibility patch where there's no other solution.

## Contents

- [1General practices](https://ck3.paradoxwikis.com/Mod_compatibility#General_practices)
  - [1.1Total conversions](https://ck3.paradoxwikis.com/Mod_compatibility#Total_conversions)
- [2Basic techniques](https://ck3.paradoxwikis.com/Mod_compatibility#Basic_techniques)
  - [2.1Shared variable](https://ck3.paradoxwikis.com/Mod_compatibility#Shared_variable)
  - [2.2Shared scripted effect](https://ck3.paradoxwikis.com/Mod_compatibility#Shared_scripted_effect)
- [3Detecting other mods](https://ck3.paradoxwikis.com/Mod_compatibility#Detecting_other_mods)
  - [3.1Global variable](https://ck3.paradoxwikis.com/Mod_compatibility#Global_variable)
  - [3.2Scripted trigger](https://ck3.paradoxwikis.com/Mod_compatibility#Scripted_trigger)

## General practices\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Mod_compatibility&veaction=edit&section=1 "Edit section: General practices") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Mod_compatibility&action=edit&section=1 "Edit section: General practices")\]

Mods may add their own things or alter/replace/remove things that are in vanilla. Any such edit is called an override, as you are replacing the vanilla definition with your own. Files or entities may be overridden (the rules are explained in greater detail [here](https://ck3.paradoxwikis.com/Modding#Override_rules "Modding")). The vanilla files or entities that a mod overrides is collectively called that mod's _footprint_.

In general, mods are compatible if their footprints do not overlap. That is, the two mods do not override the same vanilla files or entities. Certain mods will advertise which files they override on their Steam page; other mod developers can use this to see compatibility at a glance, and mod users use this information too. _CrusaderKhan120's Rally Point Overhaul_ and _DukeOfFluff's Three Hundred Additional Dog Breeds_ are expected to be compatible as they deal with wildly different things, but if either or both are particularly poorly written, they may share an on\_action structure and be incompatible. So when developing your own mod, always minimise your footprint to the smallest it can practically be.

### Total conversions\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Mod_compatibility&veaction=edit&section=2 "Edit section: Total conversions") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Mod_compatibility&action=edit&section=2 "Edit section: Total conversions")\]

Total conversions are the exceptions to this, because they do vanilla _removals_. A mod called _Sedevacantist4Life's Crusading Improvements_ could override no vanilla entities at all, having a footprint of zero, and it would still be incompatible with a _Shrek Total Conversion_, if it references Christian faiths in its own events. That is, it checks whether someone is eligible for a flavour event with a trigger like `faith = faith:catholic`. The Shrek TC has removed Catholicism, and so the crusader mod will check for something that does not exist. That causes errors and erroneous behaviour.

Being TC-compatible is a greater challenge than general compatibility, as it means you must avoid mentioning any database entities in your mod, that is, any references of specific faiths, cultures, characters, titles, and so on. That sacrifices the ability to have any systems or flavour specific to those things, and so it is a perfectly valid choice not to go on that path for your mod.

## Basic techniques\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Mod_compatibility&veaction=edit&section=3 "Edit section: Basic techniques") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Mod_compatibility&action=edit&section=3 "Edit section: Basic techniques")\]

Avoiding footprint overlap is the simplest way to have compatibility, but what if you want two mods to work together, to synergise, but still function independently as well? The two mods can leverage footprint overlaps to make this work.

### Shared variable\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Mod_compatibility&veaction=edit&section=4 "Edit section: Shared variable") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Mod_compatibility&action=edit&section=4 "Edit section: Shared variable")\]

This is a very basic technique for mod interoperability. _Lancel0tXGuin3vere's Extra Romantic Romance Events_ (ERRE) adds extra content to the seduction scheme, and _4everHoldUrPeace's Marriage Vows Expanded_ (MVE) makes weddings more special. If the second mod wants to add marriage vows specific to characters who seduced one another, then it can do so easily by checking for a Character Memory. However, the romance mod may have added different memories, and MVE cannot simply check for those types as they won't exist if ERRE is never loaded. Checking for a non-existent link can, as with the TC case, cause broken behaviour.

The solution is to make the interaction point be something you can check without knowing whether it could exist. That something is a named variable. The ERRE can decide to store a variable on each character, called `var:erre_seduced_each_other`, and it can be given a value of `flag:seduced_in_woods` for more specificity. Then MVE can simply check `has_variable = erre_seduced_each_other` and it will return true if the variable exists (it has been set by ERRE), and false otherwise. This script does not depend on either mod being loaded, but when they are loaded together, they synergise.

### Shared scripted effect\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Mod_compatibility&veaction=edit&section=5 "Edit section: Shared scripted effect") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Mod_compatibility&action=edit&section=5 "Edit section: Shared scripted effect")\]

Let's say ERRE from the previous example wants to add a shotgun wedding as part of seduction, and MVE, which already has a shotgun wedding event of its own, wants that used instead (or a modified version). A shared variable won't do you any good as here timing is important, you want ERRE to fire up MVE content; but still you want ERRE to fire up its own content when MVE is not loaded, and likewise want MVE to not depend on ERRE for its regular wedding content.

The solution is a shared scripted effect, but with special care for file names. ERRE must do the following.

**1\. Extract the firing of the shotgun wedding event to a scripted effect.** That is, in the calling logic, write this:

```
erre_fire_shotgun_wedding_effect = yes
```

And in the effect:

```
erre_fire_shotgun_wedding_effect = {
    trigger_event = erre_shotgun_wedding.1
}
```

This may seem redundant at first, but it is essential to extract this step in the process.

**2\. Save that effect in a file, whose name starts with a number or a low letter in the alphabet**, for example `aaa_erre_shotgun_wedding_effect.txt`

Then MVE must do the following:

**1\. Write its own version of the shotgun wedding effect that fires MVE content**, for example:

```
erre_fire_shotgun_wedding_effect = {
    trigger_event = mve_erre_compatibility_shotgun_wedding.1
}
```

**2\. Save that effect in a file whose name starts with a late letter in the alphabet**, for example `zzz_mve_shotgun_wedding_effect.txt`.

Now the two mods are compatible. Here's what will happen:

- If ERRE is loaded but MVE is not, then ERRE will fire _its_ definition of `erre_fire_shotgun_wedding_effect`, which will fire its own event.
- If MVE is loaded but ERRE is not, then `erre_fire_shotgun_wedding_effect` never fires, as MVE does not call it.
- If ERRE and MVE are both loaded, then ERRE will fire `erre_fire_shotgun_wedding_effect` but MVE's definition will get executed. That is because MVE defines the same entity in a file that is later in the alphabet, thus it overrides the former definition.

This basic idea applies to lots of different entity types, and it works regardless of the loading order between those mods, as the loading of different files is done in alphabetical order. You can have shared scripted triggers, scripted effects, scripted modifiers, and so on. What matters is that it is an entity that can be loaded and overridden on an entity basis. As such it does not work for events, hence the need to pipe the calling through a scripted effect.

## Detecting other mods\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Mod_compatibility&veaction=edit&section=6 "Edit section: Detecting other mods") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Mod_compatibility&action=edit&section=6 "Edit section: Detecting other mods")\]

Sometimes you just need to know that a specific mod is active. For example, if _IAcedIELTS's Language Learning Overhaul_ (LLO) is TC-compatible mod, but it does want to use different flavour text related to the Farquaad dialect if the Shrek Total Conversion is active. Shrek, the mod that needs to be detected, can do a few things to announce itself; putting up more signs around one's swamp, but also define either a scripted trigger or a global variable (or both).

### Global variable\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Mod_compatibility&veaction=edit&section=7 "Edit section: Global variable") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Mod_compatibility&action=edit&section=7 "Edit section: Global variable")\]

The global variable works like the shared variable example, with the difference that the variable here lives in the global space, and as such it can be triggered for from anywhere.

The Shrek TC simply writes the following in any on\_action file:

```
on_game_start = { on_actions = { shrek_compatibility_on_game_start } }
shrek_compatibility_on_game_start = {
    effect = {
        set_global_variable = { name = shrek_is_loaded value = yes }
    }
}
```

The first line ensures that this on\_action does not override the effect block of vanilla's on\_game\_start, this is a common mistake. Then LLO can use `has_global_variable = shrek_is_loaded` as its universal check for whether we are in Far Far Away or not.

Two things to keep in mind:

- This will only reliably set the variable _after_ on\_game\_start has passed. Simply, there's no guarantee that when two mods use on\_game\_start, one can fire something before or after the other.
- This will only work if the game is first begun with the Shrek mod active. That's expected for a TC but for other mods, if they are activated midway through a campaign, the variable will not be set.

### Scripted trigger\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Mod_compatibility&veaction=edit&section=8 "Edit section: Scripted trigger") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Mod_compatibility&action=edit&section=8 "Edit section: Scripted trigger")\]

The scripted trigger works like the example we just discussed. The Shrek Total Conversion needs to declare a scripted trigger like this:

```
shrek_is_loaded = {
    always = yes
}
```

It will of course be always true because it is the Shrek mod _defining_ this trigger; when this scripted trigger is loaded, it is loaded. It finally needs to store that scripted trigger _late_ in the alphabet, under a file like `zzz_shrek_compatibility_triggers.txt`.

LLO, a mod that wants to know if Shrek is around, needs to define its own version of `shrek_is_loaded`:

```
shrek_is_loaded = {
    always = no
}
```

It is initialised as `always = no` because there is no Shrek mod by default, it is an opt-in. But if LLO ensures to save this as a file _early_ in the alphabet, for example `aaa_llo_shrek_compatibility_triggers.txt`, then _if_ Shrek is loaded, it will override the scripted trigger. That way, LLO can simply check `shrek_is_loaded = yes` in its events and it will work appropriately.

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
| Other | [Console commands](https://ck3.paradoxwikis.com/Console_commands "Console commands") • [Checksum](https://ck3.paradoxwikis.com/Checksum "Checksum") • [Mod structure](https://ck3.paradoxwikis.com/Mod_structure "Mod structure") • Mod compatibility • [Modding tools](https://ck3.paradoxwikis.com/Modding_tools "Modding tools") • [Troubleshooting](https://ck3.paradoxwikis.com/Mod_troubleshooting "Mod troubleshooting") |

Retrieved from " [https://ck3.paradoxwikis.com/index.php?title=Mod\_compatibility&oldid=32474](https://ck3.paradoxwikis.com/index.php?title=Mod_compatibility&oldid=32474)"

[Category](https://ck3.paradoxwikis.com/Special:Categories "Special:Categories"):

- [Modding](https://ck3.paradoxwikis.com/Category:Modding "Category:Modding")