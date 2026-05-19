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

# Flavorization

From CK3 Wiki

[Jump to navigation](https://ck3.paradoxwikis.com/Flavorization#mw-head) [Jump to search](https://ck3.paradoxwikis.com/Flavorization#searchInput)

Flavorization is how the game defines and prioritizes which "title" to display on characters, who will often qualify for multiple titles. As such, we define the requirements and overall priority of a title in flavorization files to avoid conflicts and inappropriate title placement.

## Contents

- [1Grammar](https://ck3.paradoxwikis.com/Flavorization#Grammar)
- [2Custom Flavor Example](https://ck3.paradoxwikis.com/Flavorization#Custom_Flavor_Example)
- [3Expanding Functionality Through Customizable Localization](https://ck3.paradoxwikis.com/Flavorization#Expanding_Functionality_Through_Customizable_Localization)
- [4Continue Reading](https://ck3.paradoxwikis.com/Flavorization#Continue_Reading)

## Grammar\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Flavorization&veaction=edit&section=1 "Edit section: Grammar") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Flavorization&action=edit&section=1 "Edit section: Grammar")\]

Flavorization entries are broken down like this:

```
prince_male_roman = {							# The key of your title, this is how the game finds and references it
	type = character							# Who/what is this for?
	gender = male								# Which gender is this for? (Only use if type = character)
	special = ruler_child						# Are there any special requirements?
	tier = kingdom								# Which tier must you be?
	priority = 40								# How high priority is this?
	name_lists = { name_list_roman }			# Which name list do you need to belong to in order to get this?
	governments = { feudal_government }			# Which government type do you need to belong to?
	top_liege = no								# Do you need to be top liege of your realm?
}
```

| Entry | Required for Characters? | Required for Titles? | Description & Values |
| --- | --- | --- | --- |
| `type` | ✔️ | ✔️ | Can use either `character` or `title`, defines if it applies to a character or a title. Required for all. |
| `gender` | ✔️ | ❌ | Can use either `male` or `female`. Do not use on titles. |
| `special` | ✔️ | ❌ | Can be `ruler_child` (for princes or princesses), `queen_mother`, `councilor`, `head_of_faith` or `holder`. This has to be defined for character types, `holder` is the most prevalent. |
| `tier` | ❌ | ❌ | Can be `barony`, `county`,` duchy`, `kingdom`, or `empire`. Not needed, but will apply to every tier listed if left undefined. |
| `priority` | ✔️ | ✔️ | Any numeric value. Try to keep it between 0 and 2147483647. |
| `name_lists` | ❌ | ❌ | Defined by the files inside of `..game\common\culture\name_lists`. You can make your own. (Example: `name_list_anglo_saxon`). |
| `heritages` | ❌ | ❌ | Defined by `..game\common\culture\pillars\00_heritage.txt`. You can make your own. (Example: `heritage_north_germanic`). |
| `religions` | ❌ | ❌ | Defined by the files inside of `..game\common\religion\religions`. You can make your own. (Example: `christianity_religion`). |
| `faiths` | ❌ | ❌ | Defined by the faiths in religions. You can make your own. (Example: `coptic`). |
| `governments` | ❌ | ❌ | Defined by `..game\common\governments\00_government_types.txt`. You can make your own. (Example: `feudal_government`). |
| `titles` | ❌ | ❌ | Uses landed titles. (Example: `e_byzantium`). |
| `council_position` | ❌ | ❌ | Use any defined council position. Requires `special = councilor`. Do not use on titles. (Example: `councillor_court_chaplain`). |
| `only_independent` | ❌ | ❌ | Uses `yes` or `no`. Used for titles such as "Petty Kings". |
| `only_holder` | ❌ | ❌ | Uses `yes` or `no`. Spouse will no longer receive the opposite gender title if set to yes. Good for mayors or female rulers. |
| `top_liege` | ❌ | ❌ | Uses `yes` or `no`. Using `top_liege = no`, you can allow vassals with different religions/cultures to use their own title. Does not apply to spouse. |

## Custom Flavor Example\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Flavorization&veaction=edit&section=2 "Edit section: Custom Flavor Example") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Flavorization&action=edit&section=2 "Edit section: Custom Flavor Example")\]

[![](https://ck3.paradoxwikis.com/images/thumb/1/1b/Modding_custom_title_example_roboland.jpg/534px-Modding_custom_title_example_roboland.jpg)](https://ck3.paradoxwikis.com/File:Modding_custom_title_example_roboland.jpg)

[Enlarge](https://ck3.paradoxwikis.com/File:Modding_custom_title_example_roboland.jpg "Enlarge")

The end result of this example.

For this example, let's make a series of robot-themed titles.

The first step is to recreate the in-game flavorization directory (`game\common\flavorization`) in your mod folder, like this: `..Documents\Paradox Interactive\Crusader Kings III\mod\FlavourTestMod\common\flavorization`.

Once you've done this, you can create a text file where your new flavorization will be stored, for this example, we will name ours `my_cool_flavorization.txt`. You can also copy over and modify the vanilla flavorization files, but be warned that this will lesser compatibility with both other mods and future game versions.

Let's script the titles for our future robot overlords and their land:

```
### Robots
king_robot = { # Roboto
	type = character
	gender = male
	special = holder
	tier = county
	priority = 5000
	governments = { feudal_government }
	top_liege = no
}

queen_robot = { # Robota
	type = character
	gender = female
	special = holder
	tier = county
	priority = 5000
	governments = { feudal_government }
	top_liege = no
}

county_robot = { # Roboland
	type = title
	tier = county
	priority = 5000
	governments = { feudal_government tribal_government } # You can add multiple items inside of brackets, no comma required.
	top_liege = no
}
```

We want to very clearly tell if our new titles are working or not, so we've set some very simple rules: Anyone holding a county title in a feudal government is eligible.

We've also set the priority to 5000, higher values are higher priority. With a value this high, our new title will overwrite all others.

Next, we will create a file to store our localization in at `..mod\FlavourTestMod\localization\english\culture` and name it `my_new_culture_titles_l_english.yml`.

Be sure to [encode it as UTF8+Bom!](https://ck3.paradoxwikis.com/Mod_troubleshooting#Localization_Debugging)

Then, inside our localization file, we are going to add text to our title keys:

```
l_english:

### Robot ###
 king_robot: "Roboto"
 queen_robot: "Robota"
 county_robot: "Roboland"
```

If you save both your files and open the game with the mod enabled, you should be able to find " _robotos_" and " _robotas_" tending to their " _robolands_" all across the game world. Congratulations on making your first flavorization.

## Expanding Functionality Through Customizable Localization\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Flavorization&veaction=edit&section=3 "Edit section: Expanding Functionality Through Customizable Localization") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Flavorization&action=edit&section=3 "Edit section: Expanding Functionality Through Customizable Localization")\]

[![](https://ck3.paradoxwikis.com/images/thumb/2/22/Modding_custom_title_example_roboland_custom_localization_example.jpg/321px-Modding_custom_title_example_roboland_custom_localization_example.jpg)](https://ck3.paradoxwikis.com/File:Modding_custom_title_example_roboland_custom_localization_example.jpg)

[Enlarge](https://ck3.paradoxwikis.com/File:Modding_custom_title_example_roboland_custom_localization_example.jpg "Enlarge")

End result of this expansion example, showcasing how the same title can vary loc based on gold amount.

Though flavorization is powerful, it is limited in terms of which triggers it can make use of. If we wish to access a greater range of triggers, we can resort to replacing our key with a [customizable localization](https://ck3.paradoxwikis.com/Customizable_localization) key, which are localization keys with scripted behaviors.

For this example, we will take our `king_robot` title from the previous section and expand upon it.

First, we will create a file to store our custom localization logic in at `..Documents\Paradox Interactive\Crusader Kings III\mod\FlavourTestMod\common\customizable_localization` and name it `my_very_clever_custom_loc.txt`.

Next, we will script the custom logic for our localization key.

We start off by giving it a key and type, in our case, we will use `king_robot` and `character` respectively.

```
king_robot = {
    type = character
```

After that, we define all the possible localization keys it can use by creating `text` blocks, each `text` block should contain within its brackets a trigger and the key of the localization we want it to use if the trigger is successful. The custom loc will then pick the first text block that has a passing trigger. You can use `fallback = yes` to set a block as the default if none succeed (or set a `text` block at the end with no trigger).

```
king_robot = {
    type = character
    text = {
        trigger = {
            gold > 1000 # We can add as many triggers as we want, but for this example we will just check if the character is very wealthy.
        }
        localization_key = golden_king_robot # If the trigger passes (the conditions within it are true), this will be the loc key it will select!
    }
	text = {
		fallback = yes # If nothing else triggers, it will default to this, ignoring triggers.
        localization_key = rusty_king_robot
    }
}
```

As you can see, in this example we have set a gold check, replacing the usual "king robot" title with a "golden king robot" title to characters with over 1000 gold.

Of course, you can add as many complex triggers as you wish, such as a `root.faith = { has_doctrine = tenet_struggle_submission }` trigger to see if the character's faith has the `tenet_struggle_submission` tenet.

Next, we will go to our localization file from before and add the `golden_king_robot` and `rusty_king_robot` keys that we used in the previous script.

We will also tell the game to run our custom localization logic whenever the `king_robot` key is used by using a custom loc entry: `[CHARACTER.Custom('king_robot')]`.

```
l_english:

### Robot ###
 king_robot: "[CHARACTER.Custom('king_robot')]"
 golden_king_robot: "Gold-Plated MegaBot"
 rusty_king_robot: "Rust-Plated Microbot"
 queen_robot: "Robota"
 county_robot: "Roboland"
```

With this, you've successfully added a variation to your title using custom localization! Congratulations!

## Continue Reading\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Flavorization&veaction=edit&section=4 "Edit section: Continue Reading") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Flavorization&action=edit&section=4 "Edit section: Continue Reading")\]

- TheGib770 made an excellent guide (Link: [forum:1449550](https://forum.paradoxplaza.com/forum/index.php?threads/1449550 "forum:1449550")) on the Paradox Forum which delves deeper into the details and intricacies of flavorization. Feel free to reach out to him.

**[Modding](https://ck3.paradoxwikis.com/Modding "Modding")**

|     |     |
| --- | --- |
| Documentation | [Scripting](https://ck3.paradoxwikis.com/Scripting "Scripting") • [Scopes](https://ck3.paradoxwikis.com/Scopes "Scopes") • [Effects](https://ck3.paradoxwikis.com/Effects "Effects") • [Triggers](https://ck3.paradoxwikis.com/Triggers "Triggers") • [Variables](https://ck3.paradoxwikis.com/Variables "Variables") • [Modifiers](https://ck3.paradoxwikis.com/Modifier_list "Modifier list") |

|     |     |
| --- | --- |
| Scripting | [AI](https://ck3.paradoxwikis.com/AI_modding "AI modding") • [Bookmarks](https://ck3.paradoxwikis.com/Bookmarks_modding "Bookmarks modding") • [Characters](https://ck3.paradoxwikis.com/Characters_modding "Characters modding") • [Commands](https://ck3.paradoxwikis.com/Commands "Commands") • [Council](https://ck3.paradoxwikis.com/Council_modding "Council modding") • [Culture](https://ck3.paradoxwikis.com/Culture_modding "Culture modding") • [Decisions](https://ck3.paradoxwikis.com/Decisions_modding "Decisions modding") • [Dynasties](https://ck3.paradoxwikis.com/Dynasties_modding "Dynasties modding") • [Events](https://ck3.paradoxwikis.com/Event_modding "Event modding") • [Governments](https://ck3.paradoxwikis.com/Governments_modding "Governments modding") • [History](https://ck3.paradoxwikis.com/History_modding "History modding") • [Holdings](https://ck3.paradoxwikis.com/Holdings_modding "Holdings modding") • [Lifestyles](https://ck3.paradoxwikis.com/Lifestyles_modding "Lifestyles modding") • [Regiments](https://ck3.paradoxwikis.com/Regiments_modding "Regiments modding") • [Religions](https://ck3.paradoxwikis.com/Religions_modding "Religions modding") • [Script Values](https://ck3.paradoxwikis.com/Script_values "Script values") • [Story cycles](https://ck3.paradoxwikis.com/Story_cycles_modding "Story cycles modding") • [Struggles](https://ck3.paradoxwikis.com/Struggle_modding "Struggle modding") • [Titles](https://ck3.paradoxwikis.com/Title_modding "Title modding") • [Traits](https://ck3.paradoxwikis.com/Trait_modding "Trait modding") |

|     |     |
| --- | --- |
| Interface | [Interface](https://ck3.paradoxwikis.com/Interface "Interface") • [Data types](https://ck3.paradoxwikis.com/Data_types "Data types") • [Localization](https://ck3.paradoxwikis.com/Localization "Localization") • [Customizable localization](https://ck3.paradoxwikis.com/Customizable_localization "Customizable localization") • Flavorization |

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

Retrieved from " [https://ck3.paradoxwikis.com/index.php?title=Flavorization&oldid=31792](https://ck3.paradoxwikis.com/index.php?title=Flavorization&oldid=31792)"

[Category](https://ck3.paradoxwikis.com/Special:Categories "Special:Categories"):

- [Modding](https://ck3.paradoxwikis.com/Category:Modding "Category:Modding")