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

# Music modding

From CK3 Wiki

[Jump to navigation](https://ck3.paradoxwikis.com/Music_modding#mw-head) [Jump to search](https://ck3.paradoxwikis.com/Music_modding#searchInput)

It is possible to mod custom music into the game, as well as script when and where said tracks will play.

To add the Music tracks we wish to put into the Music Player into categories. To do this they must be implemented with the following files structure:

```
game
└ music
  ├ music_categories
  │ └ music_categories.txt
  └ music.txt
```

The **music.txt** files contain information on the tracks themselves, and in order to have them localized they all must have a _name = loc\_key_ field.
Example:

```
mx_raid = {
    music = "event:/DLC/FP1/MUSIC/cuetracks/mx_raid"
     name = fp1_soundtrack_01_the_raid
    pause_factor = 35
}
```

The **music\_category.txt** files contains information on the categories and tracks contained within them:

```
category = {
     id = "mx_category_10"
     name = "fp2_cue_soundtrack"
     tracks = {
         "mx_IberiaWar"
         "mx_Struggle_ending_compromise"
         "mx_Struggle_ending_conciliation"
         "mx_Struggle_ending_hostility"
         "mx_Struggle_Opening"
     }
 }
```

It is important to note that the **id** field in these categories _**must**_ be unique.

Finally to get the art in, they'll be put into following structure, if using the above category as an example:

```
game
└ gfx
  └ interface
    └ illustrations
      └ music_player
        └ fp2_cue_soundtrack.dds
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
| Audio | Music • [Sound](https://ck3.paradoxwikis.com/Sound_modding "Sound modding") |

|     |     |
| --- | --- |
| Other | [Console commands](https://ck3.paradoxwikis.com/Console_commands "Console commands") • [Checksum](https://ck3.paradoxwikis.com/Checksum "Checksum") • [Mod structure](https://ck3.paradoxwikis.com/Mod_structure "Mod structure") • [Mod compatibility](https://ck3.paradoxwikis.com/Mod_compatibility "Mod compatibility") • [Modding tools](https://ck3.paradoxwikis.com/Modding_tools "Modding tools") • [Troubleshooting](https://ck3.paradoxwikis.com/Mod_troubleshooting "Mod troubleshooting") |

**[Mechanics](https://ck3.paradoxwikis.com/Mechanics "Mechanics")**

|     |     |
| --- | --- |
| Characters | [Characters](https://ck3.paradoxwikis.com/Characters "Characters") • [Attributes](https://ck3.paradoxwikis.com/Attributes "Attributes") • [Traits](https://ck3.paradoxwikis.com/Traits "Traits") • [Resources](https://ck3.paradoxwikis.com/Resources "Resources") • [Modifiers](https://ck3.paradoxwikis.com/Modifiers "Modifiers") • [Lifestyle](https://ck3.paradoxwikis.com/Lifestyle "Lifestyle") • [Family](https://ck3.paradoxwikis.com/Family_(relation) "Family (relation)") • [Dynasty](https://ck3.paradoxwikis.com/Dynasty "Dynasty") • [Schemes](https://ck3.paradoxwikis.com/Schemes "Schemes") • [Hooks](https://ck3.paradoxwikis.com/Hooks "Hooks") • [Activities](https://ck3.paradoxwikis.com/Activity "Activity") • [Artifacts](https://ck3.paradoxwikis.com/Artifacts "Artifacts") • [Interactions](https://ck3.paradoxwikis.com/Interactions "Interactions") • [Travel](https://ck3.paradoxwikis.com/Travel "Travel") • [Adventurers](https://ck3.paradoxwikis.com/Adventurer "Adventurer") • [Prisoners](https://ck3.paradoxwikis.com/Prisoner "Prisoner") |

|     |     |
| --- | --- |
| Realm & Governance | [Council](https://ck3.paradoxwikis.com/Council "Council") • [Court](https://ck3.paradoxwikis.com/Court "Court") • [Power sharing](https://ck3.paradoxwikis.com/Power_sharing "Power sharing") • [Subjects](https://ck3.paradoxwikis.com/Subjects "Subjects") • [Succession](https://ck3.paradoxwikis.com/Succession "Succession") • [Government](https://ck3.paradoxwikis.com/Government "Government") • [Laws](https://ck3.paradoxwikis.com/Laws "Laws") • [Decisions](https://ck3.paradoxwikis.com/Decisions "Decisions") • [Titles](https://ck3.paradoxwikis.com/Titles "Titles") • [Barony](https://ck3.paradoxwikis.com/Barony "Barony") • [County](https://ck3.paradoxwikis.com/County "County") • [Buildings](https://ck3.paradoxwikis.com/Buildings "Buildings") • [Royal court](https://ck3.paradoxwikis.com/Royal_court "Royal court") • [Domiciles](https://ck3.paradoxwikis.com/Domicile "Domicile") • [Great projects](https://ck3.paradoxwikis.com/Great_projects "Great projects") |

|     |     |
| --- | --- |
| Warfare | [Warfare](https://ck3.paradoxwikis.com/Warfare "Warfare") • [Casus belli](https://ck3.paradoxwikis.com/Casus_belli "Casus belli") • [Alliance](https://ck3.paradoxwikis.com/Alliance "Alliance") • [Army](https://ck3.paradoxwikis.com/Army "Army") • [Hired forces](https://ck3.paradoxwikis.com/Hired_forces "Hired forces") • [Knights](https://ck3.paradoxwikis.com/Knight "Knight") • [Duel](https://ck3.paradoxwikis.com/Duel "Duel") • [Situations](https://ck3.paradoxwikis.com/Situation "Situation") |

|     |     |
| --- | --- |
| Culture & Faith | [Culture](https://ck3.paradoxwikis.com/Culture "Culture") • [Traditions](https://ck3.paradoxwikis.com/Traditions "Traditions") • [Innovations](https://ck3.paradoxwikis.com/Innovation "Innovation") • [Form of Address](https://ck3.paradoxwikis.com/Form_of_address "Form of address") • [Faith](https://ck3.paradoxwikis.com/Faith "Faith") • [Doctrines](https://ck3.paradoxwikis.com/Doctrines "Doctrines") • [Tenets](https://ck3.paradoxwikis.com/Tenets "Tenets") • [Holy sites](https://ck3.paradoxwikis.com/Holy_sites "Holy sites") |

|     |     |
| --- | --- |
| Meta | [Modding](https://ck3.paradoxwikis.com/Modding "Modding") • [Patches](https://ck3.paradoxwikis.com/Patches "Patches") • [Downloadable content](https://ck3.paradoxwikis.com/Downloadable_content "Downloadable content") • [Developer diaries](https://ck3.paradoxwikis.com/Developer_diaries "Developer diaries") • [Achievements](https://ck3.paradoxwikis.com/Achievements "Achievements") • [Jargon](https://ck3.paradoxwikis.com/Jargon "Jargon") • [Bookmarks](https://ck3.paradoxwikis.com/Bookmarks "Bookmarks") • [Interesting characters](https://ck3.paradoxwikis.com/Interesting_characters "Interesting characters") • [Ruler Designer](https://ck3.paradoxwikis.com/Ruler_Designer "Ruler Designer") • [Game rules](https://ck3.paradoxwikis.com/Game_rules "Game rules") |

Retrieved from " [https://ck3.paradoxwikis.com/index.php?title=Music\_modding&oldid=24677](https://ck3.paradoxwikis.com/index.php?title=Music_modding&oldid=24677)"

[Category](https://ck3.paradoxwikis.com/Special:Categories "Special:Categories"):

- [Modding](https://ck3.paradoxwikis.com/Category:Modding "Category:Modding")