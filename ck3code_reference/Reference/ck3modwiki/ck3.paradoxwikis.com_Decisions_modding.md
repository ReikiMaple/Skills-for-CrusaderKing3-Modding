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

# Decisions modding

From CK3 Wiki

[Jump to navigation](https://ck3.paradoxwikis.com/Decisions_modding#mw-head) [Jump to search](https://ck3.paradoxwikis.com/Decisions_modding#searchInput)

Please help with verifying or updating older sections of this article.

At least some were last verified for [version](https://ck3.paradoxwikis.com/CK3_Wiki:Versioning "CK3 Wiki:Versioning") 1.14.

This article is for the PC version of Crusader Kings 3 only.

|     |     |
| --- | --- |
| ![Wiki letter w.png](https://central.paradoxwikis.com/images/6/6a/Wiki_letter_w.png) | Please help improve this article or section by [**expanding it**](https://ck3.paradoxwikis.com/index.php?title=Decisions_modding&action=edit) with: examples, advanced uses. |

[Decisions](https://ck3.paradoxwikis.com/Decision "Decision") can be modded into the game. They are optional actions that adventurers and count rulers or above may take.

## Contents

- [1Location](https://ck3.paradoxwikis.com/Decisions_modding#Location)
- [2Structure](https://ck3.paradoxwikis.com/Decisions_modding#Structure)
  - [2.1Basic example](https://ck3.paradoxwikis.com/Decisions_modding#Basic_example)
- [3Localization](https://ck3.paradoxwikis.com/Decisions_modding#Localization)
  - [3.1Keys/blocks](https://ck3.paradoxwikis.com/Decisions_modding#Keys/blocks)
  - [3.2Values](https://ck3.paradoxwikis.com/Decisions_modding#Values)
- [4Custom widgets](https://ck3.paradoxwikis.com/Decisions_modding#Custom_widgets)
- [5Testing Decisions](https://ck3.paradoxwikis.com/Decisions_modding#Testing_Decisions)
- [6Decision ID](https://ck3.paradoxwikis.com/Decisions_modding#Decision_ID)

## Location\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Decisions_modding&veaction=edit&section=1 "Edit section: Location") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Decisions_modding&action=edit&section=1 "Edit section: Location")\]

Decisions belong in .txt files in the mod's `common\decisions` folder. Each text file may contain multiple decisions.

## Structure\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Decisions_modding&veaction=edit&section=2 "Edit section: Structure") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Decisions_modding&action=edit&section=2 "Edit section: Structure")\]

Decisions may be defined like so:

```
my_decision = {
	effect = {
		add_gold = 100
	}

	# Other blocks
}
```

The part that says `my_decision` is called the _name_ or _key_ or _id_ of the decision. It can be anything you want, but it should be unique. If you define another decision with the same name, one of them will override the other (depending on which one is loaded last). It is common practice to give decisions names that end with "\_decision", but it is not necessary.

### Basic example\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Decisions_modding&veaction=edit&section=3 "Edit section: Basic example") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Decisions_modding&action=edit&section=3 "Edit section: Basic example")\]

```
custom_decision = {
	picture = { reference = "gfx/interface/illustrations/decisions/decision_smith.dds" }

	desc = custom_decision_desc
	selection_tooltip = custom_decision_tooltip

	is_shown = {
		# Put conditions for the decision to show up here.
	}

	effect = {
		# Add effects of the decision here.
	}

	ai_check_interval = 0 # Change this value if you want the AI to consider this decision.
}
```

## Localization\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Decisions_modding&veaction=edit&section=4 "Edit section: Localization") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Decisions_modding&action=edit&section=4 "Edit section: Localization")\]

We also need to add 4 entries to [Localization](https://ck3.paradoxwikis.com/Localization "Localization") files to describe the decision to the player.

All 4 will start with the id of your decision, plus \_desc, \_tooltip and \_confirm.

For example, create a file `localization/english/my_decisions_l_english.yml` with this:

```
l_english:
 my_decision: "My decision's name"
 my_decision_desc: "Description shown when you open it"
 my_decision_tooltip: "Tooltip shown when hovering over it"
 my_decision_confirm: "The text on the confirm button"
```

Make sure to read the [Localization](https://ck3.paradoxwikis.com/Localization "Localization") page to properly define your localization, as it's easy to make a mistake there.

If you want, the default names of these localization entries can be changed with the `title`, `desc`, `selection_tooltip`, and `confirm_text` entries in the decision. This can be useful if you want to make multiple decisions with the same localization.

### Keys/blocks\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Decisions_modding&veaction=edit&section=5 "Edit section: Keys/blocks") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Decisions_modding&action=edit&section=5 "Edit section: Keys/blocks")\]

The table below shows keys and blocks that may be defined. "Boolean" values may be either yes or no.

For the full list see common/decision/decision.info file.

| Key/block | Type | Description | Example |
| --- | --- | --- | --- |
| picture | String (file name) | Sets the image of the decision and optionally the sound. Multiple pictures can be set with triggers to choose one. | `picture = { reference = "gfx/image.dds" }` |
| extra\_picture | String (file name) | An extra picture, currently used by Struggle decisions |  |
| decision\_group\_type | String | Foldable decision group type to put this decision in. Types are listed common\\decision\_group\_types | `decision_group_type = major` |
| sort\_order | Number | How high in the list of decisions this decision should be placed. Higher numbers are sorted above lower numbers. |  |
| is\_invisible | yes/no |  |  |
| ai\_goal | yes/no | The AI will budget for this decision. `ai_check_interval` will be ignored if this is set. |  |
| ai\_check\_interval | Integer | How many months to go between each check of this decision. Has to be set, except if ai\_goal = yes is set. An interval of 0 means the AI will never check this decision |  |
| cooldown | Block | How long the decision will be unavailable after it has been taken. Can be in years, months, or days. | `cooldown = { years = 5 }` |
| confirm\_click\_sound | String | A sound file to play | `confirm_click_sound = "event:/DLC/FP2/SFX/UI/fp2_struggle_ending_decision_confirm"` |
| selection\_tooltip | Localization key or block | Overrides the default tooltip for this decision on the decision panel. The default is the decision name plus "\_tooltip". It can also be a block like in event descriptions. |  |
| title | Localization key or block | Overrides the default localization key for the decision title, which is normally the same as the decision name. It can also be a block like in event descriptions. |  |
| desc | Localization key or block | Overrides the default localization key for the description, which is the decision name plus "\_desc".<br>It can also be a block like in event descriptions. | ```<br>desc = start_hunt_decision<br>``` |
| confirm\_text | Localization key or Block | Overrides the default localization key for the text on the confirm button, which is the decision\_name plus "\_confirm".<br>It can also be a block like in event descriptions. |  |
| is\_shown | Trigger | This determines the conditions required for the decision to appear in the decisions tab. | ```<br>is_shown = {<br>        has_royal_court = yes<br>}<br>``` |
| is\_valid\_showing\_failures\_only | Trigger | Can this decision be taken now? Both this trigger and `is_valid` must be satisfied. The tooltip for this trigger only shows conditions that were not met. | ```<br>is_valid_showing_failures_only = {<br>        is_available_adult = yes<br>        is_at_war = no<br>}<br>``` |
| is\_valid | Trigger | Can this decision be taken now? Both this trigger and `is_valid_showing_failures_only` must be satisfied. | ```<br>is_valid = {<br>        piety_level >= 3<br>}<br>``` |
| cost | Block | Sets the cost of the decision in terms of gold, piety and prestige. The default value for each resource is zero. Not every resource has to be defined. The values can be script values. | ```<br>cost = {<br>	gold = 42<br>	piety = 42<br>	prestige = 42<br>}<br>``` |
| minimum\_cost | Block | Like `cost`, but the character only needs to have that much available. The cost is not deducted when the decision is taken. Useful when the real cost is scripted in events triggered from this decision, and similar cases. |
| effect | Block | What the decision will do when it is taken. | ```<br>add_character_modifier = {<br>        modifier = vow_of_poverty_modifier<br>}<br>``` |
| ai\_potential | Trigger | Whether the AI will consider this decision. | ```<br>ai_potential = {<br>        always = yes<br>}<br>``` |
| ai\_will\_do | Block | A calculation of the % chance the AI will take this decision when considering it. | ```<br>ai_will_do = {<br>        base = 100<br>}<br>``` |
| should\_create\_alert | Trigger | This trigger is checked when the decision would otherwise notify the player that it can be taken. If the trigger is not satisfied, the alert is not shown. This can be good to add if there are situations where taking the decision is possible but not useful. | ```<br>should_create_alert = {<br>        gold >= 50<br>}<br>``` |
| widget | String or Block | A custom gui widget with extra options.<br>The widget must be created in`gui/decision_view_widgets/`, the file name must match the widget name.<br>Important! The default controller doesn't work. Try using create\_holy\_order | ```<br>widget = {<br>        gui = "decision_view_widget_commission_artifact"<br>        controller = decision_option_list_controller<br>        ...<br>}<br>``` |

### Values\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Decisions_modding&veaction=edit&section=6 "Edit section: Values") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Decisions_modding&action=edit&section=6 "Edit section: Values")\]

You can define settings (usually at the top of the file) that can be used in the decisions in place of directly writing numbers. This can be useful to avoid repeating yourself, to avoid subtle errors when you change a value in one place but not in another, or simply to emphasize that the value can be adjusted for balance reasons.

For example:

```
@sale_of_titles_prestige_cost = 500

sale_of_titles_decision = {
        ... stuff ...

        cost = {
                prestige = @sale_of_titles_prestige_cost
        }

        ... stuff ...
}
```

## Custom widgets\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Decisions_modding&veaction=edit&section=7 "Edit section: Custom widgets") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Decisions_modding&action=edit&section=7 "Edit section: Custom widgets")\]

Custom gui widgets can be added to a decision to let the player make an additional choice.

See the widget entry in the .info file for more details.

**Important!** The default controller doesn't work, try using `controller = create_holy_order`

## Testing Decisions\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Decisions_modding&veaction=edit&section=8 "Edit section: Testing Decisions") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Decisions_modding&action=edit&section=8 "Edit section: Testing Decisions")\]

Sometimes, when testing a mod, it is useful to automatically refresh the cooldown of a decision (for example, if testing an on-action triggered when a hunt or a feast begins). This can be done by running `effect remove_decision_cooldown = decision_id`. See below for a list of ids for built-in decisions.

## Decision ID\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Decisions_modding&veaction=edit&section=9 "Edit section: Decision ID") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Decisions_modding&action=edit&section=9 "Edit section: Decision ID")\]

To quickly find the id of a decision, search through localization folder for its name. You'll see something like `my_decision: "My decision"`

To do a folder search, use a proper text editor, like VSCode.

Drop the localization folder in, right-click it > Find in Folder or press Ctrl+Shift+F.

Often, the id matches the name, if we replaced all spaces with underscores and added \_decision on the end.

For example, "Commission Artifact" is called commission\_artifact\_decision.

Some decisions that do not match their internal name are included in the table below:

| Decision | Internal name |
| --- | --- |
| Call Hunt | start\_hunt |
| Search for Physician | hire\_physician |
| Borrow Gold from Holy Order | borrow\_from\_holy\_order |
| Challenge the Ruler | tribal\_challenge\_ruler |
| Stop Gaining Weight | stop\_gain\_weight |
| Stop Losing Weight | stop\_lose\_weight |
| Attempt Suicide | commit\_suicide |
| Return Roma | return\_rome |
| Determine Bhakti | select\_personal\_deity |
| Give Your Ancestor a Sky Burial | give\_sky\_burial |
| Raise a Runestone | raise\_runestone |
| Found Holy Order | create\_holy\_order |
| Revoke Holy Order Lease | cancel\_holy\_order\_lease |
| Go on a Pilgrimage | go\_on\_pilgrimage |
| Undertake the Hajj | go\_on\_hajj |
| Restore the Kingdom of Cornwall | restore\_dumnonia |
| Reclaim Constantinople | set\_capital\_constantinople |
| Reclaim Rome | set\_capital\_rome |
| Restore the Papacy | restore\_papacy |
| Form the Swiss Confederation | form\_switzerland\_kingdom |
| Form Archduchy of Austria | form\_austria\_kingdom |
| Dismantle the Papacy | dismantle\_papacy |
| Restore Carolingian Borders | reform\_carolingian\_empire |
| Unify the Burgundies | unify\_burgundy\_kingdom |
| Unify Italy | unify\_italian\_empire |
| Adopt Feudalism (unused) | convert\_to\_feudalism |
| Adopt Feudal / Clan Ways through Liege | convert\_to\_feudalism\_liege\_converted |
| Adopt Feudal / Clan Ways | convert\_whole\_realm\_to\_feudalism |
| Form the Outremer Empire | create\_outremer\_empire |
| Sell Minor Titles | sale\_of\_titles |
| Restore the Ash'ari Caliphate | restore\_sunni\_caliphate |
| Restore Israel | create\_israel\_kingdom |
| Restore the Faith High Priesthood | jewish\_restore\_high\_priesthood |
| Restore the Faith High Priesthood | zoroastrian\_restore\_high\_priesthood |
| Become the Saoshyant | become\_saoshyant |
| Dismantle German Pretenders | dismantle\_holy\_pretender |
| Dismantle Greek Pretenders | dismantle\_byz\_pretender |
| Form the Sultanate of Rum | form\_rum\_sultanate |
| Revive Greater Armenia | create\_armenian\_empire |
| Consecrate Bloodline | declare\_bloodline\_holy |
| Build a Grand Church | build\_grand\_church |
| Faith Cannibalism | accept\_cannibalism |
| Request Claim on Ireland | england\_request\_laudabiliter |
| Inspire Opus Francigenum | promote\_gothic\_innovations |
| Build a Glass Monument | lunatic\_building |
| Promote Christian Settlements | promote\_hungarian\_settlement |
| Revive Táltosism | revive\_magyar\_paganism |
| Unite the West Slavs | unite\_the\_western\_slavs |
| Unite the South Slavs | unite\_the\_southern\_slavs |
| Defenders of High God | defenders\_of\_highgod |
| Found a New Kingdom | found\_kingdom |
| Found a New Empire | found\_empire |
| Amnesty for False Conversions | encourage\_confession\_of\_false\_conversions |
| Restore the Holy Roman Empire | restore\_holy\_roman\_empire |
| Adopt Special Succession Type | adopt\_special\_succession |
| Found the Kingdom of Aragon | form\_the\_kingdom\_of\_aragon |
| Indulge in Drink | stress\_loss\_drunkard |
| Consume Hashish Cakes | stress\_loss\_hashishiyah |
| Visit a Brothel | stress\_loss\_rakish |
| Seclude Yourself | stress\_loss\_reclusive |
| Lash Out | stress\_loss\_irritable |
| Flagellate | stress\_loss\_flagellant |
| Visit the Market | stress\_loss\_profligate |
| Donate to Charity | stress\_loss\_improvident |
| Confess | stress\_loss\_contrite |
| Indulge in Food | stress\_loss\_comfort\_eater |
| Shun Food | stress\_loss\_inappetetic |
| Write Thoughts Down | stress\_loss\_journaller |
| Talk to Confidant | stress\_loss\_confider |
| Work off Some Stress | stress\_loss\_athletic |
| Accuse the Krstjani of Heresy | accuse\_krstjani\_of\_heresy |
| Prepare to Cross the Carpathians | launch\_hungarian\_migration |
| Restore the Roman Empire | restore\_roman\_empire (as Byzantine Emperor)<br>restore\_roman\_empire\_holy (as Holy Roman Emperor)<br>restore\_roman\_empire\_italian (as Emperor of Italia) |
| Host Grand Rite | host\_witch\_ritual\_decision |

**[Modding](https://ck3.paradoxwikis.com/Modding "Modding")**

|     |     |
| --- | --- |
| Documentation | [Scripting](https://ck3.paradoxwikis.com/Scripting "Scripting") • [Scopes](https://ck3.paradoxwikis.com/Scopes "Scopes") • [Effects](https://ck3.paradoxwikis.com/Effects "Effects") • [Triggers](https://ck3.paradoxwikis.com/Triggers "Triggers") • [Variables](https://ck3.paradoxwikis.com/Variables "Variables") • [Modifiers](https://ck3.paradoxwikis.com/Modifier_list "Modifier list") |

|     |     |
| --- | --- |
| Scripting | [AI](https://ck3.paradoxwikis.com/AI_modding "AI modding") • [Bookmarks](https://ck3.paradoxwikis.com/Bookmarks_modding "Bookmarks modding") • [Characters](https://ck3.paradoxwikis.com/Characters_modding "Characters modding") • [Commands](https://ck3.paradoxwikis.com/Commands "Commands") • [Council](https://ck3.paradoxwikis.com/Council_modding "Council modding") • [Culture](https://ck3.paradoxwikis.com/Culture_modding "Culture modding") • Decisions • [Dynasties](https://ck3.paradoxwikis.com/Dynasties_modding "Dynasties modding") • [Events](https://ck3.paradoxwikis.com/Event_modding "Event modding") • [Governments](https://ck3.paradoxwikis.com/Governments_modding "Governments modding") • [History](https://ck3.paradoxwikis.com/History_modding "History modding") • [Holdings](https://ck3.paradoxwikis.com/Holdings_modding "Holdings modding") • [Lifestyles](https://ck3.paradoxwikis.com/Lifestyles_modding "Lifestyles modding") • [Regiments](https://ck3.paradoxwikis.com/Regiments_modding "Regiments modding") • [Religions](https://ck3.paradoxwikis.com/Religions_modding "Religions modding") • [Script Values](https://ck3.paradoxwikis.com/Script_values "Script values") • [Story cycles](https://ck3.paradoxwikis.com/Story_cycles_modding "Story cycles modding") • [Struggles](https://ck3.paradoxwikis.com/Struggle_modding "Struggle modding") • [Titles](https://ck3.paradoxwikis.com/Title_modding "Title modding") • [Traits](https://ck3.paradoxwikis.com/Trait_modding "Trait modding") |

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

Retrieved from " [https://ck3.paradoxwikis.com/index.php?title=Decisions\_modding&oldid=26456](https://ck3.paradoxwikis.com/index.php?title=Decisions_modding&oldid=26456)"

[Categories](https://ck3.paradoxwikis.com/Special:Categories "Special:Categories"):

- [Potentially outdated](https://ck3.paradoxwikis.com/Category:Potentially_outdated "Category:Potentially outdated")
- [1.14](https://ck3.paradoxwikis.com/Category:1.14 "Category:1.14")
- [Expand](https://ck3.paradoxwikis.com/Category:Expand "Category:Expand")
- [Modding](https://ck3.paradoxwikis.com/Category:Modding "Category:Modding")