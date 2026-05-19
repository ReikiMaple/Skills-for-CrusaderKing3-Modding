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

# Defines

From CK3 Wiki

[Jump to navigation](https://ck3.paradoxwikis.com/Defines#mw-head) [Jump to search](https://ck3.paradoxwikis.com/Defines#searchInput)

Please help with verifying or updating older sections of this article.

At least some were last verified for [version](https://ck3.paradoxwikis.com/CK3_Wiki:Versioning "CK3 Wiki:Versioning") 1.2.

This article is for the PC version of Crusader Kings 3 only.

**Defines** are constants that affect certain non-scriptable game behaviors, such as army movement and schemes. They are static and global: they apply to the whole game and cannot be changed dynamically.

## Contents

- [1Configuration](https://ck3.paradoxwikis.com/Defines#Configuration)
- [2List of defines](https://ck3.paradoxwikis.com/Defines#List_of_defines)
  - [2.1Game](https://ck3.paradoxwikis.com/Defines#Game)
  - [2.2Setup](https://ck3.paradoxwikis.com/Defines#Setup)
  - [2.3Jomini Map](https://ck3.paradoxwikis.com/Defines#Jomini_Map)
  - [2.4Characters](https://ck3.paradoxwikis.com/Defines#Characters)

## Configuration\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Defines&veaction=edit&section=1 "Edit section: Configuration") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Defines&action=edit&section=1 "Edit section: Configuration")\]

Vanilla defines are set in _game\\common\\defines\\00\_defines.txt_.

To modify defines, it is best not to modify the original file, but rather to use a mod. To do so, [create a mod](https://ck3.paradoxwikis.com/Mod_structure#Creating_initial_files "Mod structure"), then create a text file in _Documents\\Paradox Interactive\\mod\\\[mod name\]\\common\\defines_. To change a define, use the following format in the following example, which changes the end date to 1800:

```
NGame = {
    END_DATE = "1800.1.1"
}
```

The file only needs to contain the edited defines—ones that are not being changed can be left out.

## List of defines\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Defines&veaction=edit&section=2 "Edit section: List of defines") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Defines&action=edit&section=2 "Edit section: List of defines")\]

The following is a (non-exhaustive) list of defines, organized by category.

### Game\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Defines&veaction=edit&section=3 "Edit section: Game") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Defines&action=edit&section=3 "Edit section: Game")\]

| Variable | Unit | Notes/description |
| --- | --- | --- |
| END\_DATE = "1453.1.1" |  | YYYY.M.D |
| GAME\_SPEED\_TICKS | Seconds | Number of seconds a day should take at every game speed (first value is speed 1, last value is speed 5). |
| COMBAT\_TICK\_LIMIT = 1 |  |  |
| LAG\_DECREASE\_SPEED\_DAYS = 15 | Days | Number of days of client lag that will cause a speed decrease in multiplayer. |
| LAG\_PAUSE\_DAYS = 30 | Days | Number of days of client lag that will cause a pause in multiplayer. |
| MULTIPLAYER\_EVENT\_TIME\_OUT = 90 | Days | Number of days an event will show in multiplayer. When all time has passed, the game will automatically select an option. |
| BENCHMARK\_TEST\_DURATION = 135 | Seconds | Duration of a benchmark test using the "-benchmark" launch option. |
| BENCHMARK\_INTERFACE\_INTERVAL = 5.0 | Seconds | Time before the benchmark changes the open UI window. |
| BENCHMARK\_OBSERVE\_CHARACTER = k\_england | Title | The title of the character who will be observed for the benchmark. |
| BENCHMARK\_WAYPOINTS |  | Where the camera should pan during the benchmark. |

### Setup\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Defines&veaction=edit&section=4 "Edit section: Setup") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Defines&action=edit&section=4 "Edit section: Setup")\]

| Variable | Unit | Notes/description |
| --- | --- | --- |
| COURTLESS\_CHARACTER\_GUEST\_CHANCE = 0.25 |  | Chance that a courtless character is sent to a court as a guest instead of a regular courtier on game start. |
| GENERATED\_POOL\_CHARACTERS |  | Random range for number of characters per pool (duchy) generated at the start of the game |
| GENERATED\_POOL\_CHARACTER\_TEMPLATES |  | Templates used for the pool character. Presumably, the trait-based templates are characters skilled in that trait. |
| GENERATED\_POOL\_CHARACTER\_TEMPLATE\_WEIGHTS |  | Influence the chance of each template appearing. Correspond to the template names at the same index. |
| DESIRED\_NEIGHBOR\_POOLS = 4 |  | Number of pools each pool should try to border. |
| MAX\_POOL\_NEIGHBOR\_DISTANCE = 3 |  | Maximum number of sea zones away a pool should search for a neighboring pool. |

### Jomini Map\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Defines&veaction=edit&section=5 "Edit section: Jomini Map") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Defines&action=edit&section=5 "Edit section: Jomini Map")\]

| Variable | Unit | Notes/description |
| --- | --- | --- |
| WORLD\_EXTENTS\_X = 8191 |  | How wide the map is. |
| WORLD\_EXTENTS\_Y = 51 |  | How deep the map is. |
| WORLD\_EXTENTS\_Z = 4095 |  | How tall the map is. |
| WATERLEVEL = 3.8 |  |  |

### Characters\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Defines&veaction=edit&section=6 "Edit section: Characters") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Defines&action=edit&section=6 "Edit section: Characters")\]

| Variable | Unit | Notes/description |
| --- | --- | --- |
| MALE\_RANDOM\_AGE\_BASE = 16 | Years | The initial age of randomly-generated male characters. |
| MALE\_RANDOM\_AGE\_SPAN = 20 | Years | The maximum difference from the base age of male characters. The age of a random character is equal to the base plus a random value within the span. |
| FEMALE\_RANDOM\_AGE\_BASE = 16 | Years | The initial age of randomly-generated female characters. |
| FEMALE\_RANDOM\_AGE\_SPAN = 16 | Years | The maximum difference from the base age of female characters. The age of a random character is equal to the base plus a random value within the span. |
| RANDOM\_PERSONALITY\_TRAITS\_BASE = 3 |  | The initial number of personality traits for randomly-generated characters. |
| RANDOM\_PERSONALITY\_TRAITS\_SPAN = 0 |  | The maximum difference from the base number of traits. By default, randomly-generated characters always have 3 traits. |
| RANDOM\_CHARACTER\_DIPLOMACY\_MIN = 0 |  | Minimum possible base diplomacy of a randomly-generated character. |
| RANDOM\_CHARACTER\_DIPLOMACY\_MAX = 10 |  | Maximum possible base diplomacy of a randomly-generated character. |
| RANDOM\_CHARACTER\_MARTIAL\_MIN = 0 |  | Minimum possible base martial of a randomly-generated character. |
| RANDOM\_CHARACTER\_MARTIAL\_MAX = 10 |  | Maximum possible base martial of a randomly-generated character. |
| RANDOM\_CHARACTER\_STEWARDSHIP\_MIN = 0 |  | Minimum possible base stewardship of a randomly-generated character. |
| RANDOM\_CHARACTER\_STEWARDSHIP\_MAX = 10 |  | Maximum possible base stewardship of a randomly-generated character. |
| RANDOM\_CHARACTER\_INTRIGUE\_MIN = 0 |  | Minimum possible base intrigue of a randomly-generated character. |
| RANDOM\_CHARACTER\_INTRIGUE\_MAX = 10 |  | Maximum possible base intrigue of a randomly-generated character. |
| RANDOM\_CHARACTER\_LEARNING\_MIN = 0 |  | Minimum possible base learning of a randomly-generated character. |
| RANDOM\_CHARACTER\_LEARNING\_MAX = 10 |  | Maximum possible base learning of a randomly-generated character. |
| RANDOM\_CHARACTER\_PROWESS\_MIN = 0 |  | Minimum possible base prowess of a randomly-generated character. |
| RANDOM\_CHARACTER\_PROWESS\_MAX = 10 |  | Maximum possible base prowess of a randomly-generated character. |
| RANDOM\_CHARACTER\_MIN\_FERTILITY = 0.5 |  | Minimum possible base fertility of a randomly-generated character. |
| RANDOM\_CHARACTER\_MAX\_FERTILITY = 0.6 |  | Maximum possible base fertility of a randomly-generated character. |
| RANDOM\_CHARACTER\_MIN\_HEALTH = 4.0 |  | Minimum possible base health of a randomly-generated character. |
| RANDOM\_CHARACTER\_MAX\_HEALTH = 5.0 |  | Maximum possible base health of a randomly-generated character. |
| RANDOM\_CHARACTER\_AGE\_MIN\_HEALTH = 2.5 |  | Minimum base health for randomly-generated characters after adjusting for age. |
| MAX\_STRESS\_LEVEL = 3 |  |  |
| STRESS\_PER\_LEVEL = 100 |  |  |
| STRESS\_MONTHLY\_CHANGE = 0 |  | Stress changes monthly by this value until reaching a character's base stress. |
| MAX\_DREAD = 100 |  |  |
| BASE\_DREAD = 0 |  |  |
| DREAD\_MONTHLY\_CHANGE = 0.5 |  | Dread changes monthly by this value until reaching a character's base dread. |
| BOLD\_LEVEL\_COWED = 45 |  | The amount of dread above a character's [boldness value](https://ck3.paradoxwikis.com/Attributes#Dread "Attributes") for them to be terrified. |
| BOLD\_LEVEL\_INTIMIDATED = 20 |  | The amount of dread above a character's [boldness value](https://ck3.paradoxwikis.com/Attributes#Dread "Attributes") for them to be intimidated. |
| MAX\_TYRANNY = 1000 |  |  |
| TYRANNY\_MONTHLY\_CHANGE = -0.25 |  | Tyranny changes by this amount every month. |
| BASE\_FERTILITY = 0.5 |  |  |
| BASE\_HEALTH = 5.0 |  |  |
| LEVELS\_PIETY |  | Amounts of piety needed for various devotion levels. The first/lowest level is first in the list, and they are sorted in ascending order. |
| LEVELS\_PRESTIGE |  | Amounts of prestige needed for various fame levels. The first/lowest level is first in the list, and they are sorted in ascending order. |
| BASE\_PIETY\_EXPERIENCE = 1000 |  | Initial piety experience (used for devotion). |
| BASE\_PRESTIGE\_EXPERIENCE = 1000 |  | Initial prestige experience (used for fame). |
| LEVEL\_DROP\_MAX\_RETAINED\_PROGRESS\_PIETY = 0.5 |  | A character who drops a level of devotion retains this amount (percentage) of progress towards the next level. |
| LEVEL\_DROP\_MAX\_RETAINED\_PROGRESS\_PRESTIGE = 0.5 |  | A character who drops a level of fame retains this amount (percentage) of progress towards the next level. |
| LEVELS\_PIETY\_GRAPHICAL\_STEP = 1 |  | How many levels of devotion should increment before the icon changes. |
| LEVELS\_PRESTIGE\_GRAPHICAL\_STEP = 1 |  | How many levels of fame should increment before the icon changes. |
| PIETY\_ZERO\_LEVEL = 1 |  | The devotion level considered to be the initial or "zero" level. |
| PRESTIGE\_ZERO\_LEVEL = 1 |  | The fame level considered to be the initial or "zero" level. |
| TODDLER\_AGE = 3 | Years | Age at which a character becomes a toddler. This is when they receive their childhood trait. |
| CHILDHOOD\_AGE = 6 | Years | Age at which a character becomes a child. This is when they are assigned an education (based on the childhood trait) and begin their education. |
| ADOLESCENCE\_AGE = 12 | Years | Age of adolescence. Used for education. |
| MALE\_ADULT\_AGE = 16 | Years | Age at which male characters become adults, which has several effects, such as unlocking various diplomatic actions. |
| FEMALE\_ADULT\_AGE = 16 | Years | Age at which female characters become adults, which has several effects, such as unlocking various diplomatic actions. |
| BETROTHAL\_TIMEOUT\_AGE = 17 | Years | Presumably the age at which unfulfilled betrothals are cancelled (once both have reached this age). |
| MALE\_ATTRACTION\_CUTOFF\_AGE = 65 | Years | After this age, the attraction of traits no longer has an effect for male characters. |
| FEMALE\_ATTRACTION\_CUTOFF\_AGE = 50 | Years | After this age, the attraction of traits no longer has an effect for female characters. |
| HEALTH\_STATE\_LEVELS\_VALUES |  | Health thresholds for the various health levels (such as "fine," "poor," etc.). |
| HEALTH\_STATE\_LEVELS\_TEXTS |  | Text for the various health thresholds. They correspond with the levels defined in HEALTH\_STATE\_LEVELS\_VALUES. |
| SKILL\_LEVELS\_VALUES |  | Skill level thresholds used for the descriptions (such as "average," "good," etc.). |
| SKILL\_LEVELS\_TEXTS |  | Text for the various skill level thresholds. They correspond with the levels defined in SKILL\_LEVELS\_VALUES. |
| SKILL\_MODIFIER\_OFFSET = -8 |  | Skill modifiers with offset add this from the skill value. |
| MAX\_RELATIONS\_TO\_SHOW = 3 |  | Used for the character window. |
| PRESTIGE\_FROM\_DYNASTY\_ON\_MARRIAGE\_FACTOR = 0.1 |  | Used to calculate prestige gain on marriage. |
| PRESTIGE\_FROM\_DYNASTY\_ON\_BORN\_FACTOR = 0.2 |  | Used to calculate initial prestige on birth. |
| MARRIAGE\_TIER\_DIFF\_PRESTIGE\_MULT = 100 |  |  |
| CHARACTER\_TRAVEL\_TIME = 0.1 |  | Multiplied by the distance between locations on the map. |
| FOCUS\_CHILD\_MIN\_AGE = 6 |  |  |
| FOCUS\_CHILD\_MAX\_CHANGES = 1 |  | Maximum number of times a child's education focus can be changed. |
| FOCUS\_ADULT\_COOLDOWN\_MONTHS = 60 | Months | Number of months between being able to change lifestyle focus. |
| SKILL\_SCALE\_AGE = 16 |  |  |
| MAX\_HEIR\_TO\_SHOWN = 4 |  | Number of "heir to" titles to be shown. |
| MAX\_PARENT\_STEPS\_FOR\_HEIR = 6 |  | Number of steps up to search for heirs if no descendants can be found. |
| MIN\_HEIR\_TO\_FIND = 20 |  | Number of heirs to find (in the line of succession) before stopping to look for more. Higher numbers can negatively impact performance. |
| MAX\_HEIRS\_IN\_LINE\_OF\_SUCCESSION\_TOOLTIP = 5 |  | How many heirs to show in the tooltip for a title. |
| MAX\_POTENTIAL\_SPOUSES = 100000 |  | Maximum number of potential spouses shown in the "find spouse" or "arrange marriage" windows. |
| MONTHS\_OF\_INCOME\_AT\_START = 12 | Months | All rulers start with this many months of income in their treasuries. |
| MAXIMUM\_DIPLOMATIC\_RANGE = 1000 |  | Distance before characters are considered outside of diplomatic range on the default setting. |
| MAXIMUM\_DIPLOMATIC\_RANGE\_RESTRICTED = 750 |  | Distance before characters are considered outside of diplomatic range on the restricted diplomatic range game rule. |
| HOOK\_COOLDOWN\_DURATION\_YEARS = 5 | Years | Strong hook cooldown duration (upon being used). |
| MAX\_COUNTIES\_IN\_REALM\_AS\_DUKE = 30 |  | As a duke or count, the player (AI characters are unaffected) will begin to suffer penalties if going beyond this number of counties. Kings and emperors do not suffer the penalty. |
| INCOME\_PENALTY\_PER\_COUNTY\_ABOVE\_LIMIT = 0.05 |  | Going above the county limit defined in MAX\_COUNTIES\_IN\_REALM\_AS\_DUKE reduces monthly income by this percentage per county. |
| FORCED\_SUCCESSION\_ELECTION\_YEARS = 5 | Years | Length of time someone is forced to vote with another elector when a strong hook is used to do so. |
| MINIMUM\_VALUE\_FOR\_PERSONALITY\_DESCRIPTION = 25 |  | [AI personality](https://ck3.paradoxwikis.com/Character#AI_Personality "Character") values below this are ignored when building personality descriptions. |
| STRONG\_VALUE\_FOR\_PERSONALITY\_DESCRIPTION = 75 |  | AI personality values above this get a stronger version in the personality description. |
| MINIMUM\_TIER\_FOR\_REGNAL\_NUMBERING = 3 |  | Minimum tier in order for regnal numbering to be used. 1 is baron, 5 is emperor. |
| PERCENTAGE\_HOMOSEXUAL = 5.0 |  | Percentage chance of a randomly-created character being homosexual. |
| PERCENTAGE\_BISEXUAL = 5.0 |  | Percentage chance of a randomly-created character being bisexual. |
| PERCENTAGE\_ASEXUAL = 1.0 |  | Percentage chance of a randomly-created character being asexual. |
| DESIGNATE\_HEIR\_DISPLAY\_COST = 1000 |  | Prestige cost for designating an heir. |
| PRETENDERS\_TO\_TITLE = 5 |  | Maximum number of characters to be stored as pretenders to a title (including the heir). |
| PARTITION\_SCORE\_PER\_OWN\_COUNTY = 2 |  | Score an owned county contributes in partition when selecting a title. The higher this value, the more getting a title with personally-owned land is encouraged. |
| PARTITION\_SCORE\_PER\_OTHER\_COUNTY = 1 |  | Score that a county owned by another heir takes away in partition when selecting a title. The higher this is, the more getting a title with land not owned by other heirs is encouraged. |
| DESIRED\_CONCUBINES\_PER\_TIER |  | Number of concubines a ruler of each tier wants if their faith allows concubines, in ascending order by tier. |
| PRESTIGE\_LOSS\_PER\_MISSING\_CONCUBINE = 0.1 |  | Monthly prestige loss per missing fertile concubine. |
| DEBT\_MODIFIER\_THRESHOLDS |  | When the various debt modifiers take effect, by months of income of debt. |

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
| Other | [Console commands](https://ck3.paradoxwikis.com/Console_commands "Console commands") • [Checksum](https://ck3.paradoxwikis.com/Checksum "Checksum") • [Mod structure](https://ck3.paradoxwikis.com/Mod_structure "Mod structure") • [Mod compatibility](https://ck3.paradoxwikis.com/Mod_compatibility "Mod compatibility") • [Modding tools](https://ck3.paradoxwikis.com/Modding_tools "Modding tools") • [Troubleshooting](https://ck3.paradoxwikis.com/Mod_troubleshooting "Mod troubleshooting") |

Retrieved from " [https://ck3.paradoxwikis.com/index.php?title=Defines&oldid=19514](https://ck3.paradoxwikis.com/index.php?title=Defines&oldid=19514)"

[Categories](https://ck3.paradoxwikis.com/Special:Categories "Special:Categories"):

- [Potentially outdated](https://ck3.paradoxwikis.com/Category:Potentially_outdated "Category:Potentially outdated")
- [1.2](https://ck3.paradoxwikis.com/Category:1.2 "Category:1.2")
- [Modding](https://ck3.paradoxwikis.com/Category:Modding "Category:Modding")