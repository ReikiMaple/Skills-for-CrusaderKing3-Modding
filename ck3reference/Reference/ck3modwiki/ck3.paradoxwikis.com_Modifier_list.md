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

# Modifier list

From CK3 Wiki

[Jump to navigation](https://ck3.paradoxwikis.com/Modifier_list#mw-head) [Jump to search](https://ck3.paradoxwikis.com/Modifier_list#searchInput)

Please help with verifying or updating older sections of this article.

At least some were last verified for [version](https://ck3.paradoxwikis.com/CK3_Wiki:Versioning "CK3 Wiki:Versioning") 1.12.

This article is for the PC version of Crusader Kings 3 only.

Modifiers are applied to different scopes.

Note that there are two different things that the game calls "modifier". The first is a long term bonus or penalty that is applied to a character, dynasty, or other game item. The second is something that changes the chances of random effects happening. They are both called "modifier" but they are not related.

_Main article: [Weight modifier](https://ck3.paradoxwikis.com/Weight_modifier "Weight modifier")_

## Contents

- [1Creating a Character Modifier](https://ck3.paradoxwikis.com/Modifier_list#Creating_a_Character_Modifier)
  - [1.1Icons](https://ck3.paradoxwikis.com/Modifier_list#Icons)
- [2List of Modifiers](https://ck3.paradoxwikis.com/Modifier_list#List_of_Modifiers)
  - [2.1Vassal Stance Related Modifiers](https://ck3.paradoxwikis.com/Modifier_list#Vassal_Stance_Related_Modifiers)
  - [2.2Government Related Modifiers](https://ck3.paradoxwikis.com/Modifier_list#Government_Related_Modifiers)
  - [2.3Holding-type Related Modifiers](https://ck3.paradoxwikis.com/Modifier_list#Holding-type_Related_Modifiers)
  - [2.4Scheme Related Modifiers](https://ck3.paradoxwikis.com/Modifier_list#Scheme_Related_Modifiers)
  - [2.5Terrain Modifiers](https://ck3.paradoxwikis.com/Modifier_list#Terrain_Modifiers)
  - [2.6Men-at-Arms Related Modifiers](https://ck3.paradoxwikis.com/Modifier_list#Men-at-Arms_Related_Modifiers)

## Creating a Character Modifier\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Modifier_list&veaction=edit&section=1 "Edit section: Creating a Character Modifier") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Modifier_list&action=edit&section=1 "Edit section: Creating a Character Modifier")\]

Character modifiers are defined in .txt files in the directory: ../common/modifiers

A character modifier is defined as given below:

```
my_new_modifier = {
	icon = icon_name

	# Modifiers, such as
	# tax_mult = 0.25
	# county_opinion_add = -30
}
```

### Icons\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Modifier_list&veaction=edit&section=2 "Edit section: Icons") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Modifier_list&action=edit&section=2 "Edit section: Icons")\]

Each modifier has an icon that is displayed with its name. It can be set by using `icon=icon_name` in the main modifier block. The base game has the following modifier icons available:

| Name | Icon | Name | Icon |
| --- | --- | --- | --- |
| cat\_positive | ![](https://ck3.paradoxwikis.com/images/thumb/9/94/Modifier_cat_positive.png/24px-Modifier_cat_positive.png) | cat\_negative | ![](https://ck3.paradoxwikis.com/images/thumb/9/95/Modifier_cat_negative.png/24px-Modifier_cat_negative.png) |
| cockroach\_positive | ![](https://ck3.paradoxwikis.com/images/thumb/8/81/Modifier_cockroach_positive.png/24px-Modifier_cockroach_positive.png) | cockroach\_negative | ![](https://ck3.paradoxwikis.com/images/thumb/b/b2/Modifier_cockroach_negative.png/24px-Modifier_cockroach_negative.png) |
| county\_modifier\_control\_positive | ![](https://ck3.paradoxwikis.com/images/thumb/8/82/Modifier_county_control_positive.png/24px-Modifier_county_control_positive.png) | county\_modifier\_control\_negative | ![](https://ck3.paradoxwikis.com/images/thumb/3/3d/Modifier_county_control_negative.png/24px-Modifier_county_control_negative.png) |
| county\_modifier\_corruption\_positive | ![](https://ck3.paradoxwikis.com/images/thumb/4/4d/Modifier_county_corruption_positive.png/24px-Modifier_county_corruption_positive.png) | county\_modifier\_corruption\_negative | ![](https://ck3.paradoxwikis.com/images/thumb/d/de/Modifier_county_corruption_negative.png/24px-Modifier_county_corruption_negative.png) |
| county\_modifier\_development\_positive | ![](https://ck3.paradoxwikis.com/images/thumb/1/1a/Modifier_county_development_positive.png/24px-Modifier_county_development_positive.png) | county\_modifier\_development\_negative | ![](https://ck3.paradoxwikis.com/images/thumb/0/01/Modifier_county_development_negative.png/24px-Modifier_county_development_negative.png) |
| county\_modifier\_opinion\_positive | ![](https://ck3.paradoxwikis.com/images/thumb/4/4d/Modifier_county_opinion_positive.png/24px-Modifier_county_opinion_positive.png) | county\_modifier\_opinion\_negative | ![](https://ck3.paradoxwikis.com/images/thumb/b/b5/Modifier_county_opinion_negative.png/24px-Modifier_county_opinion_negative.png) |
| diplomacy\_positive | ![](https://ck3.paradoxwikis.com/images/thumb/2/21/Modifier_diplomacy_positive.png/24px-Modifier_diplomacy_positive.png) | diplomacy\_negative | ![](https://ck3.paradoxwikis.com/images/thumb/1/1c/Modifier_diplomacy_negative.png/24px-Modifier_diplomacy_negative.png) |
| dog\_positive | ![](https://ck3.paradoxwikis.com/images/thumb/2/2a/Modifier_dog_positive.png/24px-Modifier_dog_positive.png) | dog\_negative | ![](https://ck3.paradoxwikis.com/images/thumb/2/23/Modifier_dog_negative.png/24px-Modifier_dog_negative.png) |
| dread\_positive | ![](https://ck3.paradoxwikis.com/images/thumb/c/ca/Modifier_dread_positive.png/24px-Modifier_dread_positive.png) | dread\_negative | ![](https://ck3.paradoxwikis.com/images/thumb/c/cb/Modifier_dread_negative.png/24px-Modifier_dread_negative.png) |
| drink\_positive | ![](https://ck3.paradoxwikis.com/images/thumb/c/c0/Modifier_drink_positive.png/24px-Modifier_drink_positive.png) | drink\_negative | ![](https://ck3.paradoxwikis.com/images/thumb/f/f6/Modifier_drink_negative.png/24px-Modifier_drink_negative.png) |
| economy\_positive | ![](https://ck3.paradoxwikis.com/images/thumb/5/5d/Modifier_economy_positive.png/24px-Modifier_economy_positive.png) | economy\_negative | ![](https://ck3.paradoxwikis.com/images/thumb/8/80/Modifier_economy_negative.png/24px-Modifier_economy_negative.png) |
| family\_positive | ![](https://ck3.paradoxwikis.com/images/thumb/4/40/Modifier_family_positive.png/24px-Modifier_family_positive.png) | family\_negative | ![](https://ck3.paradoxwikis.com/images/thumb/3/37/Modifier_family_negative.png/24px-Modifier_family_negative.png) |
| feast\_positive | ![](https://ck3.paradoxwikis.com/images/thumb/9/96/Modifier_feast_positive.png/24px-Modifier_feast_positive.png) | feast\_negative | ![](https://ck3.paradoxwikis.com/images/thumb/b/b1/Modifier_feast_negative.png/24px-Modifier_feast_negative.png) |
| fertility\_positive | ![](https://ck3.paradoxwikis.com/images/thumb/0/09/Modifier_fertility_positive.png/24px-Modifier_fertility_positive.png) | fertility\_negative | ![](https://ck3.paradoxwikis.com/images/thumb/d/dd/Modifier_fertility_negative.png/24px-Modifier_fertility_negative.png) |
| food\_positive | ![](https://ck3.paradoxwikis.com/images/thumb/2/2c/Modifier_food_positive.png/24px-Modifier_food_positive.png) | food\_negative | ![](https://ck3.paradoxwikis.com/images/thumb/6/6b/Modifier_food_negative.png/24px-Modifier_food_negative.png) |
| health\_positive | ![](https://ck3.paradoxwikis.com/images/thumb/8/8a/Modifier_health_positive.png/24px-Modifier_health_positive.png) | health\_negative | ![](https://ck3.paradoxwikis.com/images/thumb/8/8d/Modifier_health_negative.png/24px-Modifier_health_negative.png) |
| horse\_positive | ![](https://ck3.paradoxwikis.com/images/thumb/6/6f/Modifier_horse_positive.png/24px-Modifier_horse_positive.png) | horse\_negative | ![](https://ck3.paradoxwikis.com/images/thumb/e/e4/Modifier_horse_negative.png/24px-Modifier_horse_negative.png) |
| hunt\_positive | ![](https://ck3.paradoxwikis.com/images/thumb/4/41/Modifier_hunt_positive.png/24px-Modifier_hunt_positive.png) | hunt\_negative | ![](https://ck3.paradoxwikis.com/images/thumb/b/b0/Modifier_hunt_negative.png/24px-Modifier_hunt_negative.png) |
| intrigue\_positive | ![](https://ck3.paradoxwikis.com/images/thumb/6/62/Modifier_intrigue_positive.png/24px-Modifier_intrigue_positive.png) | intrigue\_negative | ![](https://ck3.paradoxwikis.com/images/thumb/1/1f/Modifier_intrigue_negative.png/24px-Modifier_intrigue_negative.png) |
| learning\_positive | ![](https://ck3.paradoxwikis.com/images/thumb/1/1e/Modifier_learning_positive.png/24px-Modifier_learning_positive.png) | learning\_negative | ![](https://ck3.paradoxwikis.com/images/thumb/6/6c/Modifier_learning_negative.png/24px-Modifier_learning_negative.png) |
| letter\_positive | ![](https://ck3.paradoxwikis.com/images/thumb/6/69/Modifier_letter_positive.png/24px-Modifier_letter_positive.png) | letter\_negative | ![](https://ck3.paradoxwikis.com/images/thumb/1/11/Modifier_letter_negative.png/24px-Modifier_letter_negative.png) |
| love\_positive | ![](https://ck3.paradoxwikis.com/images/thumb/c/c2/Modifier_love_positive.png/24px-Modifier_love_positive.png) | love\_negative | ![](https://ck3.paradoxwikis.com/images/thumb/4/4f/Modifier_love_negative.png/24px-Modifier_love_negative.png) |
| magic\_positive | ![](https://ck3.paradoxwikis.com/images/thumb/4/47/Modifier_magic_positive.png/24px-Modifier_magic_positive.png) | magic\_negative | ![](https://ck3.paradoxwikis.com/images/thumb/e/ef/Modifier_magic_negative.png/24px-Modifier_magic_negative.png) |
| martial\_positive | ![](https://ck3.paradoxwikis.com/images/thumb/2/2e/Modifier_martial_positive.png/24px-Modifier_martial_positive.png) | martial\_negative | ![](https://ck3.paradoxwikis.com/images/thumb/2/29/Modifier_martial_negative.png/24px-Modifier_martial_negative.png) |
| outdoors\_positive | ![](https://ck3.paradoxwikis.com/images/thumb/f/fa/Modifier_outdoors_positive.png/24px-Modifier_outdoors_positive.png) | outdoors\_negative | ![](https://ck3.paradoxwikis.com/images/thumb/8/83/Modifier_outdoors_negative.png/24px-Modifier_outdoors_negative.png) |
| piety\_positive | ![](https://ck3.paradoxwikis.com/images/thumb/b/b3/Modifier_piety_positive.png/24px-Modifier_piety_positive.png) | piety\_negative | ![](https://ck3.paradoxwikis.com/images/thumb/e/ea/Modifier_piety_negative.png/24px-Modifier_piety_negative.png) |
| prestige\_positive | ![](https://ck3.paradoxwikis.com/images/thumb/4/4d/Modifier_prestige_positive.png/24px-Modifier_prestige_positive.png) | prestige\_negative | ![](https://ck3.paradoxwikis.com/images/thumb/0/01/Modifier_prestige_negative.png/24px-Modifier_prestige_negative.png) |
| prison\_positive | ![](https://ck3.paradoxwikis.com/images/thumb/8/85/Modifier_prison_positive.png/24px-Modifier_prison_positive.png) | prison\_negative | ![](https://ck3.paradoxwikis.com/images/thumb/a/a0/Modifier_prison_negative.png/24px-Modifier_prison_negative.png) |
| prowess\_positive | ![](https://ck3.paradoxwikis.com/images/thumb/5/50/Modifier_prowess_positive.png/24px-Modifier_prowess_positive.png) | prowess\_negative | ![](https://ck3.paradoxwikis.com/images/thumb/b/b0/Modifier_prowess_negative.png/24px-Modifier_prowess_negative.png) |
| rat\_positive | ![](https://ck3.paradoxwikis.com/images/thumb/6/68/Modifier_rat_positive.png/24px-Modifier_rat_positive.png) | rat\_negative | ![](https://ck3.paradoxwikis.com/images/thumb/8/88/Modifier_rat_negative.png/24px-Modifier_rat_negative.png) |
| rock\_positive | ![](https://ck3.paradoxwikis.com/images/thumb/d/d3/Modifier_rock_positive.png/24px-Modifier_rock_positive.png) | rock\_negative | ![](https://ck3.paradoxwikis.com/images/thumb/b/bc/Modifier_rock_negative.png/24px-Modifier_rock_negative.png) |
| social\_positive | ![](https://ck3.paradoxwikis.com/images/thumb/a/aa/Modifier_social_positive.png/24px-Modifier_social_positive.png) | social\_negative | ![](https://ck3.paradoxwikis.com/images/thumb/5/52/Modifier_social_negative.png/24px-Modifier_social_negative.png) |
| spoon\_positive | ![](https://ck3.paradoxwikis.com/images/thumb/0/08/Modifier_spoon_positive.png/24px-Modifier_spoon_positive.png) | spoon\_negative | ![](https://ck3.paradoxwikis.com/images/thumb/0/05/Modifier_spoon_negative.png/24px-Modifier_spoon_negative.png) |
| stewardship\_positive | ![](https://ck3.paradoxwikis.com/images/thumb/7/7f/Modifier_stewardship_positive.png/24px-Modifier_stewardship_positive.png) | stewardship\_negative | ![](https://ck3.paradoxwikis.com/images/thumb/c/cf/Modifier_stewardship_negative.png/24px-Modifier_stewardship_negative.png) |
| stress\_positive | ![](https://ck3.paradoxwikis.com/images/thumb/7/73/Modifier_stress_positive.png/24px-Modifier_stress_positive.png) | stress\_negative | ![](https://ck3.paradoxwikis.com/images/thumb/1/19/Modifier_stress_negative.png/24px-Modifier_stress_negative.png) |
| treatment\_positive | ![](https://ck3.paradoxwikis.com/images/thumb/9/92/Modifier_treatment_positive.png/24px-Modifier_treatment_positive.png) | treatment\_negative | ![](https://ck3.paradoxwikis.com/images/thumb/3/3e/Modifier_treatment_negative.png/24px-Modifier_treatment_negative.png) |

There are more; you can see all of them in `gfx/interface/icons/modifiers/` in your game files.

## List of Modifiers\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Modifier_list&veaction=edit&section=3 "Edit section: List of Modifiers") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Modifier_list&action=edit&section=3 "Edit section: List of Modifiers")\]

These modifiers can be used in the definition of Modifiers to apply different effects to them. Note that this list has been generated from the output of the "script\_docs" console command.

| Name | Description | Usage | Supported Scopes | Category |
| --- | --- | --- | --- | --- |
| diplomacy | Adds or Subtracts skill points from the characters Diplomacy skill. | diplomacy = 1 | Any from the Character group. | Character |
| martial | Adds or Subtracts skill points from the characters Martial skill. | martial = -3 | Any from the Character group. | Character |
| stewardship | Adds or Subtracts skill points from the characters Stewardship skill. | stewardship = 2 | Any from the Character group. | Character |
| intrigue | Adds or Subtracts skill points from the characters Intrigue skill. | intrigue = -2 | Any from the Character group. | Character |
| learning | Adds or Subtracts skill points from the characters Learning skill. | learning = 3 | Any from the Character group. | Character |
| prowess | Adds or Subtracts skill points from the characters Prowess skill. | prowess = 3 | Any from the Character group. | Character |
| prowess\_no\_portrait | As prowess, but does not affect how buff the character looks. |  |  | Character |
| negate\_diplomacy\_penalty\_add |  |  |  | Character |
| negate\_martial\_penalty\_add |  |  |  | Character |
| negate\_stewardship\_penalty\_add |  |  |  | Character |
| negate\_intrigue\_penalty\_add |  |  |  | Character |
| negate\_learning\_penalty\_add |  |  |  | Character |
| negate\_prowess\_penalty\_add |  |  |  | Character |
| no\_prowess\_loss\_from\_age |  |  |  | Character |
| diplomacy\_per\_piety\_level | The character will receive or lose a point of Diplomacy skill for every level of piety. | diplomacy\_per\_piety\_level = 1 | Any from the Character group. | Character |
| martial\_per\_piety\_level | The character will receive or lose a point of Martial skill for every level of piety. | martial\_per\_piety\_level = -2 | Any from the Character group. | Character |
| stewardship\_per\_piety\_level | The character will receive or lose a point of Stewardship skill for every level of piety. | stewardship\_per\_piety\_level = 1 | Any from the Character group. | Character |
| intrigue\_per\_piety\_level | The character will receive or lose a point of Intrigue skill for every level of piety. | intrigue\_per\_piety\_level = 2 | Any from the Character group. | Character |
| learning\_per\_piety\_level | The character will receive or lose a point of Learning skill for every level of piety. | learning\_per\_piety\_level = -1 | Any from the Character group. | Character |
| prowess\_per\_piety\_level | The character will receive or lose a point of Prowess skill for every level of piety. | prowess\_per\_piety\_level = 1 | Any from the Character group. | Character |
| diplomacy\_per\_prestige\_level |  |  | Any from the Character group. | Character |
| martial\_per\_prestige\_level |  |  |  | Character |
| stewardship\_per\_prestige\_level |  |  |  | Character |
| intrigue\_per\_prestige\_level |  |  |  | Character |
| learning\_per\_prestige\_level |  |  |  | Character |
| prowess\_per\_prestige\_level |  |  |  | Character |
| piety\_level\_impact\_mult |  |  |  | Character |
| prestige\_level\_impact\_mult |  |  |  | Character |
| diplomacy\_per\_stress\_level |  |  |  | Character |
| martial\_per\_stress\_level |  |  |  | Character |
| stewardship\_per\_stress\_level |  |  |  | Character |
| intrigue\_per\_stress\_level |  |  |  | Character |
| learning\_per\_stress\_level |  |  |  | Character |
| prowess\_per\_stress\_level |  |  |  | Character |
| fertility |  |  |  | Character |
| health |  |  |  | Character |
| negate\_fertility\_penalty\_add |  |  |  | Character |
| negate\_health\_penalty\_add |  |  |  | Character |
| monthly\_income |  |  |  | Character |
| monthly\_income\_mult |  |  |  | Character |
| monthly\_war\_income\_add |  |  |  | Character |
| monthly\_war\_income\_mult |  |  |  | Character |
| monthly\_income\_per\_stress\_level\_add |  |  |  | Character |
| monthly\_income\_per\_stress\_level\_mult |  |  |  | Character |
| monthly\_piety |  |  |  | Character |
| monthly\_piety\_gain\_mult |  |  |  | Character |
| monthly\_piety\_gain\_per\_happy\_powerful\_vassal\_add |  |  |  | Character |
| monthly\_piety\_gain\_per\_happy\_powerful\_vassal\_mult |  |  |  | Character |
| monthly\_piety\_gain\_per\_dread\_add |  |  |  | Character |
| monthly\_piety\_gain\_per\_dread\_mult |  |  |  | Character |
| monthly\_piety\_gain\_per\_knight\_add |  |  |  | Character |
| monthly\_piety\_gain\_per\_knight\_mult |  |  |  | Character |
| monthly\_prestige |  |  |  | Character |
| monthly\_prestige\_gain\_mult |  |  |  | Character |
| monthly\_prestige\_gain\_per\_happy\_powerful\_vassal\_add |  |  |  | Character |
| monthly\_prestige\_gain\_per\_happy\_powerful\_vassal\_mult |  |  |  | Character |
| monthly\_prestige\_gain\_per\_dread\_add |  |  |  | Character |
| monthly\_prestige\_gain\_per\_dread\_mult |  |  |  | Character |
| monthly\_prestige\_gain\_per\_knight\_add |  |  |  | Character |
| monthly\_prestige\_gain\_per\_knight\_mult |  |  |  | Character |
| monthly\_piety\_from\_buildings\_mult |  |  |  | Character |
| monthly\_prestige\_from\_buildings\_mult |  |  |  | Character |
| monthly\_dynasty\_prestige |  |  |  | Character |
| monthly\_dynasty\_prestige\_mult |  |  |  | Character |
| monthly\_influence |  |  |  | Character |
| monthly\_influence\_mult |  |  |  | Character |
| stress\_gain\_mult |  |  |  | Character |
| stress\_loss\_mult |  |  |  | Character |
| monthly\_dread |  |  |  | Character |
| dread\_gain\_mult |  |  |  | Character |
| dread\_loss\_mult |  |  |  | Character |
| tyranny\_gain\_mult |  |  |  | Character |
| tyranny\_loss\_mult |  |  |  | Character |
| monthly\_tyranny |  |  |  | Character |
| dread\_baseline\_add |  |  |  | Character |
| dread\_decay\_add |  |  |  | Character |
| dread\_decay\_mult |  |  |  | Character |
| dread\_per\_tyranny\_add |  |  |  | Character |
| dread\_per\_tyranny\_mult |  |  |  | Character |
| domain\_limit |  |  |  | Character |
| vassal\_limit |  |  |  | Character |
| domain\_tax\_mult |  |  |  | Character |
| domain\_tax\_same\_faith\_mult |  |  |  | Character |
| domain\_tax\_different\_faith\_mult |  |  |  | Character |
| domain\_tax\_mult\_even\_if\_baron |  |  |  | Character |
| domain\_tax\_same\_faith\_mult\_even\_if\_baron |  |  |  | Character |
| domain\_tax\_different\_faith\_mult\_even\_if\_baron |  |  |  | Character |
| vassal\_tax\_mult |  |  |  | Character |
| men\_at\_arms\_maintenance |  |  |  | Character |
| men\_at\_arms\_maintenance\_per\_dread\_mult |  |  |  | Character |
| army\_maintenance\_mult |  |  |  | Character |
| short\_reign\_duration\_mult |  |  |  | Character |
| long\_reign\_bonus\_mult |  |  |  | Character |
| diplomatic\_range\_mult |  |  |  | Character |
| inbreeding\_chance |  |  |  | Character |
| positive\_inactive\_inheritance\_chance |  |  |  | Character |
| negative\_inactive\_inheritance\_chance |  |  |  | Character |
| positive\_random\_genetic\_chance |  |  |  | Character |
| negative\_random\_genetic\_chance |  |  |  | Character |
| genetic\_trait\_strengthen\_chance |  |  |  | Character |
| life\_expectancy | Adds a number of years to the default life expectancy. | ```<br>character_modifier = {<br>    life_expectancy = 5 # Adds +5 years to expected old age death<br>}<br>``` |  | Character |
| years\_of\_fertility |  |  |  | Character |
| knight\_limit |  |  |  | Character |
| knight\_effectiveness\_mult |  |  |  | Character |
| title\_creation\_cost |  |  |  | Character |
| title\_creation\_cost\_mult |  |  |  | Character |
| monthly\_lifestyle\_xp\_gain\_mult |  |  |  | Character |
| mercenary\_hire\_cost\_add |  |  |  | Character |
| mercenary\_hire\_cost\_mult |  |  |  | Character |
| same\_culture\_mercenary\_hire\_cost\_add |  |  |  | Character |
| same\_culture\_mercenary\_hire\_cost\_mult |  |  |  | Character |
| holy\_order\_hire\_cost\_mult |  |  |  | Character |
| holy\_order\_hire\_cost\_add |  |  |  | Character |
| same\_culture\_holy\_order\_hire\_cost\_mult |  |  |  | Character |
| same\_culture\_holy\_order\_hire\_cost\_add |  |  |  | Character |
| opinion\_of\_female\_rulers |  |  | Character | Opinion |
| opinion\_of\_male\_rulers |  |  | Character | Opinion |
| opinion\_of\_same\_culture |  |  | Character | Opinion |
| opinion\_of\_different\_culture |  |  | Character | Opinion |
| opinion\_of\_same\_faith |  |  | Character | Opinion |
| opinion\_of\_different\_faith |  |  | Character | Opinion |
| opinion\_of\_liege |  |  | Character | Opinion |
| opinion\_of\_vassal |  |  | Character | Opinion |
| opinion\_of\_different\_faith\_liege |  |  | Character | Opinion |
| same\_culture\_opinion |  |  | Character | Opinion |
| different\_culture\_opinion |  |  | Character | Opinion |
| same\_faith\_opinion |  |  | Character | Opinion |
| different\_faith\_opinion |  |  | Character | Opinion |
| direct\_vassal\_opinion |  |  | Character | Opinion |
| fellow\_vassal\_opinion |  |  | Character | Opinion |
| independent\_ruler\_opinion |  |  | Character | Opinion |
| general\_opinion |  |  | Character | Opinion |
| attraction\_opinion |  |  | Character | Opinion |
| religious\_vassal\_opinion |  |  | Character | Opinion |
| religious\_head\_opinion |  |  | Character | Opinion |
| spouse\_opinion |  |  | Character | Opinion |
| twin\_opinion |  |  | Character | Opinion |
| close\_relative\_opinion |  |  | Character | Opinion |
| dynasty\_house\_opinion |  |  | Character | Opinion |
| dynasty\_opinion |  |  | Character | Opinion |
| liege\_opinion |  |  | Character | Opinion |
| different\_faith\_liege\_opinion |  |  | Character | Opinion |
| vassal\_opinion |  |  | Character | Opinion |
| clergy\_opinion |  |  | Character | Opinion |
| councillor\_opinion |  |  | Character | Opinion |
| realm\_priest\_opinion |  |  | Character | Opinion |
| powerful\_vassal\_opinion |  |  | Character | Opinion |
| courtier\_opinion |  |  | Character | Opinion |
| guest\_opinion |  |  | Character | Opinion |
| courtier\_and\_guest\_opinion |  |  | Character | Opinion |
| prisoner\_opinion |  |  | Character | Opinion |
| player\_heir\_opinion |  |  | Character | Opinion |
| child\_opinion |  |  | Character | Opinion |
| child\_except\_player\_heir\_opinion |  |  | Character | Opinion |
| eligible\_child\_opinion |  |  | Character | Opinion |
| eligible\_child\_except\_player\_heir\_opinion |  |  | Character | Opinion |
| ignore\_negative\_culture\_opinion |  |  | Character | Opinion |
| ignore\_different\_faith\_opinion |  |  | Character | Opinion |
| pursue\_efficiency |  |  |  | Combat |
| counter\_efficiency |  |  |  | Combat |
| min\_combat\_roll |  |  |  | Combat |
| max\_combat\_roll |  |  |  | Combat |
| men\_at\_arms\_limit | Affects size of individual regiments |  |  | Combat |
| men\_at\_arms\_cap | Affects total number of regiments possible |  |  | Combat |
| embarkation\_cost\_mult |  |  |  | Combat |
| naval\_movement\_speed\_mult |  |  |  | Combat |
| siege\_phase\_time |  |  |  | Siege |
| siege\_morale\_loss |  |  |  | Siege |
| revolting\_siege\_morale\_loss\_add |  |  |  | Siege |
| revolting\_siege\_morale\_loss\_mult |  |  |  | Siege |
| vassal\_tax\_contribution\_add |  |  |  | Government |
| vassal\_tax\_contribution\_mult |  |  |  | Government |
| intimidated\_vassal\_tax\_contribution\_add |  |  |  | Character |
| intimidated\_vassal\_tax\_contribution\_mult |  |  |  | Character |
| cowed\_vassal\_tax\_contribution\_add |  |  |  | Character |
| cowed\_vassal\_tax\_contribution\_mult |  |  |  | Character |
| vassal\_levy\_contribution\_add |  |  |  | Government |
| vassal\_levy\_contribution\_mult |  |  |  | Government |
| intimidated\_vassal\_levy\_contribution\_add |  |  |  | Character |
| intimidated\_vassal\_levy\_contribution\_mult |  |  |  | Character |
| cowed\_vassal\_levy\_contribution\_add |  |  |  | Character |
| cowed\_vassal\_levy\_contribution\_mult |  |  |  | Character |
| happy\_powerful\_vassal\_tax\_contribution\_add |  |  |  | Character |
| happy\_powerful\_vassal\_tax\_contribution\_mult |  |  |  | Character |
| happy\_powerful\_vassal\_levy\_contribution\_add |  |  |  | Character |
| happy\_powerful\_vassal\_levy\_contribution\_mult |  |  |  | Character |
| scheme\_power |  |  |  | Scheme |
| scheme\_resistance |  |  |  | Scheme |
| scheme\_secrecy |  |  |  | Scheme |
| scheme\_success\_chance |  |  |  | Scheme |
| hostile\_scheme\_power\_add |  |  |  | Character |
| hostile\_scheme\_power\_mult |  |  |  | Character |
| personal\_scheme\_power\_add |  |  |  | Character |
| personal\_scheme\_power\_mult |  |  |  | Character |
| hostile\_scheme\_resistance\_add |  |  |  | Character |
| hostile\_scheme\_resistance\_mult |  |  |  | Character |
| personal\_scheme\_resistance\_add |  |  |  | Character |
| personal\_scheme\_resistance\_mult |  |  |  | Character |
| diplomacy\_scheme\_power |  |  |  | Character |
| intrigue\_scheme\_power |  |  |  | Character |
| stewardship\_scheme\_power |  |  |  | Character |
| martial\_scheme\_power |  |  |  | Character |
| prowess\_scheme\_power |  |  |  | Character |
| learning\_scheme\_power |  |  |  | Character |
| diplomacy\_scheme\_resistance |  |  |  | Character |
| intrigue\_scheme\_resistance |  |  |  | Character |
| stewardship\_scheme\_resistance |  |  |  | Character |
| martial\_scheme\_resistance |  |  |  | Character |
| prowess\_scheme\_resistance |  |  |  | Character |
| learning\_scheme\_resistance |  |  |  | Character |
| scheme\_discovery\_chance\_mult |  |  |  | Character |
| max\_personal\_schemes\_add |  |  |  | Character |
| max\_hostile\_schemes\_add |  |  |  | Character |
| owned\_hostile\_scheme\_success\_chance\_add |  |  |  | Character |
| owned\_personal\_scheme\_success\_chance\_add |  |  |  | Character |
| enemy\_hostile\_scheme\_success\_chance\_add |  |  |  | Character |
| enemy\_personal\_scheme\_success\_chance\_add |  |  |  | Character |
| movement\_speed |  |  |  | Combat |
| retreat\_losses |  |  |  | Combat |
| hard\_casualty\_modifier |  |  |  | Combat |
| enemy\_hard\_casualty\_modifier |  |  |  | Combat |
| advantage |  |  |  | Combat |
| attacker\_advantage |  |  |  | Combat |
| defender\_advantage |  |  |  | Combat |
| enemy\_terrain\_advantage |  |  |  | Combat |
| tolerance\_advantage\_mod |  |  |  | Combat |
| advantage\_against\_coreligionists |  |  |  | Combat |
| random\_advantage |  |  |  | Combat |
| controlled\_province\_advantage |  |  | Character | Combat |
| no\_water\_crossing\_penalty |  |  |  | Combat |
| raid\_speed |  |  |  | Combat |
| hostile\_county\_attrition |  |  |  | Combat |
| supply\_duration |  |  |  | Combat |
| supply\_limit\_mult |  |  |  | Province |
| supply\_limit |  |  |  | Province |
| fort\_level |  |  |  | Province |
| supply\_capacity\_add |  |  |  | Province |
| supply\_capacity\_mult |  |  |  | Province |
| hostile\_raid\_time |  |  |  | Province |
| levy\_size |  |  |  | Holding |
| garrison\_size |  |  |  | Holding |
| levy\_reinforcement\_rate |  |  |  | Holding |
| levy\_reinforcement\_rate\_same\_faith |  |  |  | Character |
| levy\_reinforcement\_rate\_different\_faith |  |  |  | Character |
| levy\_reinforcement\_rate\_even\_if\_baron |  |  |  | Character |
| levy\_reinforcement\_rate\_same\_faith\_even\_if\_baron |  |  |  | Character |
| levy\_reinforcement\_rate\_different\_faith\_even\_if\_baron |  |  |  | Character |
| levy\_reinforcement\_rate\_friendly\_territory |  |  |  | Holding |
| tax\_mult |  |  |  | Holding |
| development\_growth\_factor |  |  |  | County |
| development\_growth |  |  |  | County |
| character\_capital\_county\_monthly\_development\_growth\_add |  |  |  | Character |
| monthly\_county\_control\_growth\_add |  |  | Character, Province, County | County |
| monthly\_county\_control\_growth\_factor |  |  | Character, Province, County | County |
| monthly\_county\_control\_growth\_add\_even\_if\_baron |  |  | Character | County |
| monthly\_county\_control\_growth\_factor\_even\_if\_baron |  |  | Character | County |
| monthly\_county\_control\_decline\_add |  |  | Character, Province, County | County |
| monthly\_county\_control\_decline\_factor |  |  | Character, Province, County | County |
| monthly\_county\_control\_decline\_add\_even\_if\_baron |  |  | Character | County |
| monthly\_county\_control\_decline\_factor\_even\_if\_baron |  |  | Character | County |
| county\_opinion\_add |  |  | Character, County | Opinion |
| different\_faith\_county\_opinion\_mult |  |  | Character | Opinion |
| county\_opinion\_add\_even\_if\_baron |  |  | Character | Opinion |
| different\_faith\_county\_opinion\_mult\_even\_if\_baron |  |  | Character | Opinion |
| mercenary\_count\_mult |  |  |  | Culture |
| cultural\_head\_fascination\_add |  |  |  | Character |
| cultural\_head\_fascination\_mult |  |  |  | Character |
| faith\_conversion\_piety\_cost\_add |  |  |  | Character |
| faith\_conversion\_piety\_cost\_mult |  |  |  | Character |
| faith\_creation\_piety\_cost\_add |  |  |  | Character |
| faith\_creation\_piety\_cost\_mult |  |  |  | Character |
| ai\_boldness |  |  |  | AI |
| ai\_compassion |  |  |  | AI |
| ai\_sociability |  |  |  | AI |
| ai\_greed |  |  |  | AI |
| ai\_energy |  |  |  | AI |
| ai\_honor |  |  |  | AI |
| ai\_rationality |  |  |  | AI |
| ai\_vengefulness |  |  |  | AI |
| ai\_zeal |  |  |  | AI |
| ai\_war\_chance |  |  |  | AI |
| ai\_war\_cooldown |  |  |  | AI |
| <culture>\_opinion |  | Works with modded cultures. | Character | Opinion |
| <faith>\_opinion |  | Works with modded faiths. | Character | Opinion |
| <religion>\_opinion |  | Works with modded religions. | Character | Opinion |
| <religion\_family>\_opinion |  | Works with modded religion families. | Character | Opinion |
| monthly\_<lifestyle>\_xp\_gain\_mult |  | Works with modded lifestyles. | Character | Character |
| court\_grandeur\_baseline\_add |  |  |  | Character |
| accolade\_glory\_gain\_mult |  |  | Character |  |
| active\_accolades |  |  | Character |  |
| additional\_fort\_level |  |  | Character, Province, County |  |
| ai\_amenity\_spending |  |  | Character |  |
| ai\_amenity\_target\_baseline |  |  | Character |  |
| army\_damage\_mult |  |  | Character |  |
| army\_pursuit\_mult |  |  | Character |  |
| army\_screen\_mult |  |  | Character |  |
| army\_siege\_value\_mult |  |  | Character |  |
| army\_toughness\_mult |  |  | Character |  |
| artifact\_decay\_reduction\_mult |  |  | Character, Province, County |  |
| building\_slot\_add |  |  | Character, Province, County |  |
| character\_travel\_safety |  |  | Character |  |
| character\_travel\_safety\_mult |  |  | Character |  |
| character\_travel\_speed |  |  | Character |  |
| character\_travel\_speed\_mult |  |  | Character |  |
| coastal\_advantage |  |  | Character |  |
| counter\_resistance |  |  | Character, Terrain |  |
| cultural\_acceptance\_gain\_mult |  |  | Culture |  |
| cultural\_head\_acceptance\_gain\_mult |  |  | Character |  |
| culture\_tradition\_max\_add |  |  | Character |  |
| defender\_holding\_advantage |  |  | Character, Province, County |  |
| defender\_winter\_advantage |  |  | Province |  |
| hard\_casualty\_winter |  |  | Province |  |
| hostile\_county\_attrition\_raiding |  |  | Character |  |
| ignore\_negative\_opinion\_of\_culture |  |  | Character | Opinion |
| ignore\_opinion\_of\_different\_faith |  |  | Character | Opinion |
| independent\_primary\_defender\_advantage\_add |  |  | Character |  |
| knight\_effectiveness\_per\_dread |  |  | Character |  |
| knight\_effectiveness\_per\_tyranny |  |  | Character |  |
| led\_by\_owner\_extra\_advantage\_add |  |  | Character |  |
| levy\_maintenance |  |  | Character |  |
| levy\_pursuit |  |  | Character |  |
| levy\_screen |  |  | Character |  |
| levy\_siege |  |  | Character |  |
| max\_loot\_mult |  |  | Character |  |
| men\_at\_arms\_recruitment\_cost |  |  | Character |  |
| monthly\_county\_control\_growth\_at\_war\_add |  |  | Character, Province, County |  |
| monthly\_county\_control\_growth\_at\_war\_factor |  |  | Character, Province, County |  |
| monthly\_county\_control\_decline\_at\_war\_add |  |  | Character, Province, County |  |
| monthly\_county\_control\_decline\_at\_war\_factor |  |  | Character, Province, County |  |
| monthly\_court\_grandeur\_change\_add |  |  | Character |  |
| monthly\_court\_grandeur\_change\_mult |  |  | Character |  |
| movement\_speed\_land\_raiding |  |  | Character |  |
| no\_disembark\_penalty |  |  | Character |  |
| opinion\_of\_parents |  |  | Character | Opinion |
| owned\_scheme\_secrecy\_add |  |  | Character |  |
| same\_heritage\_county\_advantage\_add |  |  | Character |  |
| stress\_loss\_per\_piety\_level |  |  | Character |  |
| stress\_loss\_per\_prestige\_level |  |  | Character |  |
| strife\_opinion\_gain\_mult |  |  | Character | Opinion |
| strife\_opinion\_loss\_mult |  |  | Character | Opinion |
| supply\_loss\_winter |  |  | Province |  |
| travel\_companion\_opinion |  |  | Character | Opinion |
| travel\_danger |  |  | Character, Province, County |  |
| travel\_safety\_mult |  |  | Travel Plan |  |
| travel\_safety |  |  | Travel Plan |  |
| travel\_speed\_mult |  |  | Travel Plan |  |
| travel\_speed |  |  | Travel Plan |  |
| uncontrolled\_province\_advantage |  |  | Character |  |
| winter\_advantage |  |  | Character |  |
| winter\_movement\_speed |  |  | Character |  |
| <trait>\_xp\_degradation\_mult |  | Works with modded traits. | Character | Traits |
| <trait>\_xp\_gain\_mult |  | Works with modded traits. | Character | Traits |
| <trait>\_xp\_loss\_mult |  | Works with modded traits. | Character | Traits |
| trait\_track\_<track>\_xp\_degradation\_mult |  | Works with modded traits. | Character | Traits |
| trait\_track\_<track>\_xp\_gain\_mult |  | Works with modded traits. | Character | Traits |
| trait\_track\_<track>\_xp\_loss\_mult |  | Works with modded traits. | Character | Traits |
| <region>\_development\_growth |  | Only works with regions that have `generates_modifiers = yes` | Character, Province, County | Development |
| <region>\_development\_growth\_factor |  | Only works with regions that have `generates_modifiers = yes` | Character, Province, County | Development |
| legitimacy\_baseline\_add |  |  | Character | Character |
| legitimacy\_gain\_mult |  |  | Character | Character |
| legitimacy\_loss\_mult |  |  | Character | Character |
| monthly\_legitimacy\_add |  |  | Character | Character |
| monthly\_prestige\_gain\_per\_legitimacy\_level\_add |  |  | Character | Character |
| monthly\_prestige\_gain\_per\_legitimacy\_level\_mult |  |  | Character | Character |
| monthly\_piety\_gain\_per\_legitimacy\_level\_add |  |  | Character | Character |
| monthly\_piety\_gain\_per\_legitimacy\_level\_mult |  |  | Character | Character |
| owned\_legend\_spread\_add |  |  | Character | Character |
| owned\_legend\_spread\_mult |  |  | Character | Character |

### Vassal Stance Related Modifiers\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Modifier_list&veaction=edit&section=4 "Edit section: Vassal Stance Related Modifiers") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Modifier_list&action=edit&section=4 "Edit section: Vassal Stance Related Modifiers")\]

These modifiers affect the opinions and contributions of vassals with certain stances towards their lieges. The syntax is given in the table below and valid values for <vassal\_stance> are: _**courtly, glory\_hound, parochial, zealot, minority, barons\_and\_minor\_landholders**_, plus any vassal stances you have modded in `common/vassal_stances`.

| Name | Description | Usage | Supported Scopes | Category |
| --- | --- | --- | --- | --- |
| <vassal\_stance>\_opinion |  |  | Character | Opinion |
| <vassal\_stance>\_different\_culture\_opinion |  |  | Character | Opinion |
| <vassal\_stance>\_different\_faith\_opinion |  |  | Character | Opinion |
| <vassal\_stance>\_same\_culture\_opinion |  |  | Character | Opinion |
| <vassal\_stance>\_same\_faith\_opinion |  |  | Character | Opinion |
| <vassal\_stance>\_levy\_contribution\_add |  |  | Character | Government |
| <vassal\_stance>\_levy\_contribution\_mult |  |  | Character | Government |
| <vassal\_stance>\_tax\_contribution\_add |  |  | Character | Government |
| <vassal\_stance>\_tax\_contribution\_mult |  |  | Character | Government |

### Government Related Modifiers\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Modifier_list&veaction=edit&section=5 "Edit section: Government Related Modifiers") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Modifier_list&action=edit&section=5 "Edit section: Government Related Modifiers")\]

These modifiers affect the opinions and contributions of characters of certain governments towards other characters. The syntax is given in the table below and valid values for <government\_name> are: _**feudal\_government, republic\_government, theocracy\_government, clan\_government, tribal\_government, mercenary\_government, holy\_order\_government**_, plus any government types you have modded in `common/governments`.

| Name | Description | Usage | Supported Scopes | Category |
| --- | --- | --- | --- | --- |
| <government\_name>\_opinion |  |  | Character | Opinion |
| <government\_name>\_vassal\_opinion |  |  | Character | Opinion |
| <government\_name>\_opinion\_same\_faith |  |  | Character | Opinion |
| <government\_name>\_tax\_contribution\_add |  |  | Character | Government |
| <government\_name>\_tax\_contribution\_mult |  |  | Character | Government |
| <government\_name>\_levy\_contribution\_add |  |  | Character | Government |
| <government\_name>\_levy\_contribution\_mult |  |  | Character | Government |

### Holding-type Related Modifiers\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Modifier_list&veaction=edit&section=6 "Edit section: Holding-type Related Modifiers") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Modifier_list&action=edit&section=6 "Edit section: Holding-type Related Modifiers")\]

These modifiers affect the build cost and speed of (and in) the different holding types. The syntax is given in the table below and valid values for <holding> are: _**castle\_holding, city\_holding, church\_holding, tribal\_holding**_, plus any holding types you have modded in `common/holdings`. Note that since the holding types already end with `_holding`, some of these modifiers will have `_holding_holding_` in them. That is normal.

-

| Name | Description | Usage | Supported Scopes | Category |
| --- | --- | --- | --- | --- |
| <holding>\_build\_speed |  |  |  | Character, Province, County |
| <holding>\_build\_gold\_cost |  |  |  | Character, Province, County |
| <holding>\_build\_piety\_cost |  |  |  | Character, Province, County |
| <holding>\_build\_prestige\_cost |  |  |  | Character, Province, County |
| <holding>\_holding\_build\_speed |  |  |  | Character, Province, County |
| <holding>\_holding\_build\_gold\_cost |  |  |  | Character, Province, County |
| <holding>\_holding\_build\_piety\_cost |  |  |  | Character, Province, County |
| <holding>\_holding\_build\_prestige\_cost |  |  |  | Character, Province, County |
| build\_speed |  |  |  | Character, Province, County |
| build\_gold\_cost |  |  |  | Character, Province, County |
| build\_piety\_cost |  |  |  | Character, Province, County |
| build\_prestige\_cost |  |  |  | Character, Province, County |
| holding\_build\_speed |  |  |  | Character, Province, County |
| holding\_build\_gold\_cost |  |  |  | Character, Province, County |
| holding\_build\_piety\_cost |  |  |  | Character, Province, County |
| holding\_build\_prestige\_cost |  |  |  | Character, Province, County |

### Scheme Related Modifiers\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Modifier_list&veaction=edit&section=7 "Edit section: Scheme Related Modifiers") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Modifier_list&action=edit&section=7 "Edit section: Scheme Related Modifiers")\]

These modifiers affect the schemes of characters. The syntax is given in the table below and valid values for <scheme\_name> are: _**abduct, befriend, claim\_throne, convert\_to\_witchcraft, courting, elope, fabricate\_hook, murder, seduce, sway**_, plus any schemes you have modded in `common/schemes`. If the player has got the [Royal Court](https://ck3.paradoxwikis.com/Royal_Court_(DLC) "Royal Court (DLC)") DLC active there are also **learn\_language** add **steal\_back\_artifact** schemes.

| Name | Description | Usage | Supported Scopes | Category |
| --- | --- | --- | --- | --- |
| max\_<scheme\_name>\_schemes\_add |  |  | Character | Scheme |
| <scheme\_name>\_scheme\_power\_add |  |  | Character | Scheme |
| <scheme\_name>\_scheme\_power\_mult |  |  | Character | Scheme |
| <scheme\_name>\_scheme\_resistance\_add |  |  | Character | Scheme |
| <scheme\_name>\_scheme\_resistance\_mult |  |  | Character | Scheme |
| scheme\_power\_against\_<relation>\_add |  | Works with modded relations. | Character | Scheme |
| scheme\_power\_against\_<relation>\_mult |  | Works with modded relations. | Character | Scheme |

### Terrain Modifiers\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Modifier_list&veaction=edit&section=8 "Edit section: Terrain Modifiers") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Modifier_list&action=edit&section=8 "Edit section: Terrain Modifiers")\]

These modifiers change the effects of the different terrains. The syntax is given in the table below and valid values for <terrain\_name> are: _**plains, farmlands, hills, mountains, desert, desert\_mountains, oasis, jungle, forest, taiga, wetlands, steppe, floodplains, drylands**_, plus any types you have modded in `common/terrain_types`.

| Name | Description | Usage | Supported Scopes | Category |
| --- | --- | --- | --- | --- |
| <terrain\_name>\_attrition\_mult |  |  | Character | Combat |
| <terrain\_name>\_cancel\_negative\_supply |  |  | Character | Combat |
| <terrain\_name>\_advantage |  |  | Character | Combat |
| <terrain\_name>\_min\_combat\_roll |  |  | Character | Combat |
| <terrain\_name>\_max\_combat\_roll |  |  | Character | Combat |
| <terrain>\_development\_growth |  |  | Character, Province, County | Development |
| <terrain>\_development\_growth\_factor |  |  | Character, Province, County | Development |
| <terrain>\_holding\_construction\_gold\_cost |  |  | Character, Province, County | Construction |
| <terrain>\_holding\_construction\_piety\_cost |  |  | Character, Province, County | Construction |
| <terrain>\_holding\_construction\_prestige\_cost |  |  | Character, Province, County | Construction |
| <terrain>\_construction\_gold\_cost |  |  | Character, Province, County | Construction |
| <terrain>\_construction\_piety\_cost |  |  | Character, Province, County | Construction |
| <terrain>\_construction\_prestige\_cost |  |  | Character, Province, County | Construction |
| <terrain>\_supply\_limit |  |  | Character, Province, County | Combat |
| <terrain>\_supply\_limit\_mult |  |  | Character, Province, County | Combat |
| <terrain>\_levy\_size |  |  | Character, Province, County | Combat |
| <terrain>\_travel\_danger |  |  | Character, Province, County | Travel |
| <terrain>\_tax\_mult |  |  | Character, Province, County | Government |

### Men-at-Arms Related Modifiers\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Modifier_list&veaction=edit&section=9 "Edit section: Men-at-Arms Related Modifiers") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Modifier_list&action=edit&section=9 "Edit section: Men-at-Arms Related Modifiers")\]

These modifiers affect the size and efficacy of Men-at-Arms units of a character. The syntax is given in the table below and valid values for <men\_at\_arms\_name> are: _**heavy\_infantry, pikemen, archers, light\_cavalry, heavy\_cavalry, archer\_cavalry, camel\_cavalry, elephant\_cavalry, skirmishers, siege\_weapon**_, plus any types you have modded in `common/men_at_arms_types/`.

| Name | Description | Usage | Supported Scopes | Category |
| --- | --- | --- | --- | --- |
| <men\_at\_arms\_name>\_maintenance\_cost\_mult |  |  |  | Character |
| <men\_at\_arms\_name>\_recruitment\_cost\_mult |  |  |  | Character |
| <men\_at\_arms\_name>\_max\_size\_add |  |  |  | Character |
| <men\_at\_arms\_name>\_max\_size\_mult |  |  |  | Character |
| <men\_at\_arms\_name>\_siege\_value\_add |  |  |  | Character |
| <men\_at\_arms\_name>\_siege\_value\_mult |  |  |  | Character |
| <men\_at\_arms\_name>\_damage\_add |  |  |  | Character |
| <men\_at\_arms\_name>\_damage\_mult |  |  |  | Character |
| <men\_at\_arms\_name>\_toughness\_add |  |  |  | Character |
| <men\_at\_arms\_name>\_toughness\_mult |  |  |  | Character |
| <men\_at\_arms\_name>\_pursuit\_add |  |  |  | Character |
| <men\_at\_arms\_name>\_pursuit\_mult |  |  |  | Character |
| <men\_at\_arms\_name>\_screen\_add |  |  |  | Character |
| <men\_at\_arms\_name>\_screen\_mult |  |  |  | Character |
| maa\_siege\_value\_add |  |  |  | Character |
| maa\_siege\_value\_mult |  |  |  | Character |
| maa\_damage\_add |  |  |  | Character |
| maa\_damage\_mult |  |  |  | Character |
| maa\_toughness\_add |  |  |  | Character |
| maa\_toughness\_mult |  |  |  | Character |
| maa\_pursuit\_add |  |  |  | Character |
| maa\_pursuit\_mult |  |  |  | Character |
| maa\_screen\_add |  |  |  | Character |
| maa\_screen\_mult |  |  |  | Character |
| stationed\_<men\_at\_arms\_name>\_siege\_value\_add |  |  |  | Province |
| stationed\_<men\_at\_arms\_name>\_siege\_value\_mult |  |  |  | Province |
| stationed\_<men\_at\_arms\_name>\_damage\_add |  |  |  | Province |
| stationed\_<men\_at\_arms\_name>\_damage\_mult |  |  |  | Province |
| stationed\_<men\_at\_arms\_name>\_toughness\_add |  |  |  | Province |
| stationed\_<men\_at\_arms\_name>\_toughness\_mult |  |  |  | Province |
| stationed\_<men\_at\_arms\_name>\_pursuit\_add |  |  |  | Province |
| stationed\_<men\_at\_arms\_name>\_pursuit\_mult |  |  |  | Province |
| stationed\_<men\_at\_arms\_name>\_screen\_add |  |  |  | Province |
| stationed\_<men\_at\_arms\_name>\_screen\_mult |  |  |  | Province |
| stationed\_maa\_siege\_value\_add |  |  |  | Province |
| stationed\_maa\_siege\_value\_mult |  |  |  | Province |
| stationed\_maa\_damage\_add |  |  |  | Province |
| stationed\_maa\_damage\_mult |  |  |  | Province |
| stationed\_maa\_toughness\_add |  |  |  | Province |
| stationed\_maa\_toughness\_mult |  |  |  | Province |
| stationed\_maa\_pursuit\_add |  |  |  | Province |
| stationed\_maa\_pursuit\_mult |  |  |  | Province |
| stationed\_maa\_screen\_add |  |  |  | Province |
| stationed\_maa\_screen\_mult |  |  |  | Province |

**[Modding](https://ck3.paradoxwikis.com/Modding "Modding")**

|     |     |
| --- | --- |
| Documentation | [Scripting](https://ck3.paradoxwikis.com/Scripting "Scripting") • [Scopes](https://ck3.paradoxwikis.com/Scopes "Scopes") • [Effects](https://ck3.paradoxwikis.com/Effects "Effects") • [Triggers](https://ck3.paradoxwikis.com/Triggers "Triggers") • [Variables](https://ck3.paradoxwikis.com/Variables "Variables") • Modifiers |

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

Retrieved from " [https://ck3.paradoxwikis.com/index.php?title=Modifier\_list&oldid=27588](https://ck3.paradoxwikis.com/index.php?title=Modifier_list&oldid=27588)"

[Categories](https://ck3.paradoxwikis.com/Special:Categories "Special:Categories"):

- [Potentially outdated](https://ck3.paradoxwikis.com/Category:Potentially_outdated "Category:Potentially outdated")
- [1.12](https://ck3.paradoxwikis.com/Category:1.12 "Category:1.12")
- [Modding](https://ck3.paradoxwikis.com/Category:Modding "Category:Modding")