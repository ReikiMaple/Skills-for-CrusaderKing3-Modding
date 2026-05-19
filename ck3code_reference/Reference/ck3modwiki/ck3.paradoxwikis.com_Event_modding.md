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

# Event modding

From CK3 Wiki

[Jump to navigation](https://ck3.paradoxwikis.com/Event_modding#mw-head) [Jump to search](https://ck3.paradoxwikis.com/Event_modding#searchInput)

This article is [timeless](https://ck3.paradoxwikis.com/Category:Timeless "Category:Timeless") and should be accurate for any version of the game.

|     |     |
| --- | --- |
| ![Wiki letter w.png](https://central.paradoxwikis.com/images/6/6a/Wiki_letter_w.png) | Please help improve this article or section by [**expanding it**](https://ck3.paradoxwikis.com/index.php?title=Event_modding&action=edit). |

Events are the meat of every well-rounded mod; smaller and larger bits of story that can happen to a player during the campaign.

**Checklist.** Your events must:

- be in `your_mod\events\` folder
- have a .txt extension
- have a namespace defined on the first line, like `namespace = my_events`
- use the namespace as their name + number, like `my_events.1 = {...`
- be fired from script in some way, like by an [on\_action](https://ck3.paradoxwikis.com/Event_modding#On_Actions_(on_action) "Event modding")

Events do not fire automatically otherwise, like in older games. Other ways to fire them are decisions, character interactions, story cycles, etc.

## Contents

- [1Scripting Tools](https://ck3.paradoxwikis.com/Event_modding#Scripting_Tools)
  - [1.1Visual Studio Code](https://ck3.paradoxwikis.com/Event_modding#Visual_Studio_Code)
  - [1.2Sublime Text](https://ck3.paradoxwikis.com/Event_modding#Sublime_Text)
  - [1.3Notepad++](https://ck3.paradoxwikis.com/Event_modding#Notepad++)
- [2Location](https://ck3.paradoxwikis.com/Event_modding#Location)
- [3Structure](https://ck3.paradoxwikis.com/Event_modding#Structure)
  - [3.1ID and namespace](https://ck3.paradoxwikis.com/Event_modding#ID_and_namespace)
  - [3.2Flags](https://ck3.paradoxwikis.com/Event_modding#Flags)
- [4Portraits](https://ck3.paradoxwikis.com/Event_modding#Portraits)
  - [4.1Portrait Positions](https://ck3.paradoxwikis.com/Event_modding#Portrait_Positions)
  - [4.2Animations](https://ck3.paradoxwikis.com/Event_modding#Animations)
- [5Themes](https://ck3.paradoxwikis.com/Event_modding#Themes)
  - [5.1Backgrounds](https://ck3.paradoxwikis.com/Event_modding#Backgrounds)
  - [5.2Environments](https://ck3.paradoxwikis.com/Event_modding#Environments)
- [6Trigger](https://ck3.paradoxwikis.com/Event_modding#Trigger)
  - [6.1on\_trigger\_fail](https://ck3.paradoxwikis.com/Event_modding#on_trigger_fail)
- [7Description](https://ck3.paradoxwikis.com/Event_modding#Description)
- [8Immediate](https://ck3.paradoxwikis.com/Event_modding#Immediate)
- [9Options](https://ck3.paradoxwikis.com/Event_modding#Options)
- [10After](https://ck3.paradoxwikis.com/Event_modding#After)
- [11Widgets](https://ck3.paradoxwikis.com/Event_modding#Widgets)
- [12On Actions (on\_action)](https://ck3.paradoxwikis.com/Event_modding#On_Actions_(on_action))
  - [12.1Common examples](https://ck3.paradoxwikis.com/Event_modding#Common_examples)
  - [12.2Appending](https://ck3.paradoxwikis.com/Event_modding#Appending)
  - [12.3Scopes](https://ck3.paradoxwikis.com/Event_modding#Scopes)
  - [12.4Properties](https://ck3.paradoxwikis.com/Event_modding#Properties)
  - [12.5On\_actions from code](https://ck3.paradoxwikis.com/Event_modding#On_actions_from_code)
- [13Strategy](https://ck3.paradoxwikis.com/Event_modding#Strategy)
  - [13.1Triggering the event](https://ck3.paradoxwikis.com/Event_modding#Triggering_the_event)
  - [13.2Techniques and design patterns](https://ck3.paradoxwikis.com/Event_modding#Techniques_and_design_patterns)

## Scripting Tools\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Event_modding&veaction=edit&section=1 "Edit section: Scripting Tools") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Event_modding&action=edit&section=1 "Edit section: Scripting Tools")\]

There are various tools capable of helping modders script events with greater ease.

### Visual Studio Code\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Event_modding&veaction=edit&section=2 "Edit section: Visual Studio Code") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Event_modding&action=edit&section=2 "Edit section: Visual Studio Code")\]

[Visual Studio Code](https://code.visualstudio.com/) is considered to be the superior choice for modders due to the fact that it features various extensions that allow it to syntax highlight ParadoxScript.

**Recommended Extensions:**

- [CWTools - Paradox Language Services by Thomas Boby](https://marketplace.visualstudio.com/items?itemName=tboby.cwtools-vscode)
- [Paradox Syntax Highlighting by Thomas Boby](https://marketplace.visualstudio.com/items?itemName=tboby.paradox-syntax)

| Snippets For Visual Studio Code |
| --- |
| VSCode snippets are templates that make it easier to enter repeating code patterns, such as complicated scripted effects, conditional statements, or even entire events.<br>It is easy to make custom snippets for templating CK3 script components, below you can find a vanilla sample set. You are encouraged to expand upon this and make your own set tailored to your mod's needs.<br>Read more: [Snippets in Visual Studio Code - Microsoft Corporation](https://marketplace.visualstudio.com/items?itemName=tboby.cwtools-vscode) |
| ```<br>/////////////////////////////////////////////////////////////////////////////////////////////////////<br>// Crusader Kings 3 - Snippets for Visual Studio Code.                                             //<br>//                                                                                                 //<br>// How to use in four easy steps:                                                                  //<br>// 1. Install [CWTools - Paradox Language Services] by Thomas Boby                                 //<br>// 2. Install [Paradox Syntax Highlighting] by Thomas Boby                                         //<br>// 3. Copy this file to ..AppData\Roaming\Code\User\snippets                                       //<br>// 4. That's it! Now just start typing the prefix of a snippet and press tab to insert it!         //<br>/////////////////////////////////////////////////////////////////////////////////////////////////////<br>// Learn more: https://code.visualstudio.com/docs/editor/userdefinedsnippets                       //<br>// Use https://vscodesnippetgenerator.azurewebsites.net/, other tools convert tabs into spaces!!   //<br>/////////////////////////////////////////////////////////////////////////////////////////////////////<br>{<br>  "Legacy Duel": {<br>      "prefix": ["duel", "legacy duel"],<br>      "body": [<br>        "duel = {",<br>        "\tskill = learning",<br>        "\tvalue = average_skill_rating",<br>        "",<br>        "\t10 = { # Failure",<br>        "\t\t#desc = martial_authority_4001.fail.tt",<br>        "\t\tcompare_modifier = {",<br>        "\t\t\tvalue = scope:duel_value",<br>        "\t\t\tmultiplier = -1.5",<br>        "\t\t\tmin = -5",<br>        "\t\t}",<br>        "",<br>        "\t\tsend_interface_toast = {",<br>        "\t\t\ttype = event_toast_effect_bad",<br>        "\t\t\ttitle = death_bleeder",<br>        "\t\t\tleft_icon = root",<br>        "\t\t\t",<br>        "\t\t\tadd_prestige = minor_prestige_loss",<br>        "\t\t}",<br>        "\t}",<br>        "\t10 = { # Success",<br>        "\t\t#desc = bp1_yearly.1031.c_killed_all.tt",<br>        "\t\tcompare_modifier = {",<br>        "\t\t\tvalue = scope:duel_value",<br>        "\t\t\tmultiplier = 1.5",<br>        "\t\t}",<br>        "",<br>        "\t\tsend_interface_toast = {",<br>        "\t\t\ttype = event_toast_effect_good",<br>        "\t\t\ttitle = tribal.1101.a_success",<br>        "\t\t\tleft_icon = root",<br>        "\t\t\t",<br>        "\t\t\tadd_prestige = medium_prestige_gain",<br>        "\t\t}",<br>        "\t}",<br>        "}"<br>      ],<br>      "description": "A legacy duel powered by a random list."<br>  },<br>  "Combat Duel": {<br>      "prefix": ["duel", "combat duel", "fight"],<br>      "body": [<br>        "configure_start_single_combat_effect = {",<br>        "\tSC_INITIATOR = scope:actor ",<br>        "\tSC_ATTACKER = scope:actor",<br>        "\tSC_DEFENDER = scope:recipient",<br>        "\tFATALITY = default",<br>        "\tFIXED = no",<br>        "\tLOCALE = terrain_scope",<br>        "\tOUTPUT_EVENT = single_combat.1006",<br>        "\tINVALIDATION_EVENT = single_combat.1006",<br>        "}"<br>        ],<br>      "description": "A combat duel using the new duelling system."<br>  },<br>  "Hidden Event": {<br>      "prefix": ["event", "hidden event"],<br>      "body": [<br>          "yournamespace.0000 = {",<br>          "\thidden = yes",<br>          "",<br>          "\timmediate = {",<br>          "\t\t",<br>          "\t}",<br>          "}"<br>        ],<br>      "description": "A hidden event, does not render UI or present any options. Utilized for the automation of certain tasks, such as sieges or timed outcomes."<br>  },<br>  "Simple Event": {<br>      "prefix": ["event", "simple event"],<br>      "body": [<br>        "yournamespace.0000 = {",<br>        "\ttype = character_event",<br>        "\ttitle = stewardship_domain_special.1424.a",<br>        "\tdesc = stewardship_domain_special.1424.a",<br>        "",<br>        "\ttheme = mental_break",<br>        "\tleft_portrait = root",<br>        "",<br>        "\ttrigger = {",<br>        "\t\t",<br>        "\t}",<br>        "",<br>        "\timmediate = {",<br>        "\t\t",<br>        "\t}",<br>        "",<br>        "\toption = {",<br>        "\t\tname = stewardship_domain_special.1424.a",<br>        "\t}",<br>        "}"<br>        ],<br>      "description": "A simple event template containing all of the basics."<br>  },<br>  "Advanced Event": {<br>      "prefix": ["event", "advanced event"],<br>      "body": [<br>        "yournamespace.0000 = {",<br>        "\ttype = character_event",<br>        "\ttitle = stewardship_domain_special.1424.a",<br>        "\tdesc = stewardship_domain_special.1424.a",<br>        "",<br>        "\ttheme = mental_break",<br>        "\toverride_background = { reference = throne_room }",<br>        "\tleft_portrait = {",<br>        "\t\tcharacter = root",<br>        "\t\tanimation = idle",<br>        "\t}",<br>        "\tright_portrait = {",<br>        "\t\tcharacter = root",<br>        "\t\tanimation = idle",<br>        "\t}",<br>        "",<br>        "\tcooldown = { years = 5 }",<br>        "",<br>        "\ttrigger = {",<br>        "",<br>        "\t}",<br>        "",<br>        "\timmediate = {",<br>        "",<br>        "\t}",<br>        "",<br>        "\toption = {",<br>        "\t\tname = stewardship_domain_special.1424.a",<br>        "",<br>        "\t\ttrigger = {",<br>        "",<br>        "\t\t}",<br>        "",<br>        "\t\tai_chance = {",<br>        "\t\t\tbase = 50",<br>        "\t\t\tmodifier = {",<br>        "\t\t\t\tadd = 25",<br>        "\t\t\t\talways = yes",<br>        "\t\t\t}",<br>        "",<br>        "\t\t\tai_value_modifier = {",<br>        "\t\t\t\tai_boldness = 0.5",<br>        "\t\t\t\tai_compassion = 0.5",<br>        "\t\t\t\tai_greed = 0.5",<br>        "\t\t\t\tai_energy = 0.5",<br>        "\t\t\t\tai_honor = 0.5",<br>        "\t\t\t\tai_rationality = 0.5",<br>        "\t\t\t\tai_sociability = 0.5",<br>        "\t\t\t\tai_vengefulness = 0.5",<br>        "\t\t\t\tai_zeal = 0.5",<br>        "\t\t\t}",<br>        "\t\t}",<br>        "\t}",<br>        "}"<br>        ],<br>      "description": "An advanced event template containing everything a content designer could desire."<br>  },<br>  "Generate Character": {<br>      "prefix": ["create character", "character", "generate character"],<br>      "body": [<br>        "create_character = {",<br>        "\tage = { 20 32 }",<br>        "\tlocation = root.capital_province",<br>        "\tgender_female_chance = root_faith_dominant_gender_female_chance",<br>        "\tculture = root.culture",<br>        "\tfaith = root.faith",<br>        "\trandom_traits = yes",<br>        "\ttrait = blind",<br>        "\tmartial = { 3 10 }",<br>        "",<br>        "\tdynasty = none",<br>        "\tafter_creation = { ",<br>        "\t\tadd_gold = { minor_gold_value medium_gold_value }",<br>        "\t\tadd_prestige = { minor_prestige_gain medium_prestige_gain }",<br>        "\t\tadd_piety = { minor_piety_gain medium_piety_gain }",<br>        "\t}",<br>        "",<br>        "\tsave_scope_as = generated_actor",<br>        "}"<br>        ],<br>      "description": "Runtime character generation for event usage."<br>  },<br>  "Random Chance": {<br>      "prefix": ["random"],<br>      "body": [<br>          "random = {",<br>          "\tchance = 25",<br>          "\tadd_trait = Typhus",<br>          "}"<br>        ],<br>      "description": "A random chance for something to happen. Can use weights."<br>  },<br>  "Random List": {<br>      "prefix": ["list", "random list"],<br>      "body": [<br>          "random_list = {",<br>          "\t50 = { add_gold = 25 }",<br>          "\t50 = { add_gold = 500 }",<br>          "}"<br>        ],<br>      "description": "A list of possibilities. One will always be picked, can use weights and triggers."<br>  },<br>  "Banner Notification": {<br>      "prefix": ["notification", "toast", "interface", "banner notification", "send_interface_toast"],<br>      "body": [<br>          "send_interface_toast = {",<br>          "\ttype = event_toast_effect_bad",<br>          "\ttitle = stress_threshold_prison.1041.t",<br>          "\tleft_icon = ROOT",<br>          "",<br>          "\tadd_stewardship_lifestyle_xp = minor_lifestyle_experience",<br>          "\tadd_piety = -15",<br>          "}"<br>        ],<br>      "description": "An interface element displayed at the top of the screen."<br>  },<br>  "Message Notification": {<br>      "prefix": ["notification", "message", "interface", "message notification", "send_interface_message"],<br>      "body": [<br>          "send_interface_message = {",<br>          "\ttype = event_stewardship_neutral",<br>          "\ttitle = hold_court.6180.t",<br>          "\tleft_icon = scope:client",<br>          "\tright_icon = ROOT",<br>          "",<br>          "\tadd_gold = 50",<br>          "}"<br>        ],<br>      "description": "An interface element displayed in the corner of the screen."<br>  },<br>  "Triggered Animation": {<br>      "prefix": ["triggered animation", "animation"],<br>      "body": [<br>          "triggered_animation = {",<br>          "\ttrigger = { always = yes }",<br>          "\tanimation = beg",<br>          "}"<br>        ],<br>      "description": "Allows you to make conditional animations, works as a first_valid."<br>  },<br>  "Desc Jenga": {<br>      "prefix": ["Desc Jenga"],<br>      "body": [<br>        "desc = { # Desc Jenga!",<br>        "\ttriggered_desc = {",<br>        "\t\ttrigger = { always = yes }",<br>        "\t\tdesc = {",<br>        "\t\t\tdesc = stress_threshold.3201.depressed.gain",<br>        "\t\t\tdesc = {",<br>        "\t\t\t\tfirst_valid = {",<br>        "\t\t\t\t\ttriggered_desc = {",<br>        "\t\t\t\t\t\ttrigger = { always = yes }",<br>        "\t\t\t\t\t\tdesc = stress_threshold.3201.depressed.effect",<br>        "\t\t\t\t\t}",<br>        "\t\t\t\t\ttriggered_desc = {",<br>        "\t\t\t\t\t\ttrigger = { always = no }",<br>        "\t\t\t\t\t\tdesc = stress_threshold_prison.1041.flagellant",<br>        "\t\t\t\t\t}",<br>        "\t\t\t\t\tdesc = court_maintenance.0010.b.paranoid",<br>        "\t\t\t\t}",<br>        "\t\t\t}",<br>        "\t\t}",<br>        "\t}",<br>        "}"<br>        ],<br>      "description": "Prints every desc command for use in scripted loc."<br>  },<br>  "Script Header List": {<br>    "prefix": ["script header list", "header", "index"],<br>    "body": [<br>      "### EVENT LIST ####################################################################",<br>      "## XXXX - XXXX\tEvent Name Here by Author Name Here",<br>      "## XXXX - XXXX\tEvent Name Here by Author Name Here",<br>      "## XXXX - XXXX\tEvent Name Here by Author Name Here",<br>      "## XXXX - XXXX\tEvent Name Here by Author Name Here",<br>      "## XXXX - XXXX\tEvent Name Here by Author Name Here",<br>      "## XXXX - XXXX\tEvent Name Here by Author Name Here",<br>      "## XXXX - XXXX\tEvent Name Here by Author Name Here",<br>      "###################################################################################"<br>    ],<br>    "description": "A list containing all events on a script file, useful for organization."<br>  },<br>  "Event Header": {<br>    "prefix": ["event header", "header"],<br>    "body": [<br>      "###################################",<br>      "# Your event title here",<br>      "# By Your name here",<br>      "###################################"<br>    ],<br>    "description": "A header comment for scripts, containing name and author."<br>  },<br>  "Decision": {<br>    "prefix": ["decision"],<br>    "body": [<br>      "the_name_of_your_decision = {",<br>      "\tpicture = \"gfx/interface/illustrations/decisions/decision_destiny_goal.dds\"",<br>      "\tdesc = secure_iberian_foothold_decision_desc",<br>      "\tsort_order = 100",<br>      "\tmajor = no",<br>      "",<br>      "\tis_shown = {",<br>      "",<br>      "\t}",<br>      "",<br>      "\tis_valid = {",<br>      "\t\t",<br>      "\t}",<br>      "",<br>      "\teffect = {",<br>      "\t\t",<br>      "\t}",<br>      "",<br>      "\tcost = {",<br>      "",<br>      "\t}",<br>      "",<br>      "\tai_check_interval = 32",<br>      "\tai_potential = {}",<br>      "\tai_will_do = {",<br>      "\t\tbase = 100",<br>      "\t}",<br>      "}"<br>  ],<br>    "description": "Simple decision template."<br>  },<br>  "Interaction": {<br>    "prefix": ["interaction"],<br>    "body": [<br>      "your_interaction_name_here_interaction = {",<br>      "\ticon = debug_bad",<br>      "\tcategory = interaction_category_diplomacy",<br>      "\tcommon_interaction = yes",<br>      "",<br>      "\tinterface_priority = 200",<br>      "\tdesc = steward_task.1101.notification",<br>      "\t",<br>      "\tai_targets = {",<br>      "",<br>      "\t}",<br>      "\tai_target_quick_trigger = {",<br>      "\t\tadult = yes",<br>      "\t}",<br>      "\tai_frequency = 24",<br>      "\t",<br>      "\tcooldown_against_recipient = { years = 3 } # Very optional",<br>      "",<br>      "\tis_shown = {",<br>      "",<br>      "\t}",<br>      "",<br>      "\tis_valid_showing_failures_only = {",<br>      "",<br>      "\t}",<br>      "\t",<br>      "\tai_min_reply_days = 1",<br>      "\tai_max_reply_days = 5",<br>      "\tai_accept = {",<br>      "\t\tbase = 0",<br>      "\t}",<br>      "\t",<br>      "\tauto_accept = {",<br>      "\t\tcustom_description = {",<br>      "\t\t\ttext = \"spending_hook\"",<br>      "\t\t\tsubject = scope:actor",<br>      "\t\t\tobject = scope:recipient",<br>      "\t\t\tscope:hook = yes",<br>      "\t\t}",<br>      "\t}",<br>      "\t",<br>      "\tsend_options_exclusive = no",<br>      "\tsend_option = {",<br>      "\t\tis_shown = {",<br>      "\t\t\tNOT = { scope:actor = scope:recipient }",<br>      "\t\t}",<br>      "\t\tis_valid = {",<br>      "\t\t\tscope:actor = {",<br>      "\t\t\t\thas_usable_hook = scope:recipient",<br>      "\t\t\t}",<br>      "\t\t}",<br>      "\t\tflag = hook",<br>      "\t\tlocalization = GENERIC_SPEND_A_HOOK",<br>      "\t}",<br>      "\tshould_use_extra_icon = {",<br>      "\t\tscope:actor = { has_usable_hook = scope:recipient }",<br>      "\t}",<br>      "\textra_icon = \"gfx/interface/icons/character_interactions/hook_icon.dds\"",<br>      "\t",<br>      "\ton_accept = {",<br>      "",<br>      "\t}",<br>      "",<br>      "\ton_decline = {",<br>      "",<br>      "\t}",<br>      "\t",<br>      "\tai_potential = {",<br>      "",<br>      "\t}",<br>      "",<br>      "\tai_will_do = {",<br>      "\t\tbase = 0",<br>      "\t}",<br>      "}"<br>    ],<br>    "description": "Simple interaction template."<br>  },<br>  "AI Weights": {<br>    "prefix": ["ai weights", "weights"],<br>    "body": [<br>        "ai_value_modifier = {",<br>        "\tai_boldness = 0.5",<br>        "\tai_compassion = 0.5",<br>        "\tai_greed = 0.5",<br>        "\tai_energy = 0.5",<br>        "\tai_honor = 0.5",<br>        "\tai_rationality = 0.5",<br>        "\tai_sociability = 0.5",<br>        "\tai_vengefulness = 0.5",<br>        "\tai_zeal = 0.5",<br>        "}"<br>      ],<br>    "description": "Component with all AI weights for event options."<br>  },<br>  "Valid Combatant Trigger": {<br>    "prefix": ["valid combatant trigger"],<br>    "body": ["can_be_combatant_based_on_gender_trigger = { ARMY_OWNER = liege }"],<br>    "description": "Trigger component used to check if a character can be an active combatant."<br>  },<br>  "Letter Event": {<br>    "prefix": ["letter event", "event"],<br>    "body": [<br>      "yournamespace.0000 = {",<br>      "\ttype = letter_event",<br>      "\tsender = root",<br>      "\topening = court_amenities_interactions.0001.a",<br>      "\tdesc = yearly.1040.a",<br>      "",<br>      "\timmediate = {",<br>      "",<br>      "\t}",<br>      "",<br>      "\toption = {",<br>      "\t\tname = trait_specific.8501.d",<br>      "\t}",<br>      "}"<br>    ],<br>    "description": "Creates a barebones letter event, for usage when two characters interact."<br>  },<br>  "Struggle Event": {<br>    "prefix": ["struggle event"],<br>    "body": [<br>      "DLC_struggle.0000 = {",<br>      "\ttype = fullscreen_event",<br>      "\ttitle = bp1_yearly.5722.t",<br>      "\tdesc = bp1_yearly.5719.a",<br>      "\ttheme = realm",<br>      "\toverride_background = { reference = fp2_fullscreen_intro }",<br>      "\toverride_sound = { reference = \"event:/DLC/FP2/SFX/UI/fp2_struggle_ui_intro_animate\" }",<br>      "",<br>      "\twidgets = {",<br>      "\t\twidget = {",<br>      "\t\t\tgui = \"event_window_widget_struggle_info\"",<br>      "\t\t\tcontainer = \"dynamic_content_widget\"",<br>      "\t\t\tcontroller = struggle_info",<br>      "\t\t\tsetup_scope = { struggle:YOUR_STRUGGLE_HERE = { save_scope_as = struggle } }",<br>      "\t\t}",<br>      "\t}",<br>      "",<br>      "\timmediate = {",<br>      "",<br>      "\t}",<br>      "",<br>      "\toption = {",<br>      "\t\tname = dynn_Hardegg",<br>      "\t\tclicksound = \"event:/DLC/FP2/SFX/UI/fp2_struggle_start_select\"",<br>      "\t}",<br>      "}"<br>    ],<br>    "description": "Full-screen event used for struggles (intros, endings, etc)."<br>  },<br>  "Stress Impact": {<br>    "prefix": "stress impact",<br>    "body": [<br>        "stress_impact = {",<br>        "\twrathful = major_stress_impact_gain",<br>        "\tcompassionate = medium_stress_impact_gain",<br>        "\tlifestyle_gardener = minor_stress_impact_loss",<br>        "}"<br>    ],<br>    "description": "stress impact with examples, good for options."<br>  },<br>  "Add Opinion": {<br>    "prefix": ["add opinion", "opinion modifier"],<br>    "body": [<br>        "add_opinion = {",<br>        "\ttarget = scope:count_reinhard_von_lohengramm",<br>        "\tmodifier = rebellious_vassal_opinion",<br>        "\topinion = 25",<br>        "\tyears = 10",<br>        "}"<br>    ],<br>    "description": "pre-filled opinion effect for affecting the opinion of the scope character towards the scoped character."<br>  }<br>}<br>``` |

### Sublime Text\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Event_modding&veaction=edit&section=3 "Edit section: Sublime Text") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Event_modding&action=edit&section=3 "Edit section: Sublime Text")\]

[Sublime Text](https://www.sublimetext.com/) is a popular choice amongst many because it excels at handling localization files. This is a free software.

### Notepad++\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Event_modding&veaction=edit&section=4 "Edit section: Notepad++") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Event_modding&action=edit&section=4 "Edit section: Notepad++")\]

[Notepad++](https://notepad-plus-plus.org/) is a direct update over using regular notepad for scripting, if the two options above seem too daunting, you can start here.

## Location\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Event_modding&veaction=edit&section=5 "Edit section: Location") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Event_modding&action=edit&section=5 "Edit section: Location")\]

Events belong in a .txt file inside the `events` directory directly below your [root mod folder](https://ck3.paradoxwikis.com/Mod_structure#Mod_folder "Mod structure"). Each file can hold as many events as one would like. The `events` directory may also have sub-folders containing their own event files, if one prefers.

## Structure\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Event_modding&veaction=edit&section=6 "Edit section: Structure") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Event_modding&action=edit&section=6 "Edit section: Structure")\]

The overall structure is similar to that of a [CK2 event](https://ck2.paradoxwikis.com/Event_modding "ckii:Event modding"), with some tweaks to the syntax and a whole lot of extra features, many of them optional. The barest possible event is laid out here, and each element is described individually in a later section.

```
namespace = example
example.1 = {
	desc = example.1.desc

	option = {
		name = example.1.a
	}
}
```

There you go! Add this to your mod, trigger it from the in-game console using "event example.1", and you have got yourself a working event! Everything else is optional, but necessary to really flesh out the events. This is as bare-bones as it gets.
Here is an example of a more fleshed out event, containing only the basics:

```
## This a basic event, use it as a base for other events. Though you probably will want to remove the annotation spam first.
superexample.1337 = { # Use comments (like this one!) to put the event name here, this way other scripters can find the event you are working on without knowing the ID.
	type = character_event
	title = "A Modding Example Worthy of Kings" # Protip: you can use strings and later replace it with loc refs later
	desc = birth.1003.b # For Sublime users: there is a "find in files" feature that is excellent for digging through loc

	theme = mental_break
	left_portrait = root

	option = { # Use comments to state what the option says or does (eg "No, I denounce you heretic!" or "Engage in duel against child"), much like with event titles, it's good practice.
		name = stewardship_domain_special.1424.a
	}
}
```

### ID and namespace\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Event_modding&veaction=edit&section=7 "Edit section: ID and namespace") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Event_modding&action=edit&section=7 "Edit section: ID and namespace")\]

Namespaces can be any alphanumeric string (without the '.' character), and are used as prefix in the form `<namespace>.<id>`. The ID uniquely identifies your event.

If an event file uses a namespace, it has to be declared at the beginning of the file with `namespace = <namespace>`. This has to be done for every file the namespace is used in.

Notice that if the ID exceeds 9999, the event calling system will become buggy, so please consider the max allowed ID for a given namespace as 9999.

### Flags\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Event_modding&veaction=edit&section=8 "Edit section: Flags") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Event_modding&action=edit&section=8 "Edit section: Flags")\]

These are top-level variables that determine your event's kind and appearance. They have a limited set of values.

| Flag | Meaning | Possible values |
| --- | --- | --- |
| type | The kind of event. It determines what sort of scope the root is. | - character\_event<br>- letter\_event<br>- duel\_event<br>- none (when an event doesn't use the root scope at all)<br>- empty (necessary for characterless events to trigger. NOTE: this means typing type = empty ) |
| hidden | Set this to true, and the event will not be shown at all; it will happen in the background. Useful for doing maintenance events that are not immediately relevant to the player. | true, false |

## Portraits\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Event_modding&veaction=edit&section=9 "Edit section: Portraits") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Event_modding&action=edit&section=9 "Edit section: Portraits")\]

In Crusader Kings III, portraits are now in 3D, and can now be animated as well! What follows is a list of the different portrait positions, as well as a list of animations for them.

### Portrait Positions\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Event_modding&veaction=edit&section=10 "Edit section: Portrait Positions") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Event_modding&action=edit&section=10 "Edit section: Portrait Positions")\]

[![](https://ck3.paradoxwikis.com/images/thumb/2/2a/Example_event.png/300px-Example_event.png)](https://ck3.paradoxwikis.com/File:Example_event.png)

[Enlarge](https://ck3.paradoxwikis.com/File:Example_event.png "Enlarge")

Portrait Positions

| Portrait Position | Description |
| --- | --- |
| left\_portrait | Shown on the left side of the event scene. |
| right\_portrait | Shown on the right side of the event scene. |
| lower\_left\_portrait | Shown on the lower left part of the event scene. |
| lower\_center\_portrait | Shown on the lower center part of the event scene. |
| lower\_right\_portrait | Shown on the lower right part of the event scene. |

Here is an example of all of the portrait positions in use at the same time, along with a screenshot:

```
example_event.1001 = {
	left_portrait = {
		character = ROOT # Whoever this is scoped to will show up in this event window position, exhibiting the chosen animation.
		animation = fear # Take note that characters with SOME genetic traits (for example, gigantism, dwarfism) that change their character models have different animations, and if you assign one of THOSE animations to a character that does not have that model, crashes may occur.
	}
	right_portrait = {
		character = ROOT
		animation = scheme
	}
	lower_left_portrait = {
		character = ROOT
	}
	lower_center_portrait = {
		character = ROOT
	}
	lower_right_portrait = {
		character = ROOT
	}
}
```

Portraits can take the following parameters:

| Parameter | Description | Example |
| --- | --- | --- |
| character | The character whose portrait is shown. | `character = scope:event_target` |
| animation | The animation that will play | `animation = anger` |
| triggered\_animation | Plays a certain animation if the triggers are met. If not, will default to animation set with `animation =` | ```<br>triggered_animation = {<br>	trigger = {}<br>	animation = fear<br>}<br>``` |
| triggered\_outfit | Set an outfit for use in this event. [(Additional Information on outfit\_tags)](https://ck3.paradoxwikis.com/Characters_modding#Outfit_Tags) | ```<br>triggered_outfit = {<br>	trigger = {}<br>	outfit_tags = no_clothes (also accepts multiple tags, in the format outfit_tags = { tag1 tag2 }<br>	remove_default_outfit = yes/no<br>}<br>``` |
| hide\_info | Prevents the game from showing any info on the character (tooltip, COA, clicks, etc). Only the portrait will be shown. | `hide_info = yes/no` |

### Animations\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Event_modding&veaction=edit&section=11 "Edit section: Animations") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Event_modding&action=edit&section=11 "Edit section: Animations")\]

| Event-Compatible Animation IDs |
| --- |
| idle | chancellor | steward | marshal | spymaster | chaplain |
| anger | rage | disapproval | disbelief | disgust | fear |
| sadness | shame | shock | worry | boredom | grief |
| paranoia | dismissal | flirtation | flirtation\_left | love | schadenfreude |
| stress | happiness | ecstasy | admiration | lunatic | scheme |
| beg | pain | poison | aggressive\_axe | aggressive\_mace | aggressive\_sword |
| aggressive\_dagger | aggressive\_spear | aggressive\_hammer | celebrate\_axe | celebrate\_mace | celebrate\_sword |
| celebrate\_dagger | celebrate\_spear | celebrate\_hammer | loss\_1 | chess\_certain\_win | chess\_cocky |
| laugh | lantern | eyeroll | eavesdrop | assassin | toast |
| toast\_goblet | drink | drink\_goblet | newborn | sick | severelywounded |
| prisonhouse | prisondungeon | war\_attacker | war\_defender | war\_over\_tie | war\_over\_win |
| war\_over\_loss | pregnant | personality\_honorable | personality\_dishonorable | personality\_bold | personality\_coward |
| personality\_greedy | personality\_content | personality\_vengeful | personality\_forgiving | personality\_rational | personality\_irrational |
| personality\_compassionate | personality\_callous | personality\_zealous | personality\_cynical | frontend\_center\_idle | frontend\_left\_idle |
| frontend\_right\_idle | throne\_room\_chancellor | throne\_room\_kneel\_1 | throne\_room\_kneel\_2 | throne\_room\_curtsey\_1 | throne\_room\_messenger\_1 |
| throne\_room\_messenger\_2 | throne\_room\_messenger\_3 | throne\_room\_conversation\_1 | throne\_room\_conversation\_2 | throne\_room\_conversation\_3 | throne\_room\_conversation\_4 |
| throne\_room\_cheer\_1 | throne\_room\_cheer\_2 | throne\_room\_applaud\_1 | throne\_room\_bow\_1 | throne\_room\_bow\_2 | throne\_room\_bow\_3 |
| throne\_room\_one\_handed\_passive\_1 | throne\_room\_one\_handed\_passive\_2 | throne\_room\_two\_handed\_passive\_1 | throne\_room\_writer | test\_case\_1 | holding\_staff |
| marshal\_random\_weapon | crying | delirium | disappointed | eccentric | manic |
| marshal\_axe | interested | interested\_left | stunned | wailing | wedding\_happy\_cry |
| marshal\_dagger | peekaboo | child\_hobby\_horse | clutching\_toy | clutching\_ball | clutching\_doll |
| marshal\_mace | go\_to\_your\_room | cough | shiver | sick\_stomach | loss\_1 |
| marshal\_shield | page\_flipping | writing | reading | stressed\_teacher | happy\_teacher |
| thinking | emotion\_thinking\_scepter | wedding\_drunk | acknowledging | betting | bribing |
| chess\_certain\_win | chess\_cocky | dancing | dancing\_plague | debating | hero\_flex |
| obsequious\_bow | physician | prayer | scepter | stayback | storyteller |
| survey | aggressive\_axe | aggressive\_mace | aggressive\_sword | aggressive\_dagger | aggressive\_spear |
| aggressive\_hammer | aggressive\_unarmed | celebrate\_axe | celebrate\_mace | celebrate\_sword | celebrate\_dagger |
| celebrate\_spear | celebrate\_hammer | sword\_coup\_degrace | wrestling\_victory | sword\_yield\_start | wrestling\_yield\_start |
| wooden\_sword\_yield\_start | throne\_room\_wooden\_sword | celebrate\_wooden\_sword | aggressive\_wooden\_sword | marshal\_wooden\_sword | wooden\_sword\_coup\_degrace |
| random\_weapon\_coup\_degrace | random\_weapon\_aggressive | random\_weapon\_celebrate | random\_weapon\_yield | inspect\_weapon | menacing |
| threatening | throne\_room\_ruler | throne\_room\_ruler\_2 | throne\_room\_ruler\_3 | throne\_room\_two\_handed\_passive\_shield | crossbow |
| bow\_idle | hunting\_shortbow\_rest\_arrow\_default | hunting\_shortbow\_rest\_bluntarrow\_default | hunting\_shortbow\_aim\_arrow\_default | hunting\_shortbow\_aim\_bluntarrow\_default | hunting\_longbow\_rest\_arrow\_default |
| hunting\_longbow\_rest\_bluntarrow\_default | hunting\_longbow\_aim\_arrow\_default | hunting\_longbow\_aim\_bluntarrow\_default | hunting\_horn | hunting\_carcass\_start | hunting\_knife\_start |
| hunting\_falcon | jockey\_lance\_tilted | jockey\_lance\_couched\_gallop | jockey\_gallop | jockey\_idle | jockey\_victory |
| jockey\_loss | jockey\_walk | jockey\_wave | chariot\_neutral | chariot\_happy | chariot\_shocked |
| chariot\_w\_horses\_neutral | chariot\_w\_horses\_happy | chariot\_w\_horses\_shocked | wedding\_groom\_right | wedding\_bride\_left | wedding\_priest |
| reception\_groom\_left | reception\_bride\_right | wedding\_objection\_start | instrument\_active | instrument\_idle | shawm\_active |
| shawm\_idle | qanun\_active | qanun\_idle | lute\_active | lute\_idle | chifonie\_active |
| chifonie\_idle | alto\_flute\_active | alto\_flute\_idle | incapable | dead | survey\_staff |

## Themes\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Event_modding&veaction=edit&section=12 "Edit section: Themes") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Event_modding&action=edit&section=12 "Edit section: Themes")\]

A Theme is a collection of background, lighting environment for character portraits, and sound effects. They are declared in common/event\_themes/.

| Theme |
| --- |
| abduct\_scheme | alliance | bastardy | battle |
| befriend\_scheme | claim\_throne\_scheme | corruption | crown |
| culture\_change | death | default | diplomacy |
| diplomacy\_family\_focus | diplomacy\_foreign\_affairs\_focus | diplomacy\_majesty\_focus | dread |
| dungeon | dynasty | education | fabricate\_hook\_scheme |
| faith | family | feast\_activity | friend\_relation |
| friendly | generic\_intrigue\_scheme | healthcare | hunt\_activity |
| hunting | intrigue | intrigue\_intimidation\_focus | intrigue\_skulduggery\_focus |
| intrigue\_temptation\_focus | learning | learning\_medicine\_focus | learning\_scholarship\_focus |
| learning\_theology\_focus | love | lover\_relation | marriage |
| martial | martial\_authority\_focus | martial\_chivalry\_focus | martial\_strategy\_focus |
| medicine | mental\_break | mental\_health | murder\_scheme |
| party | pet | physical\_health | pilgrimage\_activity |
| pregnancy | prison | realm | recovery |
| rival\_relation | romance\_scheme | secret | seduce\_scheme |
| seduction | skull | stewardship | stewardship\_domain\_focus |
| stewardship\_duty\_focus | stewardship\_wealth\_focus | sway\_scheme | unfriendly |
| vassal | war | witchcraft |

Individual elements of the theme can be overridden using `override_background`, `override_icon`, `override_sound`, and `override_environment`.

#### Backgrounds\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Event_modding&veaction=edit&section=13 "Edit section: Backgrounds") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Event_modding&action=edit&section=13 "Edit section: Backgrounds")\]

| Background |
| --- |
| alley\_day | alley\_night | armory | army\_camp |
| battlefield | bedchamber | burning\_building | corridor\_day |
| corridor\_night | council\_chamber | courtyard | docks |
| dungeon | farmland | feast | gallows |
| garden | market | market\_east | market\_india |
| market\_tribal | market\_west | physicians\_study | sitting\_room |
| study | tavern | temple | temple\_church |
| temple\_generic | temple\_mosque | temple\_scope | terrain |
| terrain\_activity | terrain\_scope | throne\_room | throne\_room\_east |
| throne\_room\_india | throne\_room\_mediterranean | throne\_room\_scope | throne\_room\_tribal |
| throne\_room\_west | wilderness | wilderness\_desert | wilderness\_forest |
| wilderness\_forest\_pine | wilderness\_mountains | wilderness\_scope | wilderness\_steppe |

### Environments\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Event_modding&veaction=edit&section=14 "Edit section: Environments") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Event_modding&action=edit&section=14 "Edit section: Environments")\]

When you've selected a background, the appropriate environment is automatically selected. Only overwrite it when necessary.

| Environment |
| --- |
| environment\_body | environment\_council | environment\_cw\_east\_main |
| environment\_cw\_east\_spouse | environment\_cw\_east\_throneroom\_main | environment\_cw\_east\_throneroom\_spouse |
| environment\_cw\_india\_main | environment\_cw\_india\_spouse | environment\_cw\_india\_throneroom\_main |
| environment\_cw\_india\_throneroom\_spouse | environment\_cw\_mediterranean\_main | environment\_cw\_mediterranean\_spouse |
| environment\_cw\_mediterranean\_throneroom\_main | environment\_cw\_mediterranean\_throneroom\_spouse | environment\_cw\_tavern |
| environment\_cw\_tavern\_spouse | environment\_cw\_tribal\_main | environment\_cw\_tribal\_spouse |
| environment\_cw\_west | environment\_cw\_west\_spouse | environment\_event\_alley |
| environment\_event\_alley\_day | environment\_event\_armory | environment\_event\_battlefield |
| environment\_event\_bedchamber | environment\_event\_church | environment\_event\_corridor\_day |
| environment\_event\_courtyard | environment\_event\_desert | environment\_event\_docks |
| environment\_event\_dungeon | environment\_event\_farms | environment\_event\_feast |
| environment\_event\_forest | environment\_event\_forest\_pine | environment\_event\_gallows |
| environment\_event\_garden | environment\_event\_genericcamp | environment\_event\_market\_east |
| environment\_event\_market\_tribal | environment\_event\_market\_west | environment\_event\_mosque |
| environment\_event\_mountains | environment\_event\_sittingroom | environment\_event\_standard |
| environment\_event\_steppe | environment\_event\_study | environment\_event\_study\_physician |
| environment\_event\_tavern | environment\_event\_temple | environment\_event\_throne\_room\_west |
| environment\_frontend\_east\_heir | environment\_frontend\_east\_main | environment\_frontend\_east\_secondary |
| environment\_frontend\_india\_heir | environment\_frontend\_india\_main | environment\_frontend\_india\_secondary |
| environment\_frontend\_mediterranean\_heir | environment\_frontend\_mediterranean\_main | environment\_frontend\_mediterranean\_secondary |
| environment\_frontend\_tribal\_heir | environment\_frontend\_tribal\_main | environment\_frontend\_tribal\_secondary |
| environment\_frontend\_west\_heir | environment\_frontend\_west\_main | environment\_frontend\_west\_secondary |
| environment\_head | environment\_hud | environment\_portrait\_editor |
| environment\_shoulders | environment\_standard | environment\_torso |
| environment\_war\_overview |  |

## Trigger\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Event_modding&veaction=edit&section=15 "Edit section: Trigger") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Event_modding&action=edit&section=15 "Edit section: Trigger")\]

This is an additional requirement for an event to work.

```
trigger = { # This is the set of requirements necessary for this event to enable (a gigant IF statement for the event itself)
	culture = {
		has_innovation = innovation_guilds # Checks if you have unlocked guilds on your cultural research
	}
}
```

You can also lock certain requirements in a trigger behind a trigger of their own, using `trigger_if`.

The requirements inside of the `trigger_if` will only be checked if the contents of the `limit` block are true. Optionally, you can add a `trigger_else` afterwards to check alternative requirements if the `trigger_if` fails.

```
trigger = {
	any_held_county = { # We check that we have a blacksmith
		any_county_province = {
			has_building_or_higher = blacksmiths_01
		}
	}

	trigger_if = { # If our character is greedy, then we add the requirement to have 500 gold
		limit = { has_trait = greedy }
		gold > 500
	}
	trigger_else = { # Otherwise, you must have at least 50 piety and 10 gold
		piety > 50
        gold > 10
	}
}
```

The trigger is checked before the event fires, which means that you cannot use any of the scopes created in the [Immediate block](https://ck3.paradoxwikis.com/Event_modding#Immediate "Event modding") when checking if certain characters meet triggers. For example, if you wanted to create an event where you wanted to know if a knight had the brave trait, you could not create a scope called `scope:knight` in the immediate block and then check that same scope in the trigger. Instead, to check if a character could meet the triggers for your event, you probably want to use a list builder.

```
trigger = {
    any_knight = { # Will look at all knights of the root character to see if any match the triggers
        has_trait = brave
    }
}
```

### on\_trigger\_fail\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Event_modding&veaction=edit&section=16 "Edit section: on trigger fail") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Event_modding&action=edit&section=16 "Edit section: on trigger fail")\]

Runs when the trigger fails.

## Description\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Event_modding&veaction=edit&section=17 "Edit section: Description") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Event_modding&action=edit&section=17 "Edit section: Description")\]

Text that is going to show up in the event window can include the event's title, description, option names, and option flavor text. To write a description for an event, you can either write out literal text in the event file, or you can refer the description to a localization key which is stored in the `your_mod\localization\english\` folder (where english can be replaced by the language of the localization key for your mod). In the vanilla files, localization keys are stored in a subfolder of `localization\english` called `event_localization`, but the game can read any localization key stored in the language folder.

```
my_event.0001 = {
    title = "The Event's Title" # Literal text which will show up in game exactly as displayed here
    desc = my_event.0001.desc # A localization key to be defined in your_mod\localization\english
    # ...
}
```

It can be useful to write literal text when in the early stages of writing an event, but it is generally not advised to use literal text in your mod as it produces an error in the error.log, and it prevents you from using the powerful data context tools that allow you to reactively write out a character's name, pronouns, etc. based on which characters are getting the event. See [Localization](https://ck3.paradoxwikis.com/Localization "Localization") for more information on how to use these data types.
To make your descriptions even more reactive, you can also write out branching and complicated `desc` entries to account for different factors when the event fires. For example, you could write out different `desc` blocks to be displayed depending on the traits of the character who is getting the event. You can do this by using `first_valid` and `random_valid` inside of your `desc` entry.

```
desc = {
    first_valid = { # Display the localization of the first valid desc block which returns true
        triggered_desc = {
            trigger = {
                has_trait = drunkard
            }
            desc = my_event.0001.desc.drunkard # An loc key to display if the trigger is true
        }
        desc = my_event.0001.desc.fallback # Another loc key to display if nothing before it is valid to display
    }
    random_valid = { # Will display a random localization key, picking from any loc keys for which the triggers return true
        desc = my_event.0001.random_1
        desc = my_event.0001.random_2
        desc = my_event.0001.random_3
        triggered_desc = {
            trigger = {
                is_female = yes
            }
            desc = my_event.0001.random_4
        }
    }
}
```

`first_valid` will pick the first `desc` block inside of it which is valid (i.e., its triggers are true). If you want to set specific triggers, you can do so by using a `triggered_desc` block, which requires a trigger and a `desc` that it should display if this description is chosen. If you write in a `desc` block instead of a `triggered_desc` block, then its triggers will always be considered true, and it will always be a valid choice to display. This means that if you use a `first_valid` block and put a `desc` before a `triggered_desc` block, the `desc` will always display.

`random_valid` is similar to `first_valid`, but instead of picking the first `desc` which returns true, it will pick a random description that has true triggers. In this case, you can put the `triggered_desc` and `desc` keys in any order, as the choice will be randomized. Like with `first_valid`, a key that is simply `desc` will always be considered a valid choice for the random selection.

You can also combine `first_valid` and `random_valid` to make a more curated randomization for your description.

```
desc = {
    first_valid = { # Pick the first desc block that returns true
        triggered_desc = { # If the character has brave...
            trigger = {
                has_trait = brave
            }
            desc = { # Then randomly pick one of these
                random_valid = {
                    desc = my_event.0001.brave.random_1
                    desc = my_event.0001.brave.random_2
                    desc = my_event.0001.brave.random_3
                }
            }
        }
        desc = { # Otherwise, if not brave, randomly pick one of these
            random_valid = {
               desc = my_event.0001.fallback.random_1
               desc = my_event.0001.fallback.random_2
               desc = my_event.0001.fallback.random_3
            }
        }
    }
}
```

You can make these descriptions quite varied and complicated by combining these together, but be aware that writing a lot of alternatives for events can be quite time consuming.
You can also combine `desc` entries by adding multiple `desc` keys outside of a `first_valid` or `random_valid` entry.

```
desc = {
    desc = { # Only display the opening if the character has the blind trait
        first_valid = {
            triggered_desc = {
                trigger = {
                    has_trait = eccentric
                }
                desc = "Many people have said, because of my eccentricity,"
            }
        }
    desc = "I am an endless font of inspiration," # Always display the middle
    desc = { # Display a different ending depending on if the character has the pregnant trait
        first_valid = {
            triggered_desc = {
                trigger = {
                    has_trait = pregnant
                }
                desc = "and I hope that I am able to pass that on to my child."
            }
            desc = "and it feels good to be appreciated like that."
        }
    }
}
```

The above description will output as many as three separate localization keys as a single event description. If the character receiving the event is eccentric and pregnant, then the event description will read: "Many people have said, because of my eccentricity, I am an endless font of inspriation, and I hope that I am able to pass that on to my child." If the character is eccentric, but not pregnant, then it will read: "Many people have said, because of my eccentricity, I am an endless font of inspiration, and it feels good to be appreciated like that." If the character is not eccentric but is pregnant, then it will read: "I am an endless font of inspiration, and I hope that i am able to pass that on to my child." And, finally, if the character is neither eccentric nor pregnant, it will read: "I am an endless font of inspiration, and it feels good to be appreciated like that."

You can make very complex event descriptions like this, but it can take a lot of work to make sure that all of the possible variations are able to work together, so if you're going to do complciated things, you're going to want to aggressively test the various permutations of your event's description to make sure that all of them make sense.

Also note that when you combine localization strings like this, they are concatenated with a space between strings. If you write two localization keys that say "I have seen this before", and ", haven't you?", then when combined, the description will read: "I have seen this before , haven't you?" So be careful when splitting localization keys to avoid misplaced spaces. On a similar note, the developers also seem to use the en-dash instead of the em-dash for punctuating description text, as the generally accepted use of an en-dash involves a leading and trailing space, whereas an em-dash is usually abutting both characters it is between (e.g., "Hello – how are you?" vs. "Hello—how are you?"), which makes it easier to disguse where the cuts are between localization keys.

`desc` blocks can be used in various places, as well, such as in the names for options:

```
option = {
    name = {
        text = {
            first_valid = {
                triggered_desc = {
                    trigger = {
                        is_female = yes
                    }
                    desc = my_event.0001.a.female
                }
                desc = my_event.0001.a.fallback
            }
        }
    }
}
```

When it comes to options, however, you have to use a `text` block between `name` and `first_valid`, or else the description won't display properly. Alternatively, for `option` blocks, you can also do it like:

```
name = {
    trigger = { has_trait = brave }
    text = my_event.0001.a.brave
}
```

You can also use these more complex descriptions in `flavor` blocks, and for those you do not need to use the `text` block, but can just do it the same as a description block:

```
flavor = {
    first_valid = {
	triggered_desc = {
	    trigger = {
                is_female = yes
             }
	     desc = my_event.0001.a.flavor.female
	}
    desc = my_event.0001.a.flavor.fallback
    }
}
```

## Immediate\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Event_modding&veaction=edit&section=18 "Edit section: Immediate") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Event_modding&action=edit&section=18 "Edit section: Immediate")\]

This is a block of effect script: it will be ran _immediately_ as your event is triggered, before the title, description, portraits, are even evaluated let alone rendered. This block is useful for setting variables and saving scopes to use in your text or for portraits; or for functional effects that you want to happen without the player having any control over it.

"has happened" tooltip.

```
immediate = { # Stuff that happens when the event appears on screen, works regardless of what option you select.
	add_gold = 50 # adds 50 gold to the player
}
```

## Options\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Event_modding&veaction=edit&section=19 "Edit section: Options") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Event_modding&action=edit&section=19 "Edit section: Options")\]

Options within events are able to be pressed by the user. Each event may have any number of options, including none at all (a common example includes hidden events). Each option in defined in the main event block, like so:

```
example.1 = {

	# [...]

	option = {
		# option info
	}

	# [...]

}
```

A more complex example:

```
option = { # Option title
	name = stewardship_domain_special.1424.a
	trigger_event = { # Makes another event happen
		id = yearly.1012 # The event ID is the thing at the top (so stewardship_domain.6017 is valid, as is any other event, so long as it exists).
		days = { 7 14 } # Get random number between two values (unknown wether it is inclusive or exclusive), anything that takes = {X Y} can also just work as = X
	}

	hidden_effect = { # Hides stuff from showing up on the tooltip of the option
		scope:county = { # Gets the location stored in the scope "county"
			add_county_modifier = { # To add modifiers (bonuses or penalites)
				modifier = governance_land_cleared_for_settlement_modifier # https://ck3.paradoxwikis.com/Modifier_list be sure to use one that belongs to the right type (in this case, country).
				days = 3650 # How long it lasts, you can use days = {X Y} too
			}
		}
	}

	ai_chance = {
		base = 50 # What are the chances of selecting this option over others? (Does not need to be 0 to 100, it can be anything)
		modifier = {  # You can change the value based on a variety of things, in this case it is the traits of the AI character
			add = 15
			has_trait = sadistic # List of traits can be found at ..\game\common\traits\00_traits.txt
		}
		modifier = {
			add = -40 # To remove something you just add a negative number (5 + -10 = -5)
			has_trait = compassionate
		}
	}
}
```

The table below describes available keys within the `option` block:

| Key | Required | Description | Example |
| --- | --- | --- | --- |
| name | Yes | Points to a localization key for the event option button text. | name=example.1.a |
| (effects) | No | Any [effects](https://ck3.paradoxwikis.com/Effect "Effect") that the option may have can be written directly in the `option` block. | play\_music\_cue = mx\_cue\_banquet |
| trigger | No | Defines a [trigger](https://ck3.paradoxwikis.com/Trigger "Trigger") that has to be fulfilled for the option to be valid and thus available to the user. Not to be confused with the [main event trigger](https://ck3.paradoxwikis.com/Event_modding#Trigger). | ```<br>trigger = {<br>	has_trait = shy<br>}<br>``` |
| show\_as\_unavailable | No | If the option is invalid, but this trigger is, the option will be shown, but disabled. This behavior is also influenced by the EVENT\_OPTIONS\_SHOWN\_HIDE\_UNAVAILABLE define. | ```<br>show_as_unavailable = {<br>	short_term_gold < medium_gold_value<br>}<br>``` |
| trait | No | If the player has the given trait, show it on the left side of the option. Hovering over it will say the option is available because of the trait. This is only providing flavor, and does not actually affect the functionality of the option. | trait = honest |
| skill | No | Show the chosen skill on the left side of the option. Hovering over it will say the option is available because of your high skill. This is only providing flavor, and does not actually affect the functionality of the option. | skill = prowess |
| add\_internal\_flag | No | Can take the values "special" or "dangerous". The key "special" highlights the option as yellow, "dangerous" highlights the option as red. This is only providing flavor, and does not actually affect the functionality of the option. | add\_internal\_flag = special |
| highlight\_portrait | No | Highlights the event portrait of this character while this option is hovered. This is in addition to the automatic highlighting when hovering an event option that has an effect that affects portrait characters. | highlight\_portrait = scope:custom |
| fallback | No | If this is yes: if no other options meet their triggers, then this option will be shown even if its trigger is not met either. You can use this together with `trigger = { always = no }` to create an option that is only ever shown as a last resort. | fallback = yes |
| exclusive | No | If an option is marked exclusive = yes and it meets its triggers, it will be the only option shown. If multiple options are marked exclusive = yes and each meets their triggers, each will be shown. | exclusive = yes |
| flavor | No | Flavor text that is shown in the tooltip of the option. The flavor can either be a loc key or a dynamic desc with first\_valid etc. | flavor = my\_events.1001.a.flavor |

## After\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Event_modding&veaction=edit&section=20 "Edit section: After") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Event_modding&action=edit&section=20 "Edit section: After")\]

This is a block of effect script that runs after the event has ran its course and an option has been chosen. Works the exact same as the immediate block. Won't do anything if the event has no options (for hidden events, for example).

It is most commonly used for clean-up duty, removing variables, characters, and other kinds of data that are likely to persist when not intended to.

As an example, in the event `fp2_struggle.2009`, "Catching Thieves of Myth", the `after` block is used to check if we have a saved scope (used as a boolean) to decide if we should delete the event-generated character once the event is over.

```
after = {
	if = {
		limit = { NOT = { exists = scope:fp2_2009_thief_permanence_scope } } # Acts as a boolean, if this exists, then it is true
		scope:fp2_2009_garduna_young_thief = { silent_disappearance_effect = yes } # We kill (delete) the young thief, as it is no longer of use for future events
	}
}
```

## Widgets\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Event_modding&veaction=edit&section=21 "Edit section: Widgets") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Event_modding&action=edit&section=21 "Edit section: Widgets")\]

What types of widgets are there, with screenshots for each of what they look like.

## On Actions (on\_action)\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Event_modding&veaction=edit&section=22 "Edit section: On Actions (on action)") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Event_modding&action=edit&section=22 "Edit section: On Actions (on action)")\]

On Actions are scripts that execute every time a specific action is called by the game code (such as a child being born, a character inheriting land or using a hook).

This allows modders to intercept and run their own scripts whenever said On Actions are called.

They are defined in **common/on\_action**

**Important:** double-check your path. This is a singular **on\_action**, not on\_actions. This is a common mistake.

Example (trigger a custom event when a child is born):

```
on_birth_child = {
  events = {
    my_event.1
  }
}
```

See the .info file in that folder for more details. See on\_actions.log for a full list of on\_actions.

Some on\_actions are called by game code directly, while others are called by script: other on\_actions, events, decisions, etc.

For example, `on_birthday` is fired by code every birthday and tries to fire `on_birthday_adulthood`, but since it has a trigger `is_adult = yes` it will only fire when a character is an adult.

Such custom on\_actions are useful to group events or effects. We can create new custom on\_actions, we cannot create new code on\_actions.

### Common examples\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Event_modding&veaction=edit&section=23 "Edit section: Common examples") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Event_modding&action=edit&section=23 "Edit section: Common examples")\]

- `on_birth_child` \- when a child is born
- `on_16th_birthday` \- when a child becomes an adult
- `random_yearly_playable_pulse` \- once a year, at a random date, for every count+ character who is allowed to be played. Useful for rare events.
- `quarterly_playable_pulse` \- a more frequent pulse, every three months, for the same kind of characters
- `on_game_start` \- when the game starts, but before the player selects a character, so `every_player` doesn't work here
- `on_game_start_after_lobby` \- after the player has selected a character and confirmed. This is where you can affect player characters
- `on_death` \- right before a character dies. Useful to transfer any variables to the primary\_heir

Note, there is no monthly on\_action. This was done to ensure better performance.

If you _really_ need a monthly pulse, you could use quarterly\_playable\_pulse and trigger your on\_action three times with increasing delay:

```
on_actions = {
  my_on_action
  delay = { months = 1 }
  my_on_action
  delay = { months = 2 }
  my_on_action
}
```

Alternatively, have the on\_action call itself with a monthly delay.

### Appending\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Event_modding&veaction=edit&section=24 "Edit section: Appending") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Event_modding&action=edit&section=24 "Edit section: Appending")\]

Most of the time, we want to add something to on\_actions without overwriting them. We call this appending.

**Important:** effects and triggers cannot be appended directly. Only events and other on\_actions are appended.

To ensure compatibility and not overwrite vanilla effects, do the following:

1. Make a new txt file.
2. Create your own on\_action and add it to an existing on\_action:

```
on_birth_child = {
	on_actions = {
		my_on_action # custom on_action appended to on_birth_child
	}
}
my_on_action = {
	trigger = { ... } # trigger used only for this on_action
	effect = { ... } # all effects are appended safely
}
```

The example below will ovewrite vanilla effect and trigger (and any added by other mods)

```
on_birth_child = {
	trigger = { ... }
	effect = {... } # effect and trigger are overwritten, not appended
}
```

On\_actions can also be called by events and other effects like this:

`trigger_event = { on_action = my_on_action }`

### Scopes\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Event_modding&veaction=edit&section=25 "Edit section: Scopes") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Event_modding&action=edit&section=25 "Edit section: Scopes")\]

Make sure to check what scopes are available in each on\_action.

There are comments above each on\_action in their files that explain their scopes.

For example, `on_game_start` doesn't have a root scope. It fires once, globally. This means we need to use global effects, like `every_ruler`.

On the other hand, `yearly_playable_pulse` fires for all playable characters, and has the character as the root scope. So we can use character effects directly, like add\_gold.

**Important**: Do not use `every_living_character` in `yearly_playable_pulse` and similar on\_actions.

That on\_action already fires for every character. If you then try to iterate through all characters, that would result in about 200002 operations, causing massive lag and repetition of your effects.

### Properties\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Event_modding&veaction=edit&section=26 "Edit section: Properties") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Event_modding&action=edit&section=26 "Edit section: Properties")\]

This table uses contents from _/common/on\_action/on\_actions.info_ file.

| Name | Description | Expected type | Example |
| --- | --- | --- | --- |
| trigger | On\_actions can have triggers. If an on\_action fires and its trigger returns false, nothing happens | boolean | ```<br>trigger = {<br>	trigger_conditions = yes<br>}<br>``` |
| weight\_multiplier | Used to manipulate the weight of this on\_action if it is a candidate in a random\_on\_actions list (see below) | integer | ```<br>weight_multiplier = {<br>	base = 1<br>	modifier = {<br>		add = 1<br>		trigger_conditions = yes<br>	}<br>}<br>``` |
| events | Events listed in "events" brackets will always fire as long as their trigger evaluates to true |  | ```<br>events = {<br>	event_id_1<br>	delay = { days = 365 }		# A delay will mean that all events listed after it will only be fired after the delay has passed. NOTE: For performance reasons, an event will only successfully fire if it is valid both when the on_action is executed AND once the delay is complete. All firing entries support delays, whether for events or on_actions.<br>	event_id_2<br>	delay = { months = { 6 12 } }	# Setting a new delay overrides a previous delay. Delays support random ranges<br>	event_id_3<br>}<br>``` |
| random\_events | A single event will be picked to fire |  | ```<br>random_events = {	# A single event will be picked to fire<br>		<br>	chance_to_happen = 25	# A percentage chance determining whether the events involved will be evaluated at all<br>	chance_of_no_event = { 	# An entry that can be formatted as a script value (and therefore have conditional entries). Separated from "chance_to_happen" for performance reasons. Will only be evaluated if chance_to_happen is true.<br>		value = 0<br>		if = {<br>			limit = { trigger_conditions = yes }<br>			add = 10<br>		}<br>	}<br>	100 = event_id_1 	# The number is the weight for picking a specific event. The weight is factored by the event's weight_multiplier entry. (If no weight_multiplier is defined for the event, it is 1)<br>	200 = event_id_2<br>	100 = 0		# Having a "0" entry means that there is a chance no event fires, even if there are other valid events. Good for making sure that rare events don't always fire just because every other possible event is invalid.<br>}<br>``` |
| first\_valid | Pick the first event for which the trigger returns true | List<event> | ```<br>first_valid = {		# Pick the first event for which the trigger returns true<br>	event_id_1<br>	event_id_2<br>	fallback_event_without_trigger<br>}<br>``` |
| on\_actions | An on\_action can fire other on\_actions, following the same rules as with events | List<on\_action> | ```<br>on_actions = {	# An on_action can fire other on_actions, following the same rules as with events<br>	on_action_1<br>	on_action_2<br>	on_action_3<br>}<br>``` |
| random\_on\_actions | Same as with events. On\_actions are also factored by their weight\_multipliers, which defaults to 1 |  | ```<br>random_on_actions = {<br>	100 = on_action_1<br>	200 = on_action_2<br>	100 = 0<br>}<br>``` |
| first\_valid\_on\_action |  | List<on\_action> | ```<br>first_valid_on_action = {<br>	on_action_1<br>	on_action_2<br>}<br>``` |
| effect | An on\_action can run effects. It can access the same default or saved scopes as the script chain/code functionality it was fired from. Note that it happens concurrently to events triggered by the on\_action, NOT before. Effects run here create a separate chain than events the on\_action fires, so you can for example not manipulate values in the effect, and then reliably access those in an event that was fired at the same time. Scopes or local variables set in the effect here will not carry over to any event fired by the on\_action. |  | ```<br>effect = {<br>	effects = yes<br>}<br>``` |
| fallback | on\_actions can define a fallback on\_action. If no events/on\_actions are run by the on\_action, the fallback gets called instead. Avoid creating infinite fallback loops, or the game may be prevented from advancing time! | on\_action | ```<br>fallback = another_on_action<br>``` |

### On\_actions from code\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Event_modding&veaction=edit&section=27 "Edit section: On actions from code") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Event_modding&action=edit&section=27 "Edit section: On actions from code")\]

| Name | Description | From code | Expected scope | Other |
| --- | --- | --- | --- | --- |
| on\_prestige\_level\_loss |  | Yes | None |  |
| on\_rank\_down |  | Yes | None |  |
| on\_weight\_changed |  | Yes | Character |  |
| on\_faith\_monthly |  | Yes | Faith |  |
| on\_knight\_combat\_pulse |  | Yes | Character |  |
| on\_war\_invalidated |  | Yes | None |  |
| on\_war\_transferred |  | Yes | Character |  |
| on\_divorce |  | Yes | None |  |
| on\_leave\_court |  | Yes | Character |  |
| on\_guest\_ready\_to\_move\_to\_pool |  | Yes | Character |  |
| on\_guest\_arrived\_from\_pool |  | Yes | Character |  |
| on\_siege\_completion |  | Yes | Character |  |
| on\_war\_won\_attacker |  | Yes | Casus belli |  |
| on\_alliance\_added |  | Yes | None |  |
| on\_pregnancy\_mother |  | Yes | Character |  |
| on\_raid\_action\_start |  | Yes | None |  |
| on\_county\_faith\_change |  | Yes | Landed Title |  |
| on\_title\_gain\_usurpation |  | Yes | None |  |
| on\_release\_from\_prison |  | Yes | Character |  |
| random\_yearly\_playable\_pulse |  | Yes | Character |  |
| on\_raid\_action\_completion |  | Yes | Army |  |
| on\_death |  | Yes | Character |  |
| on\_birth\_father |  | Yes | None |  |
| on\_betrothal\_broken |  | Yes | None |  |
| on\_war\_white\_peace |  | Yes | None |  |
| three\_year\_playable\_pulse |  | Yes | Character |  |
| on\_defeat\_raid\_army |  | Yes | Army |  |
| on\_army\_enter\_province |  | Yes | Character |  |
| on\_join\_court |  | Yes | Character |
| on\_fired\_from\_council |  | Yes | Character |  |
| on\_raid\_loot\_delivered |  | Yes | Army |  |
| on\_pregnancy\_ended\_mother |  | Yes | None |  |
| on\_title\_lost |  | Yes | None |  |
| on\_title\_gain |  | Yes | Character |  |
| on\_character\_culture\_change |  | Yes | Character |  |
| on\_birth\_child |  | Yes | Character |  |
| on\_holy\_order\_hired |  | Yes | None |  |
| on\_great\_holy\_war\_invalidation |  | Yes | Great Holy War |  |
| on\_combat\_end\_loser |  | Yes | Combat Side |  |
| on\_concubinage |  | Yes | None |  |
| on\_commander\_combat\_pulse |  | Yes | Character |  |
| random\_yearly\_everyone\_pulse |  | Yes | Character |  |
| five\_year\_everyone\_pulse |  | Yes | Character |  |
| on\_perks\_refunded |  | Yes | None |  |
| quarterly\_playable\_pulse |  | Yes | None |  |
| on\_prestige\_level\_gain |  | Yes | None |  |
| on\_faith\_created |  | Yes | Character |  |
| on\_holy\_order\_new\_lease |  | Yes | None |  |
| on\_title\_gain\_inheritance |  | Yes | None |  |
| on\_game\_start |  | Yes | None |  |
| on\_character\_faith\_change |  | Yes | Character |  |
| on\_combat\_end\_winner |  | Yes | Combat Side |  |
| on\_courtier\_decided\_to\_move\_to\_pool |  | Yes | Character |  |
| on\_culture\_era\_changed |  | Yes | None |  |
| on\_birthday |  | Yes | Character |  |
| on\_faith\_conversion |  | Yes | Character |  |
| on\_raid\_action\_weekly |  | Yes | None |  |
| on\_explicit\_claim\_gain |  | Yes | Character |  |
| on\_courtier\_ready\_to\_move\_to\_pool |  | Yes | Character |  |
| on\_potential\_great\_holy\_war\_invalidation |  | Yes | Great Holy War |  |
| on\_holy\_order\_destroyed |  | Yes | None |  |
| on\_war\_won\_defender |  | Yes | Casus belli |  |
| yearly\_global\_pulse |  | Yes | None |  |
| on\_great\_holy\_war\_countdown\_end |  | Yes | GreaT Holy War |  |
| yearly\_playable\_pulse |  | Yes | Character |  |
| three\_year\_pool\_pulse |  | Yes | Character |  |
| on\_pregnancy\_father |  | Yes | None |  |
| on\_piety\_level\_loss |  | Yes | None |  |
| on\_piety\_level\_gain |  | Yes | None |  |
| on\_siege\_looting |  | Yes | None |  |
| on\_title\_destroyed |  | Yes | None |  |
| on\_army\_monthly |  | Yes | None |  |
| on\_game\_start\_after\_lobby |  | Yes | None |  |
| on\_imprison |  | Yes | Character |  |
| on\_birth\_mother |  | Yes | Character |  |
| on\_dynasty\_created |  | Yes | None |  |
| on\_alliance\_removed |  | Yes | None |  |
| on\_county\_occupied |  | Yes | None |  |
| on\_rank\_up |  | Yes | None |  |
| on\_vassal\_become\_powerful |  | Yes | None |  |
| on\_join\_war\_as\_secondary |  | Yes | Character |  |
| on\_explicit\_claim\_lost |  | Yes | Character |  |
| on\_alliance\_broken |  | Yes | None |  |
| on\_natural\_death\_second\_chance |  | Yes | None |  |
| on\_leave\_council |  | Yes | Character |  |
| on\_county\_culture\_change |  | Yes | None |  |
| on\_war\_started |  | Yes | None | On-action scopes: scope:defender/scope:attacker/scope:war |
| on\_marriage |  | Yes | Character |  |
| on\_great\_holy\_war\_participant\_replaced |  | Yes | Character |  |
| five\_year\_playable\_pulse |  | Yes | Character |  |
| on\_birth\_real\_father |  | Yes | None |  |
| on\_game\_start\_with\_tutorial |  | Yes | None |  |

## Strategy\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Event_modding&veaction=edit&section=28 "Edit section: Strategy") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Event_modding&action=edit&section=28 "Edit section: Strategy")\]

### Triggering the event\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Event_modding&veaction=edit&section=29 "Edit section: Triggering the event") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Event_modding&action=edit&section=29 "Edit section: Triggering the event")\]

|     |     |
| --- | --- |
| ![Wiki letter w.png](https://central.paradoxwikis.com/images/6/6a/Wiki_letter_w.png) | Please help improve this article or section by [**expanding it**](https://ck3.paradoxwikis.com/index.php?title=Event_modding&action=edit). |

Events do not fire automatically, they have to be fired by something in the script, for example:

- [on\_actions](https://ck3.paradoxwikis.com/Event_modding#On_Actions_(on_action) "Event modding")
- [story cycles](https://ck3.paradoxwikis.com/Story_cycles_modding "Story cycles modding")
- [decisions](https://ck3.paradoxwikis.com/Decisions_modding "Decisions modding")
- character interactions

etc.

### Techniques and design patterns\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Event_modding&veaction=edit&section=30 "Edit section: Techniques and design patterns") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Event_modding&action=edit&section=30 "Edit section: Techniques and design patterns")\]

|     |     |
| --- | --- |
| ![Wiki letter w.png](https://central.paradoxwikis.com/images/6/6a/Wiki_letter_w.png) | Please help improve this article or section by [**expanding it**](https://ck3.paradoxwikis.com/index.php?title=Event_modding&action=edit). |

If you just input the information in your will be overriding vanilla on\_actions. The example below is just one of the way to add in your own events.

```
five_year_playable_pulse = {
	on_actions = { my_five_year_playable_pulse }
}
my_five_year_playable_pulse = {
		random_events = {
# Your event change name is here.
	}
}
```

Pinging events, message events.

Other fancy ideas.

**[Modding](https://ck3.paradoxwikis.com/Modding "Modding")**

|     |     |
| --- | --- |
| Documentation | [Scripting](https://ck3.paradoxwikis.com/Scripting "Scripting") • [Scopes](https://ck3.paradoxwikis.com/Scopes "Scopes") • [Effects](https://ck3.paradoxwikis.com/Effects "Effects") • [Triggers](https://ck3.paradoxwikis.com/Triggers "Triggers") • [Variables](https://ck3.paradoxwikis.com/Variables "Variables") • [Modifiers](https://ck3.paradoxwikis.com/Modifier_list "Modifier list") |

|     |     |
| --- | --- |
| Scripting | [AI](https://ck3.paradoxwikis.com/AI_modding "AI modding") • [Bookmarks](https://ck3.paradoxwikis.com/Bookmarks_modding "Bookmarks modding") • [Characters](https://ck3.paradoxwikis.com/Characters_modding "Characters modding") • [Commands](https://ck3.paradoxwikis.com/Commands "Commands") • [Council](https://ck3.paradoxwikis.com/Council_modding "Council modding") • [Culture](https://ck3.paradoxwikis.com/Culture_modding "Culture modding") • [Decisions](https://ck3.paradoxwikis.com/Decisions_modding "Decisions modding") • [Dynasties](https://ck3.paradoxwikis.com/Dynasties_modding "Dynasties modding") • Events • [Governments](https://ck3.paradoxwikis.com/Governments_modding "Governments modding") • [History](https://ck3.paradoxwikis.com/History_modding "History modding") • [Holdings](https://ck3.paradoxwikis.com/Holdings_modding "Holdings modding") • [Lifestyles](https://ck3.paradoxwikis.com/Lifestyles_modding "Lifestyles modding") • [Regiments](https://ck3.paradoxwikis.com/Regiments_modding "Regiments modding") • [Religions](https://ck3.paradoxwikis.com/Religions_modding "Religions modding") • [Script Values](https://ck3.paradoxwikis.com/Script_values "Script values") • [Story cycles](https://ck3.paradoxwikis.com/Story_cycles_modding "Story cycles modding") • [Struggles](https://ck3.paradoxwikis.com/Struggle_modding "Struggle modding") • [Titles](https://ck3.paradoxwikis.com/Title_modding "Title modding") • [Traits](https://ck3.paradoxwikis.com/Trait_modding "Trait modding") |

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

Retrieved from " [https://ck3.paradoxwikis.com/index.php?title=Event\_modding&oldid=33909](https://ck3.paradoxwikis.com/index.php?title=Event_modding&oldid=33909)"

[Categories](https://ck3.paradoxwikis.com/Special:Categories "Special:Categories"):

- [Pages using deprecated enclose attributes](https://ck3.paradoxwikis.com/index.php?title=Category:Pages_using_deprecated_enclose_attributes&action=edit&redlink=1 "Category:Pages using deprecated enclose attributes (page does not exist)")
- [Pages with syntax highlighting errors](https://ck3.paradoxwikis.com/index.php?title=Category:Pages_with_syntax_highlighting_errors&action=edit&redlink=1 "Category:Pages with syntax highlighting errors (page does not exist)")
- [Timeless](https://ck3.paradoxwikis.com/Category:Timeless "Category:Timeless")
- [Expand](https://ck3.paradoxwikis.com/Category:Expand "Category:Expand")
- [Modding](https://ck3.paradoxwikis.com/Category:Modding "Category:Modding")