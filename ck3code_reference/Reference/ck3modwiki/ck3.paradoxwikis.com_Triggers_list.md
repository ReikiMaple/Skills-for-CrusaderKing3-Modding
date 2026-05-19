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

# Triggers list

From CK3 Wiki

[Jump to navigation](https://ck3.paradoxwikis.com/Triggers_list#mw-head) [Jump to search](https://ck3.paradoxwikis.com/Triggers_list#searchInput)

_Main article: [Triggers](https://ck3.paradoxwikis.com/Triggers "Triggers")_

triggers.log is a documentation provided by the game, which contains all code triggers that can be used.

You can dump it locally on your computer by using the console command `script_docs` which will create it in Documents/Paradox Interactive/Crusader Kings III/logs/

The file needs to be generated again after each major patch to get the latest version.

The list is transcribed here, but be aware that it is outdated.
Some triggers have been deprecated, and some triggers added after launch are missing.

| Name | Description | Usage | Traits | Supported Scopes | Supported Targets |
| --- | --- | --- | --- | --- | --- |
| all\_court\_artifact\_slots | check if all the scoped characters court artifact slots are empty or full |  |  | character |  |
| all\_inventory\_artifact\_slots | check if all the scoped characters inventory artifact slots are empty or full |  |  | character |  |
| amenity\_level | Compares the scoped character's amenity level in the given type to the given value | ```<br>amenity_level = { target = court_food_quality value > 2 }<br>(It is "target" instead of "type" hereafter. "type" has been decommissioned.)<br>``` |  | character | <, <=, =, !=, >, >= |
| any\_artifact | Iterate through all existing artifacts | ```<br>any_artifact = { <count=num/all> / <percent=fixed_point> <triggers> }<br>``` |  | none | artifact |
| any\_artifact\_claimant | Iterate through all characters with a claim on the scoped artifact | ```<br>any_artifact_claimant = { <count=num/all> / <percent=fixed_point> <triggers> }<br>``` |  | artifact | character |
| any\_artifact\_house\_claimant | Iterate through all dynasty houses with a claim on the scoped artifact | ```<br>any_artifact_house_claimant = { <count=num/all> / <percent=fixed_point> <triggers> }<br>``` |  | artifact | dynasty house |
| any\_character\_artifact | Iterate through all artifacts in a given characters inventory | ```<br>any_character_artifact = { <count=num/all> / <percent=fixed_point> <triggers> }<br>``` |  | character | artifact |
| any\_character\_struggle | Iterate through all struggles that character is involved in. Optional: Narrow down the involvement status \*\_character\_struggle = { involvement = involved \| interloper } | ```<br>any_character_struggle = { <count=num/all> / <percent=fixed_point> <triggers> }<br>``` |  | character | struggle |
| any\_character\_with\_royal\_court | Iterate through all characters with a royal court | ```<br>any_character_with_royal_court = { <count=num/all> / <percent=fixed_point> <triggers> }<br>``` |  | none | character |
| any\_claimed\_artifact | Iterate through all claimed artifacts of the scoped character | ```<br>any_claimed_artifact = { <count=num/all> / <percent=fixed_point> <triggers> }<br>``` |  | character | artifact |
| any\_controlled\_faith | Iterate through all faiths headed by a title | ```<br>any_controlled_faith = { <count=num/all> / <percent=fixed_point> <triggers> }<br>``` |  | landed title | faith |
| any\_county\_struggle | Iterate through all struggles that a county is involved in. | ```<br>any_county_struggle = { <count=num/all> / <percent=fixed_point> <triggers> }<br>``` |  | landed title | struggle |
| any\_court\_position\_employer | Iterates through all characters that employ the scoped character in any court position. | ```<br>any_court_position_employer = { <count=num/all> / <percent=fixed_point> <triggers> }<br>``` |  | character | character |
| any\_court\_position\_holder | Iterates through all characters employed by the scoped character in the target court position. | ```<br>any_court_position_holder = { <count=num/all> / <percent=fixed_point> <triggers> }<br>``` |  | character | character |
| any\_culture\_county | Iterate through all counties of the culture | ```<br>any_culture_county = { <count=num/all> / <percent=fixed_point> <triggers> }<br>``` |  | culture | landed title |
| any\_culture\_duchy | Iterate through all duchies of the culture (duchies with at least one county of the culture | ```<br>any_culture_duchy = { <count=num/all> / <percent=fixed_point> <triggers> }<br>``` |  | culture | landed title |
| any\_culture\_empire | Iterate through all empires of the culture (empires with at least one county of the culture | ```<br>any_culture_empire = { <count=num/all> / <percent=fixed_point> <triggers> }<br>``` |  | culture | landed title |
| any\_culture\_global | Iterate through all cultures in the game | ```<br>any_culture_global = { <count=num/all> / <percent=fixed_point> <triggers> }<br>``` |  | none | culture |
| any\_culture\_kingdom | Iterate through all kingdoms of the culture (kingdoms with at least one county of the culture | ```<br>any_culture_kingdom = { <count=num/all> / <percent=fixed_point> <triggers> }<br>``` |  | culture | landed title |
| any\_de\_jure\_county | Iterate through all counties within this dejure title | ```<br>any_de_jure_county = { <count=num/all> / <percent=fixed_point> <triggers> }<br>``` |  | landed title | landed title |
| any\_direct\_de\_facto\_vassal\_title | Iterate through all de facto vassal titles | ```<br>any_direct_de_facto_vassal_title = { <count=num/all> / <percent=fixed_point> <triggers> }<br>``` |  | landed title | landed title |
| any\_direct\_de\_jure\_vassal\_title | Iterate through the all de jure vassals titles | ```<br>any_direct_de_jure_vassal_title = { <count=num/all> / <percent=fixed_point> <triggers> }<br>``` |  | landed title | landed title |
| any\_equipped\_character\_artifact | Iterate through all equipped artifacts in a given characters inventory | ```<br>any_equipped_character_artifact = { <count=num/all> / <percent=fixed_point> <triggers> }<br>``` |  | character | artifact |
| any\_faith\_character | Iterate through characters of the scoped faith | ```<br>any_faith_character = { <count=num/all> / <percent=fixed_point> <triggers> }<br>``` |  | faith | character |
| any\_faith\_playable\_ruler | Iterate through playable rulers of the scoped faith | ```<br>any_faith_playable_ruler = { <count=num/all> / <percent=fixed_point> <triggers> }<br>``` |  | faith | character |
| any\_faith\_ruler | Iterate through rulers of the scoped faith | ```<br>any_faith_ruler = { <count=num/all> / <percent=fixed_point> <triggers> }<br>``` |  | faith | character |
| any\_house\_claimed\_artifact | Iterate through all claimed artifacts of the scoped house | ```<br>any_house_claimed_artifact = { <count=num/all> / <percent=fixed_point> <triggers> }<br>``` |  | dynasty house | artifact |
| any\_inspiration | Iterate through all inspirations in the world | ```<br>any_inspiration = { <count=num/all> / <percent=fixed_point> <triggers> }<br>``` |  | none | inspiration |
| any\_inspired\_character | Iterate through all characters with an inspirations in the world | ```<br>any_inspired_character = { <count=num/all> / <percent=fixed_point> <triggers> }<br>``` |  | none | character |
| any\_interloper\_ruler | Iterate through all characters that are interloper in a struggle. | ```<br>any_interloper_ruler = { <count=num/all> / <percent=fixed_point> <triggers> }<br>``` |  | struggle | character |
| any\_involved\_ruler | Iterate through all characters that are involved in a struggle. | ```<br>any_involved_ruler = { <count=num/all> / <percent=fixed_point> <triggers> }<br>``` |  | struggle | character |
| any\_killed\_character | Iterate through all kills of a character | ```<br>any_killed_character = { <count=num/all> / <percent=fixed_point> <triggers> }<br>``` |  | character, artifact | character |
| any\_memory | Iterate through all memories of a character | ```<br>any_memory = { <count=num/all> / <percent=fixed_point> <triggers> }<br>``` |  | character | character memory |
| any\_memory\_participant | Iterate through all participating character of a memory | ```<br>any_memory_participant = { <count=num/all> / <percent=fixed_point> <triggers> }<br>``` |  | character memory | character |
| any\_opposite\_sex\_spouse\_candidate | Iterate through all the spouse candidates of the opposite sex of a character. | ```<br>WARNING: THIS IS VERY SLOW DO NOT DO IT OFTEN.<br>any_opposite_sex_spouse_candidate = { <count=num/all> / <percent=fixed_point> <triggers> }<br>``` |  | character | character |
| any\_parent\_culture | Iterate through all parent cultures | ```<br>any_parent_culture = { <count=num/all> / <percent=fixed_point> <triggers> }<br>``` |  | culture | culture |
| any\_parent\_culture\_or\_above | Iterate through all parent cultures or above | ```<br>any_parent_culture_or_above = { <count=num/all> / <percent=fixed_point> <triggers> }<br>``` |  | culture | culture |
| any\_past\_holder | Iterate through all past owners of a title from earliest to latest | ```<br>any_past_holder = { <count=num/all> / <percent=fixed_point> <triggers> }<br>``` |  | landed title | character |
| any\_past\_holder\_reversed | Iterate through all past owners of a title from latest to earliest | ```<br>any_past_holder_reversed = { <count=num/all> / <percent=fixed_point> <triggers> }<br>``` |  | landed title | character |
| any\_personal\_claimed\_artifact | Iterate through all personally claimed artifacts of the scoped character | ```<br>any_personal_claimed_artifact = { <count=num/all> / <percent=fixed_point> <triggers> }<br>``` |  | character | artifact |
| any\_played\_character | Iterate through all characters the player playing this character has played. Matches the game over legacy, except for excluding the currently played character | ```<br>any_played_character = { <count=num/all> / <percent=fixed_point> <triggers> }<br>``` |  | character | character |
| any\_powerful\_vassal | Iterate through the all powerful vassals of a character | ```<br>any_powerful_vassal = { <count=num/all> / <percent=fixed_point> <triggers> }<br>``` |  | character | character |
| any\_same\_sex\_spouse\_candidate | Iterate through all the spouse candidates of the same sex of a character. | ```<br>WARNING: THIS IS VERY SLOW DO NOT DO IT OFTEN.<br>any_same_sex_spouse_candidate = { <count=num/all> / <percent=fixed_point> <triggers> }<br>``` |  | character | character |
| any\_sponsored\_inspiration | Iterate through all sponsored inspirations | ```<br>any_sponsored_inspiration = { <count=num/all> / <percent=fixed_point> <triggers> }<br>``` |  | character | inspiration |
| aptitude | What is the scoped character's aptitude in the target court position type? aptitude = { court\_position = court\_position\_type value >= 1 } |  |  | character | <, <=, =, !=, >, >= |
| artifact\_durability | does this artifact have the required durability? |  |  | artifact | <, <=, =, !=, >, >= |
| artifact\_max\_durability | does this artifact have the required max durability? |  |  | artifact | <, <=, =, !=, >, >= |
| artifact\_slot\_type | is the artifact of the given inventory slot type? |  |  | artifact |  |
| artifact\_type | is the artifact of the given type? |  |  | artifact |  |
| average\_amenity\_level | average\_amenity\_level >= 3 | ```<br>Compares the scoped character's average amenity level to the given value, you probably never want to check for direct equality since the average will be some decimal number<br>``` |  | character | <, <=, =, !=, >, >= |
| base\_inspiration\_gold\_cost | base\_inspiration\_gold\_cost > 5 | ```<br>Gets the base gold cost of the scoped inspiration<br>``` |  | inspiration | <, <=, =, !=, >, >= |
| can\_be\_claimed\_by | Can the scoped artifact be claimed by the given character? |  |  | artifact | character |
| can\_be\_employed\_as | can the scoped character be employed as target court position type? |  |  | character |  |
| can\_benefit\_from\_artifact | Can the scoped character benefit from the main bonuses of this artifact? |  |  | character | artifact |
| can\_declare\_war | Can the scoped character declare war on the defender with the specified casus bellis on the defender character for the target titles with an optional claimant. can\_declare\_war = { defender = X casus\_belli = Y target\_titles = { Z } claimant = A } |  |  | character |  |
| can\_disband\_army | Can we disband this army? |  |  | army | yes/no |
| can\_diverge | Can this ruler diverge their culture? Includes checking the cost |  |  | character | yes/no |
| can\_diverge\_excluding\_cost | Can this ruler diverge their culture? Does not check the cost |  |  | character | yes/no |
| can\_employ\_court\_position\_type | can the scoped character employ the target court position type? |  |  | character |  |
| can\_equip\_artifact | Can the scoped character equip given artifact? |  |  | character | artifact |
| can\_fire\_position | Check if the scope task's councillor can be fired. Will check both can\_fire and things like it being illegal to reassing the position | ```<br>scope:task = { position_can_be_fired = yes }<br>``` |  | council task | yes/no |
| can\_hybridize | Can this ruler hybridize with the target culture? Includes checking the cost |  |  | character | culture |
| can\_hybridize\_excluding\_cost | Can this ruler hybridize with the target culture? Does not check the cost |  |  | character | culture |
| can\_sponsor\_inspiration | can\_sponsor\_inspiration = inspiration | ```<br>Can the scoped character sponsor the target inspiration<br>``` |  | character | inspiration |
| category | is the scoped artifact of given category? |  |  | artifact |  |
| court\_grandeur\_base | Gets the base court grandeur value for a character, always NRoyalCourt::COURT\_GRANDEUR\_MIN for those without one |  |  | character | <, <=, =, !=, >, >= |
| court\_grandeur\_current | Gets the current court grandeur value for a character, always NRoyalCourt::COURT\_GRANDEUR\_MIN for those without one |  |  | character | <, <=, =, !=, >, >= |
| court\_grandeur\_current\_level | Gets the current court grandeur level for a character, always 0 for those without one |  |  | character | <, <=, =, !=, >, >= |
| court\_grandeur\_minimum\_expected | Gets the minimum expected court grandeur value for a character, always NRoyalCourt::COURT\_GRANDEUR\_MIN for those without one |  |  | character | <, <=, =, !=, >, >= |
| court\_grandeur\_minimum\_expected\_level | Gets the minimum expected court grandeur level for a character, always 0 for those without one |  |  | character | <, <=, =, !=, >, >= |
| court\_positions\_currently\_available | How many court positions the scope character CAN currently employs |  |  | character | <, <=, =, !=, >, >= |
| court\_positions\_currently\_filled | How many court positions the scope character currently employs |  |  | character | <, <=, =, !=, >, >= |
| cultural\_acceptance | The cultural acceptance of the scoped culture with the target culture | ```<br>cultural_acceptance = { target = culture value > 50 }<br>``` |  | culture | <, <=, =, !=, >, >= |
| culture\_age | Checks the age of the scope culture in years. If the culture has no creation date set, this will simply return the current year | ```<br>culture_age >= 200<br>``` |  | culture | <, <=, =, !=, >, >= |
| culture\_number\_of\_counties | How many counties are there of this culture? | ```<br>culture_number_of_counties > 10<br>``` |  | culture | <, <=, =, !=, >, >= |
| culture\_overlaps\_geographical\_region | Checks if any county with this culture is in the given geographical region |  |  | culture |  |
| current\_day | Compare the current ingame day \[1, 31\] |  |  | none | <, <=, =, !=, >, >= |
| current\_military\_strength | Is the scoped character's current military strength this big? |  |  | character | <, <=, =, !=, >, >= |
| current\_year | Compare the current ingame year |  |  | none | <, <=, =, !=, >, >= |
| days\_as\_ruler | Number of days this character has been a ruler, returns -1 if character isn't a ruler |  |  | character | <, <=, =, !=, >, >= |
| days\_since\_creation | Gets the days since creation of the scoped inspiration | ```<br>days_since_creation > 5<br>``` |  | inspiration | <, <=, =, !=, >, >= |
| days\_since\_death | number of days since the character has died. |  |  | character | <, <=, =, !=, >, >= |
| days\_since\_joined\_court | Gets the days since scoped character joined their current court | ```<br>days_since_joined_court > 5<br>``` |  | character | <, <=, =, !=, >, >= |
| days\_since\_sponsorship | Gets the days since sponsorship started of the scoped inspiration | ```<br>days_since_sponsorship > 5<br>``` |  | inspiration | <, <=, =, !=, >, >= |
| debt\_level | Is the scoped character's debt level this value? -1 if not meeting any debt level threshold. 0 for the first one, and so on. Note that this might not match exactly with the modifier in effect as it calculates what the modifier will be now, and the character's actual modifier can lag behind |  |  | character | <, <=, =, !=, >, >= |
| debug\_log | Log whether the parent trigger succeeded or failed |  |  | none |  |
| debug\_log\_details | Log whether the parent trigger succeeded or failed. Log which children succeeded or failed |  |  | none |  |
| diplomacy\_lifestyle\_unlockable\_perks | How many perks from this lifestyle can the character currently unlock? This checks that they have the parent perks, and that the can\_be\_picked is met. It doesn't check perk points |  |  | character | <, <=, =, !=, >, >= |
| discontent\_per\_month | How much is the Faction's Discontent increasing each month? |  |  | faction | <, <=, =, !=, >, >= |
| domain\_size\_excluding\_grace\_period | Is the scoped character's domain this big? Does not count titles currently in the grace period |  |  | character | <, <=, =, !=, >, >= |
| dynasty\_num\_unlocked\_perks | does the dynasty has the required number of unlocked dynasty perks? |  |  | dynasty | <, <=, =, !=, >, >= |
| employs\_court\_position | is the scoped character employing a target court position type? |  |  | character |  |
| ep1\_culture\_legacy\_track\_perks | How many perks in the lifestyle does this dynasty have? |  |  | dynasty | <, <=, =, !=, >, >= |
| fp1\_adventure\_legacy\_track\_perks | How many perks in the lifestyle does this dynasty have? |  |  | dynasty | <, <=, =, !=, >, >= |
| fp1\_pillage\_legacy\_track\_perks | How many perks in the lifestyle does this dynasty have? |  |  | dynasty | <, <=, =, !=, >, >= |
| fp2\_coterie\_legacy\_track\_perks | How many perks in the lifestyle does this dynasty have? |  |  | dynasty | <, <=, =, !=, >, >= |
| fp2\_urbanism\_legacy\_track\_perks | How many perks in the lifestyle does this dynasty have? |  |  | dynasty | <, <=, =, !=, >, >= |
| has\_any\_artifact | does the scoped character have any artifacts? |  |  | character | yes/no |
| has\_any\_artifact\_claim | does the scoped character have any artifact claims at all? ( CHEAP ) |  |  | character | yes/no |
| has\_any\_court\_position | does the scoped character have any court positions? |  |  | character | yes/no |
| has\_any\_unequipped\_artifact | does the scoped character have any unequipped artifacts? |  |  | character | yes/no |
| has\_artifact\_claim | Does the scoped character have a personal or house claim on the target artifact |  |  | character | artifact |
| has\_artifact\_feature | Does the artifact have the given feature? | ```<br>has_artifact_feature = key<br>``` |  | artifact |  |
| has\_artifact\_feature\_group | Does the artifact have the given feature group? | ```<br>has_artifact_feature_group = key<br>``` |  | artifact |  |
| has\_artifact\_modifier | Does the artifact have the given modifier? | ```<br>has_artifact_modifier  = key<br>``` |  | artifact |  |
| has\_building\_gfx | Does the culture have this building gfx? | ```<br><culture> = { has_building_gfx = mena_building_gfx }<br>``` |  | culture |  |
| has\_clothing\_gfx | Does the culture have this clothing gfx? | ```<br><culture> = { has_clothing_gfx = mena_clothing_gfx }<br>``` |  | culture |  |
| has\_coa\_gfx | Does the culture have this CoA gfx? | ```<br><culture> = { has_coa_gfx = mena_coa_gfx }<br>``` |  | culture |  |
| has\_completed\_inspiration | Checks if the scoped character has ever completed an inspiration | ```<br>has_completed_inspiration = bool<br>``` |  | character | yes/no |
| has\_court\_language | Is the character's court language the given language? | ```<br>has_court_language = language_norwegian<br>``` |  | character |  |
| has\_court\_language\_of\_culture | Is the character's court language the language of the target culture? | ```<br>has_court_language_of_culture = scope:target_culture<br>``` |  | character | culture |
| has\_court\_position | is the scoped character holding the target court position type? |  |  | character |  |
| has\_court\_type | has\_court\_type = court\_diplomatic | ```<br>Does the character have this court type?<br>``` |  | character |  |
| has\_cultural\_parameter | Does the culture have this cultural parameter? | ```<br><culture> = { has_cultural_parameter = name }<br>``` |  | culture |  |
| has\_cultural\_pillar | Does the culture have this cultural pillar? | ```<br><culture> = { has_cultural_pillar = name }<br>``` |  | culture |  |
| has\_cultural\_tradition | Does the culture have this cultural tradition? | ```<br><culture> = { has_cultural_tradition = name }<br>``` |  | culture |  |
| has\_dlc\_feature | Does the host have DLC that enables this particular feature |  |  | none | Valid Features: garments\_of\_the\_hre, fashion\_of\_the\_abbasid\_court, the\_northern\_lords, hybridize\_culture, diverge\_culture, royal\_court, reform\_culture, court\_artifacts, the\_fate\_of\_iberia, and friends\_and\_foes |
| has\_employed\_any\_court\_position | does the scoped character have any employed court positions? |  |  | character | yes/no |
| has\_holding | does the scope province have holding? | ```<br>	has_holding = yes<br>``` |  | province | yes/no |
| has\_house\_artifact\_claim | Does the scoped dynasty house have a personal claim on the target artifact |  |  | dynasty house | artifact |
| has\_innovation\_flag | Has the culture discovered an innovation with this flag? has\_innovation\_flag = flag |  |  | culture |  |
| has\_inspiration\_type | has\_inspiration\_type = type | ```<br>Checks if the scoped inspiration has the given inspiration database type<br>``` |  | inspiration |  |
| has\_local\_player\_open\_court\_event | Has the local player opened a court event in the royal court view? | ```<br>An interface trigger, can only be used in specific places<br>``` |  | none | yes/no |
| has\_local\_player\_seen\_unopened\_court\_event | Has the local player seen the unopened court event(s) waiting in the royal court view? | ```<br>An interface trigger, can only be used in specific places<br>``` |  | none | yes/no |
| has\_local\_player\_unopened\_court\_event | Has the local player an unopened court event waiting in the royal court view? | ```<br>An interface trigger, can only be used in specific places<br>``` |  | none | yes/no |
| has\_memory\_category | Does the character memory have this memory category? | ```<br>has_memory_category = happy<br>``` |  | character memory |  |
| has\_memory\_participant | Does the character memory have this target character as a participant? | ```<br>has_memory_participant = character<br>``` |  | character memory | character |
| has\_memory\_type | Does the character memory have this memory type? | ```<br>has_memory_type = battle<br>``` |  | character memory |  |
| has\_name\_list | Does the culture have this name list? | ```<br><culture> = { has_name_list = name }<br>``` |  | culture |  |
| has\_outstanding\_artifact\_claims | does the scoped character have any artifact claims that can be pressed? ( EXPENSIVE ) |  |  | character | yes/no |
| has\_pending\_court\_events | Does the character have pending court events? Meaning court events that'll spawn when they next open the royal court view. Can only be used on player characters with a royal court. | ```<br>has_pending_court_events = bool<br>``` |  | character | yes/no |
| has\_personal\_artifact\_claim | Does the scoped character have a personal claim on the target artifact |  |  | character | artifact |
| has\_primary\_name\_list | Does the culture have this name list as its first name list? | ```<br><culture> = { has_primary_name_list = name }<br>``` |  | culture |  |
| has\_prisoners | Does the character have prisoners? |  |  | character | yes/no |
| has\_relation\_antiquarian | Checks for a scripted relationship with a target character |  |  | character | character target |
| has\_relation\_to | does the character have a relation to the target? Matches the logic of the data system function HasRelationTo, has\_relation\_to = <character> |  |  | character | character |
| has\_royal\_court | has\_royal\_court = bool | ```<br>Does the scoped character have a royal court<br>``` |  | character | yes/no |
| has\_same\_court\_language | Is the character's court language the same language as the target character's? | ```<br>has_same_court_language = scope:target_character<br>``` |  | character | character |
| has\_same\_court\_type\_as | has\_same\_court\_type\_as = character | ```<br>Does the character have the same court type as the target?<br>``` |  | character | character target |
| has\_same\_culture\_ethos | Does the culture have the same ethos as the target? |  |  | culture | culture |
| has\_same\_culture\_heritage | Does the culture have the same heritage as the target? |  |  | culture | culture |
| has\_same\_culture\_language | Does the culture have the same language as the target? |  |  | culture | culture |
| has\_same\_culture\_martial\_tradition | Does the culture have the same martial tradition as the target? |  |  | culture | culture |
| has\_same\_sinful\_trait | do the two characters share a trait that is considered sinful by both of their respective faiths? | ```<br>scope:character_1 = { has_same_sinful_trait = scope:character_2 }<br>``` |  | character | character target |
| has\_same\_virtue\_trait | do the two characters share a trait that is considered virtuous by both of their respective faiths? | ```<br>scope:character_1 = { has_same_virtue_trait = scope:character_2 }<br>``` |  | character | character target |
| has\_secret\_relation\_antiquarian | Checks for a secret scripted relationship with a target character |  |  | character | character target |
| has\_spawned\_court\_events | has\_spawned\_court\_events = bool | ```<br>Does the character have spawned court events? Meaning court events are shown (opened or not) in the royal court view.<br>Can only be used on player characters with a royal court.<br>``` |  | character | yes/no |
| has\_struggle\_phase\_parameter | Does the given struggle's current phase have the given parameter? Can only check for bool parameters. has\_struggle\_phase\_parameter = parameter\_key |  |  | struggle |  |
| has\_unit\_gfx | Does the culture have this unit gfx? | ```<br><culture> = { has_unit_gfx = mena_unit_gfx }<br>``` |  | culture |  |
| has\_user\_set\_coa | Has the user set a specific coat of arms for this title? |  |  | landed title | yes/no |
| inspiration\_gold\_invested | Gets the amount of gold invested in the scoped inspiration | ```<br>inspiration_gold_invested > 5<br>``` |  | inspiration | <, <=, =, !=, >, >= |
| inspiration\_progress | Gets the progress of the scoped inspiration | ```<br>inspiration_progress > 5<br>``` |  | inspiration | <, <=, =, !=, >, >= |
| intrigue\_lifestyle\_unlockable\_perks | How many perks from this lifestyle can the character currently unlock? This checks that they have the parent perks, and that the can\_be\_picked is met. It doesn't check perk points |  |  | character | <, <=, =, !=, >, >= |
| is\_council\_task\_valid | Check if the task of the scope councillor is valid { task\_type = council\_position\_type\_key target = for\_targeted\_tasks } |  |  | character |  |
| is\_court\_position\_employer | is the scoped character employed in the target position by target character |  |  | character |  |
| is\_culture\_involved\_in\_struggle | is the culture involved in struggle? | ```<br>	is_culture_involved_in_struggle = culture:english<br>``` |  | struggle | culture |
| is\_decision\_on\_cooldown | Is the given decision on cooldown for the current character. If decision on cooldown return True. | ```<br>is_decision_on_cooldown = decision_key<br>``` |  | character | yes/no |
| is\_divergent\_culture | Checks if the scope culture was created by diverging from a single parent culture and returns yes if true or no if false. | ```<br>is_divergent_culture = yes<br>``` |  | culture | yes/no |
| is\_equipped | is the scoped artifact currently equipped in its owners inventory? |  |  | artifact | yes/no |
| is\_faith\_involved\_in\_struggle | is the faith involved in struggle? | ```<br>	is_faith_involved_in_struggle  = faith:baltic_pagan<br>``` |  | struggle | faith |
| is\_from\_ruler\_designer | Was this character made from the ruler designer |  |  | character | yes/no |
| is\_head\_of\_faith | Is this title a head of faith title |  |  | landed title | yes/no |
| is\_hybrid\_culture | Checks if the scope culture was created from a hybridization of two cultures and returns yes if true or no if false. | ```<br>is_hybrid_culture = yes<br>``` |  | culture | yes/no |
| is\_landless\_ruler | Is the scope character a landless ruler (holds any title, but no on-map land)? |  |  | character | yes/no |
| is\_pregnant | is the scoped character pregnant ? |  |  | character | yes/no |
| is\_raided | Is this province currently being raided? |  |  | province | yes/no |
| is\_riverside\_county | is the county riverside? |  |  | landed title | yes/no |
| is\_riverside\_province | is the province riverside? |  |  | province | yes/no |
| is\_sea\_province | Is this a sea province? |  |  | province | yes/no |
| is\_struggle\_phase | is the scope struggle's current phase particular phase? | ```<br>	is_struggle_phase = struggle_iberia_phase_opportunity<br>``` |  | struggle |  |
| is\_struggle\_type | is the scope struggle's type particular type? | ```<br>	is_struggle_type = iberian_struggle<br>``` |  | struggle |  |
| is\_unique | Is the scoped artifact unique | ```<br>defined in the scripted template of the artifact<br>``` |  | artifact | yes/no |
| is\_valid\_for\_event\_debug | is the scoped character valid for the given event, without checking event cooldown? | ```<br>NOTE: this is only for debug purposes and will not work in release mode!<br>is_valid_for_event_debug = event_key<br>``` |  | character |  |
| is\_valid\_for\_event\_debug\_cooldown | is the scoped character valid for the given event, including a cooldown check? | ```<br>NOTE: this is only for debug purposes and will not work in release mode!<br>is_valid_for_event_debug_cooldown = event_key<br>``` |  | character |  |
| knows\_court\_language\_of | Does the character know the court language of the target character? | ```<br>knows_court_language_of = scope:target_character<br>``` |  | character | character |
| knows\_language | Does the character know the language? | ```<br>knows_language = language_norwegian<br>``` |  | character |  |
| knows\_language\_of\_culture | Does the character know the language of the target culture? | ```<br>knows_language_of_culture = scope:target_culture<br>``` |  | character | culture |
| learning\_lifestyle\_unlockable\_perks | How many perks from this lifestyle can the character currently unlock? This checks that they have the parent perks, and that the can\_be\_picked is met. It doesn't check perk points |  |  | character | <, <=, =, !=, >, >= |
| long\_term\_gold\_maximum | How big is the 'long term' budget is supposed to get? |  |  | character | <, <=, =, !=, >, >= |
| martial\_lifestyle\_unlockable\_perks | How many perks from this lifestyle can the character currently unlock? This checks that they have the parent perks, and that the can\_be\_picked is met. It doesn't check perk points |  |  | character | <, <=, =, !=, >, >= |
| monthly\_character\_income\_long\_term | did the character allocate the required gold? (AI category long term) |  |  | character | <, <=, =, !=, >, >= |
| monthly\_character\_income\_reserved | did the character allocate the required gold? (AI category reserved) |  |  | character | <, <=, =, !=, >, >= |
| monthly\_character\_income\_short\_term | did the character allocate the required gold? (AI category short term) |  |  | character | <, <=, =, !=, >, >= |
| monthly\_character\_income\_war\_chest | did the character allocate the required gold? (AI category war chest) |  |  | character | <, <=, =, !=, >, >= |
| months\_as\_ruler | Number of months this character has been a ruler, returns -1 if character isn't a ruler |  |  | character | <, <=, =, !=, >, >= |
| months\_until\_max\_discontent | How many months until Discontent is max (100)? |  |  | faction | <, <=, =, !=, >, >= |
| morph\_gene\_attribute | Compare entity attribute from specific gene | ```<br>scope:character = {<br>	morph_gene_attribute = {<br>		category = gene_height<br>		attribute = body_height<br>		value < 0.05<br>	}<br>}<br>An interface trigger, can only be used in specific places<br>``` |  | character | <, <=, =, !=, >, >= |
| morph\_gene\_value | Compare value of specific gene. Does NOT take into account trait modifiers | ```<br>scope:character = {<br>		morph_gene_attribute = {<br>			category = gene_height<br>			value < 0.05<br>		}<br>	}<br>An interface trigger, can only be used in specific places<br>``` |  | character | <, <=, =, !=, >, >= |
| num\_artifact\_kills | How many kills has this artifact been used in? |  |  | artifact | <, <=, =, !=, >, >= |
| num\_enemies\_killed | Number of troops killed on the opposite side. | ```<br>num_enemies_killed >= 500<br>``` |  | combat side | <, <=, =, !=, >, >= |
| num\_of\_known\_languages | How many languages does the character know? | ```<br>num_of_known_languages > 1<br>``` |  | character | <, <=, =, !=, >, >= |
| num\_of\_relation\_antiquarian | Compares the number of scripted relations a character has of the type |  |  | character | <, <=, =, !=, >, >= |
| num\_total\_troops | Number of total troops on boths sides. | ```<br>num_total_troops >= 2000<br>``` |  | combat | <, <=, =, !=, >, >= |
| number\_of\_sinful\_traits\_in\_common | do the two characters share a number of traits that is considered sinful by both of their respective faiths? | ```<br>number_of_sinful_traits_in_common = { target = X value >/</>=/<= Y }<br>``` |  | character | <, <=, =, !=, >, >= |
| number\_of\_virtue\_traits\_in\_common | do the two characters share a number of traits that is considered virtuous by both of their respective faiths? | ```<br>number_of_virtue_traits_in_common = { target = X value >/</>=/<= Y }<br>``` |  | character | <, <=, =, !=, >, >= |
| percent\_enemies\_killed | Percantage of enemies killed out of total number of enemy soldiers. | ```<br>percent_enemies_killed >= 80<br>``` |  | combat side | <, <=, =, !=, >, >= |
| perks\_in\_diplomacy\_lifestyle | How many perks does this lifestyle have? |  |  | none | <, <=, =, !=, >, >= |
| perks\_in\_intrigue\_lifestyle | How many perks does this lifestyle have? |  |  | none | <, <=, =, !=, >, >= |
| perks\_in\_learning\_lifestyle | How many perks does this lifestyle have? |  |  | none | <, <=, =, !=, >, >= |
| perks\_in\_martial\_lifestyle | How many perks does this lifestyle have? |  |  | none | <, <=, =, !=, >, >= |
| perks\_in\_stewardship\_lifestyle | How many perks does this lifestyle have? |  |  | none | <, <=, =, !=, >, >= |
| phase\_has\_catalyst | Is any of the future phases affected by the given catalyst?phase\_has\_catalyst = catalyst\_key |  |  | struggle |  |
| rarity | is the scoped artifact of given rarity? |  |  | artifact |  |
| reserved\_gold | does the character have the required gold? (AI category 'reserved') |  |  | character | <, <=, =, !=, >, >= |
| reserved\_gold\_maximum | How big is the 'reserved' budget is supposed to get? |  |  | character | <, <=, =, !=, >, >= |
| save\_temporary\_opinion\_value\_as | Saves the scoped character's opinion of the target character as an arbitrarily-named target to be referenced later in the in the same trigger | ```<br>save_temporary_opinion_value_as = { name = <string> target = x <br>``` |  | none |  |
| scriptedtests\_gold\_income\_no\_theocracy | does the character have the specified tax income, excluding income from the theocratic lessee? |  |  | character | <, <=, =, !=, >, >= |
| short\_term\_gold\_maximum | How big is the 'short term' budget is supposed to get?(It may exceed this if all other budgets are full) |  |  | character | <, <=, =, !=, >, >= |
| should\_decay | should the scoped artifact decay with time? |  |  | artifact | yes/no |
| should\_show\_nudity | can nudity be shown? | ```<br>An interface trigger, can only be used in specific places<br>``` |  | none | yes/no |
| stewardship\_lifestyle\_unlockable\_perks | How many perks from this lifestyle can the character currently unlock? This checks that they have the parent perks, and that the can\_be\_picked is met. It doesn't check perk points |  |  | character | <, <=, =, !=, >, >= |
| time\_since\_death | for how long has the character is dead? time\_since\_death = { days/months/years =,>,< X } |  |  | character |  |
| time\_to\_hook\_expiry | The # of days until the scoped character's hook on the target expires | ```<br>time_to_hook_expiry = { target = someone value > 50 }<br>``` |  | character | <, <=, =, !=, >, >= |
| title\_held\_years | Returns the number of years a title is held if valid (otherwise returns 0) |  |  | landed title | <, <=, =, !=, >, >= |
| total\_army\_damage | What is the army's total damage stat in its current location? |  |  | army | <, <=, =, !=, >, >= |
| total\_army\_pursuit | What is the army's total pursuit stat in its current location? |  |  | army | <, <=, =, !=, >, >= |
| total\_army\_screen | What is the army's total screen stat in its current location? |  |  | army | <, <=, =, !=, >, >= |
| total\_army\_siege\_value | What is the army's total siege value stat in its current location? |  |  | army | <, <=, =, !=, >, >= |
| total\_army\_toughness | What is the army's total toughness stat in its current location? |  |  | army | <, <=, =, !=, >, >= |
| troops\_ratio | Side's troops/opposide side's troops.ntroops\_ratio < 0.5 |  |  | combat side | <, <=, =, !=, >, >= |
| war\_chest\_gold | does the character have the required gold? (AI category 'war chest') |  |  | character | <, <=, =, !=, >, >= |
| war\_chest\_gold\_maximum | How big is the 'war chest' budget is supposed to get? |  |  | character | <, <=, =, !=, >, >= |
| warscore\_value | Warscore value. | ```<br>warscore_value >= 25<br>``` |  | combat | <, <=, =, !=, >, >= |
| years\_as\_ruler | Number of years this character has been a ruler, returns -1 if character isn't a ruler |  |  | character | <, <=, =, !=, >, >= |
| any\_dynasty\_member | Iterate through all dynasty members | any\_dynasty\_member = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | dynasty | character |
| blood\_legacy\_track\_perks | How many legacies in the Blood legacy track does this dynasty have? |  | <, <=, =, !=, >, >= | dynasty |  |
| dynasty\_can\_unlock\_relevant\_perk | Can the scoped dynasty unlock a 'relevant' legacy? Relevant meaning one that isn't the first in its track unless the dynasty has no partially filled tracks |  | yes/no | dynasty |  |
| dynasty\_prestige | Does the dynasty have the required prestige? |  | <, <=, =, !=, >, >= | dynasty |  |
| dynasty\_prestige\_level | Does the dynasty have the required level of splendor? |  | <, <=, =, !=, >, >= | dynasty |  |
| erudition\_legacy\_track\_perks | How many legacies in the Erudition legacy track does this dynasty have? |  | <, <=, =, !=, >, >= | dynasty |  |
| glory\_legacy\_track\_perks | How many legacies in the Glory legacy track does this dynasty have? |  | <, <=, =, !=, >, >= | dynasty |  |
| guile\_legacy\_track\_perks | How many legacies in the Guile legacy track does this dynasty have? |  | <, <=, =, !=, >, >= | dynasty |  |
| has\_dynasty\_modifier | Does the scoped dynasty have a given modifier? | has\_dynasty\_modifier = name |  | dynasty |  |
| has\_dynasty\_modifier\_duration\_remaining | Does the scoped dynasty have the duration remaining on a given modifier? | has\_dynasty\_modifier\_duration\_remaining = name |  | dynasty |  |
| has\_dynasty\_perk | Does the dynasty have this legacy? | has\_dynasty\_perk = key |  | dynasty |  |
| kin\_legacy\_track\_perks | How many legacies in the Kin legacy track does this dynasty have? |  | <, <=, =, !=, >, >= | dynasty |  |
| law\_legacy\_track\_perks | How many legacies in the Law legacy track does this dynasty have? |  | <, <=, =, !=, >, >= | dynasty |  |
| warfare\_legacy\_track\_perks | How many legacies in the Warfare legacy track does this dynasty have? |  | <, <=, =, !=, >, >= | dynasty |  |
| compare\_value | Compare the scoped value instead of scoping into it. | var:variable\_name = { compare\_value < 4 }<br>var:variable\_name.compare\_value < {value = var:other\_variable add = 5} | <, <=, =, !=, >, >= | value |  |
| any\_house\_member | Iterate through all house members | any\_house\_member = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | dynasty house | character |
| has\_house\_modifier | Does the scoped house have a given modifier? | has\_house\_modifier = name |  | dynasty house |  |
| has\_house\_modifier\_duration\_remaining | Does the scoped house have the duration remaining on a given modifier? | has\_house\_modifier\_duration\_remaining = name |  | dynasty house |  |
| any\_faith | Iterate through all faiths within a religion | any\_faith = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | religion | faith |
| is\_in\_family | Is the scoped faith in a given religious family? | is\_in\_family = rf\_abrahamic |  | religion |  |
| any\_scheme\_agent | Iterate through all agents in the scheme | any\_scheme\_agent = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | scheme | character |
| has\_scheme\_modifier | Is the scheme currently affected by the specified modifier? | has\_scheme\_modifier = X |  | scheme |  |
| is\_hostile | Is the scoped scheme a hostile scheme? | is\_hostile = bool | yes/no | scheme |  |
| is\_scheme\_agent\_exposed | Is the target character an exposed agent in the scope scheme? |  | character target | scheme |  |
| is\_scheme\_exposed | Is the scheme exposed? |  | yes/no | scheme |  |
| scheme\_duration\_days | The number of days since the scheme was started |  | <, <=, =, !=, >, >= | scheme |  |
| scheme\_is\_character\_agent | Is the target character part of this scheme? |  | character target | scheme |  |
| scheme\_monthly\_progress | Monthly scheme progress in % (i.e. 50 equals 50%) |  | <, <=, =, !=, >, >= | scheme |  |
| scheme\_number\_of\_agents | The number of agents in a scheme |  | <, <=, =, !=, >, >= | scheme |  |
| scheme\_number\_of\_exposed\_agents | The number of exposed agents in a scheme |  | <, <=, =, !=, >, >= | scheme |  |
| scheme\_power | Scheme power |  | <, <=, =, !=, >, >= | scheme |  |
| scheme\_power\_resistance\_difference | Scheme power minus scheme resistance |  | <, <=, =, !=, >, >= | scheme |  |
| scheme\_power\_resistance\_ratio | Scheme power/resistance ratio. Set to ±10000 if resistance is zero and power is positive/negative (0 if both power and resistance are 0) |  | <, <=, =, !=, >, >= | scheme |  |
| scheme\_progress | Scheme progress (0 - 10 (defined)) |  | <, <=, =, !=, >, >= | scheme |  |
| scheme\_resistance | Scheme resistance |  | <, <=, =, !=, >, >= | scheme |  |
| scheme\_secrecy | Scheme secrecy |  | <, <=, =, !=, >, >= | scheme |  |
| scheme\_skill | Is the scheme currently affected by the specified modifier? | has\_scheme\_modifier = X |  | scheme |  |
| scheme\_success\_chance | Scheme success chance |  | <, <=, =, !=, >, >= | scheme |  |
| scheme\_type | Is the scheme of the specified type? | scheme\_type = X |  | scheme |  |
| active\_de\_jure\_drift\_progress |  | task\_current\_value = scope:county.active\_de\_jure\_drift\_progress | <, <=, =, !=, >, >= | landed title |  |
| any\_claimant | Iterate through all claimants to title. parameters: explicit = yes/no/all - default yes | any\_claimant = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | landed title | character |
| any\_connected\_county | Iterate through all counties connected to this one. Is based on top liege | any/every/whatever\_connected\_county = {<br>max\_naval\_distance = 500<br>allow\_one\_county\_land\_gap = yes<br>any\_connected\_county = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | landed title | landed title |
| any\_county\_province | Iterate through all baronies in a county | any\_county\_province = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | landed title | province |
| any\_de\_jure\_county\_holder | Iterate through all characters directly holding counties within this de jure title | any\_de\_jure\_county\_holder = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | landed title | character |
| any\_de\_jure\_top\_liege | Iterate through all top lieges of the counts within this de jure title | any\_de\_jure\_top\_liege = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | landed title | character |
| any\_dejure\_vassal\_title\_holder | Iterate through all the vassal holders of the title | any\_dejure\_vassal\_title\_holder = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | landed title | character |
| any\_election\_candidate | Iterate through all characters who are valid candidates in an election for a title | any\_election\_candidate = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | landed title | character |
| any\_elector | Iterate through all characters who are valid electors in an election for a title | any\_elector = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | landed title | character |
| any\_in\_de\_facto\_hierarchy | Iterate through the title itself, all de facto vassals, and below. The continue trigger specifies whether to recursively iterate through the vassal's vassals | continue is unrelated to the limit; if the limit is met it is added to the list, but its vassals will get checked even if the limit isn't met as long as the 'continue' trigger is<br>...\_de\_jure\_vassal\_and\_below = { continue = { conditions } }<br>any\_in\_de\_facto\_hierarchy = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | landed title | landed title |
| any\_in\_de\_jure\_hierarchy | Iterate through the title itself, all de jure vassals, and below. The continue trigger specifies whether to recursively iterate through the vassal's vassal | This is unrelated to the limit; if the limit is met it is added to the list, but its vassals will get checked even if the limit isn't met as long as the 'continue' trigger is<br>...\_de\_jure\_vassal\_and\_below = { continue = { conditions } }<br>any\_in\_de\_jure\_hierarchy = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | landed title | landed title |
| any\_neighboring\_county | Iterate through all neighboring counties. Can only be used in county scope | any\_neighboring\_county = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | landed title | landed title |
| any\_this\_title\_or\_de\_jure\_above | Iterate through this title and all its de jure liege titles | any\_this\_title\_or\_de\_jure\_above = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | landed title | landed title |
| any\_title\_heir | Line of succession for the scoped title | any\_title\_heir = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | landed title | character |
| any\_title\_joined\_faction | Iterate through all factions joined the scope landed title | any\_title\_joined\_faction = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | landed title | faction |
| any\_title\_to\_title\_neighboring\_and\_across\_water\_county | Scopes from a title to a neighboring county (incl. across water, looking through the de jure lieges) | any\_title\_to\_title\_neighboring\_and\_across\_water\_county = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | landed title | landed title |
| any\_title\_to\_title\_neighboring\_and\_across\_water\_duchy | Scopes from a title to a neighboring duchy (incl. across water, looking through the de jure lieges) | any\_title\_to\_title\_neighboring\_and\_across\_water\_duchy = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | landed title | landed title |
| any\_title\_to\_title\_neighboring\_and\_across\_water\_empire | Scopes from a title to a neighboring empire (incl. across water, looking through the de jure lieges) | any\_title\_to\_title\_neighboring\_and\_across\_water\_empire = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | landed title | landed title |
| any\_title\_to\_title\_neighboring\_and\_across\_water\_kingdom | Scopes from a title to a neighboring kingdom (incl. across water, looking through the de jure lieges) | any\_title\_to\_title\_neighboring\_and\_across\_water\_kingdom = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | landed title | landed title |
| any\_title\_to\_title\_neighboring\_county | Scopes from a title to a neighboring county (looking through the de jure lieges) | any\_title\_to\_title\_neighboring\_county = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | landed title | landed title |
| any\_title\_to\_title\_neighboring\_duchy | Scopes from a title to a neighboring duchy (looking through the de jure lieges) | any\_title\_to\_title\_neighboring\_duchy = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | landed title | landed title |
| any\_title\_to\_title\_neighboring\_empire | Scopes from a title to a neighboring empire (looking through the de jure lieges) | any\_title\_to\_title\_neighboring\_empire = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | landed title | landed title |
| any\_title\_to\_title\_neighboring\_kingdom | Scopes from a title to a neighboring kingdom (looking through the de jure lieges) | any\_title\_to\_title\_neighboring\_kingdom = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | landed title | landed title |
| can\_be\_leased\_out | Can the scoped title be leased out? |  | yes/no | landed title |  |
| can\_title\_create\_faction | Can the title create the faction of the specified type against the specified character? | can\_title\_create\_faction = { type = X target = Y } |  | landed title |  |
| can\_title\_join\_faction | Can the the scoped title join the faction? | can\_title\_join\_faction = faction |  | landed title |  |
| county\_control | Does the county title have the required county control? |  | <, <=, =, !=, >, >= | landed title |  |
| county\_control\_rate | How much county control is the county gaining each month? |  | <, <=, =, !=, >, >= | landed title |  |
| county\_control\_rate\_modifier | What's the multiplier to the control gain rate? E.g., if there's just a +20% modifier, this would return 1.2 |  | <, <=, =, !=, >, >= | landed title |  |
| county\_holder\_opinion | Compares the county's opinion of its holder |  | <, <=, =, !=, >, >= | landed title |  |
| county\_opinion | Compares the county's opinion of the current count |  | <, <=, =, !=, >, >= | landed title |  |
| county\_opinion\_target | Compares the county's opinion of the target character to the specified value | county\_opinion\_target = { target = X value >/</= Y } |  | landed title |  |
| de\_jure\_drift\_progress | Compare drift progress towards target with value | <drifting\_title> = { de\_jure\_drift\_progress = { target = <drift\_target\_title> value > 50 } } |  | landed title |  |
| de\_jure\_drifting\_towards | Is the scoped landed title de jure drifting toward another title? | <drifting\_title> = { de\_jure\_drifting\_towards = <drift\_target\_title> } | landed title scope | landed title | landed title |
| development\_level | Does the county title have the required county development level? |  | <, <=, =, !=, >, >= | landed title |  |
| development\_rate | How much development progress is the county gaining each month? |  | <, <=, =, !=, >, >= | landed title |  |
| development\_rate\_modifier | What's the multiplier to the development progress? |  | <, <=, =, !=, >, >= | landed title |  |
| development\_towards\_level\_increase | Does the county title have the required progress towards the next level of development? E.g., if level 1 is 100, level 2 is 300 (these are set in defines), and current total is 150, this would return 50 |  | <, <=, =, !=, >, >= | landed title |  |
| has\_character\_nominiated | Has the target character nominated a successor for the scoped title? |  | character target | landed title |  |
| has\_county\_modifier | Does the scoped county have a given modifier? | has\_county\_modifier = name |  | landed title |  |
| has\_county\_modifier\_duration\_remaining | Does the scoped county have the duration remaining on a given modifier? | has\_county\_modifier\_duration\_remaining = name |  | landed title |  |
| has\_disabled\_building | Is the scoped landed title connected to a holding that contains at least one disabled building? |  | yes/no | landed title |  |
| has\_holy\_site\_flag | Does the barony have a holy site with the given flag? | has\_holy\_site\_flag = some\_flag |  | landed title |  |
| has\_order\_of\_succession | Does the scoped title have a given succession type? | has\_order\_of\_succession = election |  | landed title |  |
| has\_revokable\_lease | Is the title under a lease that can be revoked manually? |  | yes/no | landed title |  |
| has\_title\_law | Does the scoped title have the given title-specific law? |  |  | landed title |  |
| has\_title\_law\_flag | Does the scoped title have a title-specific law with the given flag? |  |  | landed title |  |
| has\_wrong\_holding\_type | Is the scope landed title connected to a holding that cannot be governed by the current lessee or holder? |  | yes/no | landed title |  |
| is\_capital\_barony | Is title in the scope a capital barony? |  | yes/no | landed title |  |
| is\_coastal\_county | Is the county coastal? |  | yes/no | landed title |  |
| is\_connected\_to | Is the county connected to the other county? Is based on top liege | is\_connected\_to = {<br>max\_naval\_distance = 500<br>allow\_one\_county\_land\_gap = yes<br>target = some other county<br>} |  | landed title |  |
| is\_contested | Is the scope landed title contested in any war? |  | yes/no | landed title |  |
| is\_de\_facto\_liege\_or\_above\_target | Is the title de facto liege or above the target title? |  | landed title target | landed title |  |
| is\_de\_jure\_liege\_or\_above\_target | Is the title de jure liege or above the target title? |  | landed title target | landed title |  |
| is\_holy\_order | Is the scope landed title a holy order? |  | yes/no | landed title |  |
| is\_holy\_site | Is the barony a holy site of any faith? | is\_holy\_site = yes | yes/no | landed title |  |
| is\_holy\_site\_controlled\_by | Does the target character control a holy site of the scoped object? | is\_holy\_site\_controlled\_by = root | character scope | landed title | character |
| is\_holy\_site\_of | Is the barony a holy site of the given faith? | is\_holy\_site\_of = catholic |  | landed title |  |
| is\_landless\_type\_title | Is this title considered a landless type title? |  | yes/no | landed title |  |
| is\_leased\_out | Is the scoped title leased out? |  | yes/no | landed title |  |
| is\_mercenary\_company | Is the scope landed title a mercenary company? |  | yes/no | landed title |  |
| is\_neighbor\_to\_realm | Is this landed title adjacent to the character's realm? | is\_neighbor\_to\_realm = character | character scope | landed title | character |
| is\_target\_of\_council\_task | Is the county currently affected by the specified council task? Needs to be in a county title scope |  |  | landed title |  |
| is\_title\_created | Is title in the scope created? |  | yes/no | landed title |  |
| is\_titular | Is this title titular (has no de jure counties in it, and is not a barony/county)? |  | yes/no | landed title |  |
| is\_under\_holy\_order\_lease | Is the scoped title leased out to any holy order? |  | yes/no | landed title |  |
| place\_in\_line\_of\_succession | What place in line of succession does the character hold? |  |  | landed title |  |
| recent\_history | Does the scope title have a history entry of the specified type in recent history? | recent\_history = { type = X days/months/years = Y }<br>The type can be omitted, all history types are considered then<br>Possible types:<br>- conquest<br>- conquest\_holy\_war<br>- conquest\_claim<br>- conquest\_populist<br>- election<br>- inheritance<br>- abdication<br>- created<br>- destroyed<br>- usurped<br>- granted<br>- revoked<br>- independency<br>- leased\_out<br>- lease\_revoked<br>- returned<br>- faction\_demand |  | landed title |  |
| target\_is\_de\_facto\_liege\_or\_above | Is the target title de facto liege or above? |  | landed title target | landed title |  |
| target\_is\_de\_jure\_liege\_or\_above | Is the target title de jure liege or above? |  | landed title target | landed title |  |
| tier | What tier is the scoped title? Use the script values please, not raw numbers | The tiers are<br>1. tier\_barony<br>2. tier\_county<br>3. tier\_duchy<br>4. tier\_kingdom<br>5. tier\_empire | <, <=, =, !=, >, >= | landed title |  |
| title\_create\_faction\_type\_chance | Check if the chance to create a faction against a target of the scope landed title is is true against the scripted value | title\_create\_faction\_type\_chance = {<br>```<br>   type = faction_type #An ongoing faction<br>   target = target_character<br>   value <|<=|>=|> 0<br>```<br>} |  | landed title |  |
| title\_is\_a\_faction\_member | Is the scope title a member of a faction? |  | yes/no | landed title |  |
| title\_join\_faction\_chance | Check if the chance of the scope landed title to join the faction against the scripted value | title\_join\_faction\_chance = {<br>```<br>   faction = faction_target #An ongoing faction<br>   value <|<=|>=|> 0<br>```<br>} |  | landed title |  |
| title\_will\_leave\_sub\_realm\_on\_succession | Will the title leave the sub-realm of the character on the right-hand-side upon succession? That is, is the first heir in someone outside the sub-realm, and the highest tier title they'll inherit from the person holding the title is not higher than their current tier |  | character target | landed title |  |
| story\_type | Is the story in scope of this type? |  |  | story cycle |  |
| can\_get\_innovation\_from | Get random applicable innovation from another culture |  |  | culture |  |
| has\_all\_innovations | Has the culture discovered all innovations matching the filter? | has\_all\_innovations = {<br>with\_flag = flag\_name # innovation matches if it has the flag; optional<br>without\_flag = flag\_name # innovation matches if it does not have the flag; optional<br>culture\_era = era\_key # innovation matches if it is from the era; optional<br>} |  | culture |  |
| has\_cultural\_era\_or\_later | Has this culture achieved specified era? | <culture> = { has\_cultural\_era\_or\_later = culture\_era\_early\_medieval } |  | culture |  |
| has\_innovation | Have the culture discovered this innovation? |  |  | culture |  |
| mercenary\_company\_expiration\_days | How many days are left in the mercenary contract. 0 if not hired. |  | <, <=, =, !=, >, >= | mercenary company |  |
| age | Compare character age |  | <, <=, =, !=, >, >= | character |  |
| ai\_boldness | AI boldness |  | <, <=, =, !=, >, >= | character |  |
| ai\_compassion | AI compassion |  | <, <=, =, !=, >, >= | character |  |
| ai\_diplomacy\_stance | The AI's diplomatic view of the target character | ai\_diplomacy\_stance = {<br>```<br>   target = target_character<br>   stance = neutral/threat/enemy/friend<br>```<br>} |  | character |  |
| ai\_energy | AI energy |  | <, <=, =, !=, >, >= | character |  |
| ai\_greed | AI greed |  | <, <=, =, !=, >, >= | character |  |
| ai\_honor | AI honor |  | <, <=, =, !=, >, >= | character |  |
| ai\_rationality | AI rationality |  | <, <=, =, !=, >, >= | character |  |
| ai\_sociability | AI sociability |  | <, <=, =, !=, >, >= | character |  |
| ai\_values\_divergence | Compare AI values between characters | target = other character value >/</= sum of differences in ai values |  | character |  |
| ai\_vengefulness | AI vengefulness |  | <, <=, =, !=, >, >= | character |  |
| ai\_zeal | AI zeal |  | <, <=, =, !=, >, >= | character |  |
| allowed\_concubines | Can the scope owner have concubines? |  | yes/no | character |  |
| allowed\_more\_concubines | Can the scope owner have more concubines? |  | yes/no | character |  |
| allowed\_more\_spouses | Can the scope owner have more spouses? |  | yes/no | character |  |
| any\_alert\_creatable\_title | Iterate through all titles that can be created by the character. (only for alerts) | any\_alert\_creatable\_title = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | landed title |
| any\_alert\_usurpable\_title | Iterate through all titles that can be usurped by the character. (only for alerts) | any\_alert\_usurpable\_title = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | landed title |
| any\_ally | Iterate through all allies | any\_ally = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | character |
| any\_ancestor | Iterate through all the ancestors of the scope character up to 5 generations | any\_ancestor = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | character |
| any\_army | Iterate through all armies | any\_army = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | army |
| any\_character\_to\_title\_neighboring\_and\_across\_water\_county | Scopes from a character to a neighboring county (incl. across water, looking through the de jure lieges) | any\_character\_to\_title\_neighboring\_and\_across\_water\_county = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | landed title |
| any\_character\_to\_title\_neighboring\_and\_across\_water\_duchy | Scopes from a character to a neighboring duchy (incl. across water, looking through the de jure lieges) | any\_character\_to\_title\_neighboring\_and\_across\_water\_duchy = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | landed title |
| any\_character\_to\_title\_neighboring\_and\_across\_water\_empire | Scopes from a character to a neighboring empire (incl. across water, looking through the de jure lieges) | any\_character\_to\_title\_neighboring\_and\_across\_water\_empire = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | landed title |
| any\_character\_to\_title\_neighboring\_and\_across\_water\_kingdom | Scopes from a character to a neighboring kingdom (incl. across water, looking through the de jure lieges) | any\_character\_to\_title\_neighboring\_and\_across\_water\_kingdom = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | landed title |
| any\_character\_to\_title\_neighboring\_county | Scopes from a character to a neighboring county (looking through the de jure lieges) | any\_character\_to\_title\_neighboring\_county = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | landed title |
| any\_character\_to\_title\_neighboring\_duchy | Scopes from a character to a neighboring duchy (looking through the de jure lieges) | any\_character\_to\_title\_neighboring\_duchy = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | landed title |
| any\_character\_to\_title\_neighboring\_empire | Scopes from a character to a neighboring empire (looking through the de jure lieges) | any\_character\_to\_title\_neighboring\_empire = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | landed title |
| any\_character\_to\_title\_neighboring\_kingdom | Scopes from a character to a neighboring kingdom (looking through the de jure lieges) | any\_character\_to\_title\_neighboring\_kingdom = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | landed title |
| any\_character\_war | Wars of the scoped character | any\_character\_war = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | war |
| any\_child | Iterate through all children | any\_child = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | character |
| any\_claim | Iterate through the titles of all claims held by a character; parameters: explicit = yes/no/all pressed = yes/no/all | any\_claim = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | landed title |
| any\_close\_family\_member | Iterate through all the close family \[father, mother, siblings, children, grandparents\] | any\_close\_family\_member = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | character |
| any\_close\_or\_extended\_family\_member | Iterate through all the close and extended relatives \[father, mother, siblings, children, grandparents, uncles/aunts, nephew/niece, cousins\] | any\_close\_or\_extended\_family\_member = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | character |
| any\_concubine | Iterate through all concubines | any\_concubine = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | character |
| any\_consort | Iterate through all consorts (concubines and spouses) | any\_consort = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | character |
| any\_councillor | Iterate through all councillors | any\_councillor = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | character |
| any\_courtier | Iterate through all courtiers. It stops iterating when finds very first suitable element therefore it does not check other elements. It might be annoying when you have another additional dependent triggers with that element previously found. | any\_courtier = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | character |
| any\_courtier\_away | Iterate through all courtiers that are away | any\_courtier\_away = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | character |
| any\_courtier\_or\_guest | Iterate through all courtiers and guests (pool and foreign court guests) It stops iterating when finds very first suitable element therefore it does not check other elements. It might be annoying when you have another additional dependent triggers with that element previously found. | any\_courtier\_or\_guest = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | character |
| any\_de\_jure\_claim | Iterate through all de jure claims for a character | any\_de\_jure\_claim = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | landed title |
| any\_diplomacy\_councillor | Iterate through all diplomacy-based councillors | any\_diplomacy\_councillor = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | character |
| any\_directly\_owned\_province | Iterate through all directly owned provinces | any\_directly\_owned\_province = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | province |
| any\_election\_title | Iterate through all titles the scoped character can vote on | any\_election\_title = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | landed title |
| any\_extended\_family\_member | Iterate through all the extended family \[uncles/aunts, nephew/niece, cousins\] | any\_extended\_family\_member = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | character |
| any\_foreign\_court\_guest | Iterate through all guests visiting from another court (in contrast to pool\_guest they have a liege) | any\_foreign\_court\_guest = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | character |
| any\_former\_concubine | Iterate through all former concubines. Not persisted past death | any\_former\_concubine = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | character |
| any\_former\_concubinist | Iterate through all former concubinists. Not persisted past death | any\_former\_concubinist = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | character |
| any\_former\_spouse | Iterate through all former spouses | any\_former\_spouse = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | character |
| any\_general\_councillor | Iterate through all councillors that are not related to a skill | any\_general\_councillor = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | character |
| any\_heir | Heirs of the scoped character | any\_heir = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | character |
| any\_heir\_title | Iterate through all landed titles character is heir to | any\_heir\_title = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | landed title |
| any\_heir\_to\_title | Iterate through all titles the scoped character is heir to | any\_heir\_to\_title = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | landed title |
| any\_held\_title | Iterate through all held landed titles | any\_held\_title = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | landed title |
| any\_hired\_mercenary | Iterate through all hired mercenary companies | any\_hired\_mercenary = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | mercenary company |
| any\_hooked\_character | Iterate through all characters this character has a hook on | any\_hooked\_character = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | character |
| any\_hostile\_raider | Iterate through anyone the character is hostile to due to their top liege's realm having been raided | any\_hostile\_raider = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | character |
| any\_intrigue\_councillor | Iterate through all intrigue-based councillors | any\_intrigue\_councillor = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | character |
| any\_knight | Iterate through all knights | any\_knight = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | character |
| any\_known\_secret | Iterate through all secrets known by the character | any\_known\_secret = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | secret |
| any\_learning\_councillor | Iterate through all learning-based councillors | any\_learning\_councillor = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | character |
| any\_liege\_or\_above | Iterate through all lieges above a character (skipping the character themselves) | any\_liege\_or\_above = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | character |
| any\_martial\_councillor | Iterate through all martial-based councillors | any\_martial\_councillor = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | character |
| any\_neighboring\_and\_across\_water\_realm\_same\_rank\_owner | A sub-realm or realm bordering the scope character's realm (including across water) that has the same rank as the scoped character (look for lieges of the owner of the land if necessary) | any\_neighboring\_and\_across\_water\_realm\_same\_rank\_owner = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | character |
| any\_neighboring\_and\_across\_water\_top\_liege\_realm | A realm with a different top liege neighboring the realm of the scoped character's top liege (including across water); switches to the realm's top title. Can be based on borders a day or two out of date | any\_neighboring\_and\_across\_water\_top\_liege\_realm = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | landed title |
| any\_neighboring\_and\_across\_water\_top\_liege\_realm\_owner | A realm with a different top liege neighboring the realm of the scope character's top liege (including across water); switches to the holder of the realm. Can be based on borders a day or two out of date | any\_neighboring\_and\_across\_water\_top\_liege\_realm\_owner = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | character |
| any\_neighboring\_realm\_same\_rank\_owner | A sub-realm or realm bordering the scope character's realm and has the same rank as the scope character (look for lieges of he owner of the land if necessary) | any\_neighboring\_realm\_same\_rank\_owner = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | character |
| any\_neighboring\_top\_liege\_realm | A realm with a different top liege neighboring the realm of the scope character's top liege; switches to the realm's top title. Can be based on borders a day or two out of date | any\_neighboring\_top\_liege\_realm = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | landed title |
| any\_neighboring\_top\_liege\_realm\_owner | A realm with a different top liege neighboring the realm of the scope character's top liege; switches to the holder of the realm. Can be based on borders a day or two out of date | any\_neighboring\_top\_liege\_realm\_owner = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | character |
| any\_owned\_story | Iterate through all owned stories for a character | any\_owned\_story = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | story cycle |
| any\_parent | Iterate through all (both) parents | any\_parent = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | character |
| any\_patroned\_holy\_order | Iterate through all holy orders that the scoped character is a patron of | any\_patroned\_holy\_order = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | holy order |
| any\_pinned\_character | Iterate through characters this player has pinned | any\_pinned\_character = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | character |
| any\_pinning\_character | Iterate through characters whose player has this character pinned | any\_pinning\_character = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | character |
| any\_player\_heir | Iterate through player heirs, capped at the first 10 | any\_player\_heir = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | character |
| any\_pool\_guest | Iterate through all guests visiting the court from the pool (in contrast to foreign\_court\_guest they don't have a liege) | any\_pool\_guest = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | character |
| any\_potential\_marriage\_option | Iterate through all potential selectable marriage or betrothal options | any\_potential\_marriage\_option = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | character |
| any\_pretender\_title | Iterate through all landed titles character is pretender to | any\_pretender\_title = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | landed title |
| any\_primary\_war\_enemy | Iterate through all primary war enemies | any\_primary\_war\_enemy = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | character |
| any\_prisoner | Iterate through all prisoners in the scoped character's dungeon | any\_prisoner = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | character |
| any\_prowess\_councillor | Iterate through all prowess-based councillors | any\_prowess\_councillor = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | character |
| any\_raid\_target | Iterate through anyone the character is hostile to due to having raided them. Only returns top lieges | any\_raid\_target = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | character |
| any\_realm\_county | Iterate through all counties in the realm. Based on top liege | any\_realm\_county = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | landed title |
| any\_realm\_de\_jure\_duchy | Iterate through all de jure duchies that have at least one county in the realm. Based on top liege | any\_realm\_de\_jure\_duchy = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | landed title |
| any\_realm\_de\_jure\_empire | Iterate through all de jures empire that have at least one county in the realm. Based on top liege | any\_realm\_de\_jure\_empire = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | landed title |
| any\_realm\_de\_jure\_kingdom | Iterate through all de jure kingdom that have at least one county in the realm. Based on top liege | any\_realm\_de\_jure\_kingdom = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | landed title |
| any\_realm\_province | Iterate through all realm provinces \[baronies?\] of a character | any\_realm\_province = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | province |
| any\_relation | Iterate through scripted relations of a given type or multiple types. If someone is multiple relations they will only be in the list once | any\_relation = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | character |
| any\_scheme | Iterate through all schemes owned by the character | any\_scheme = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | scheme |
| any\_secret | Iterate through all secrets of the character | any\_secret = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | secret |
| any\_sibling | Iterate through all siblings | any\_sibling = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | character |
| any\_spouse | Iterate through all spouses | any\_spouse = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | character |
| any\_spouse\_candidate | Iterate through all the spouse candidates of a character. WARNING: THIS IS VERY SLOW DO NOT DO IT OFTEN. | any\_spouse\_candidate = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | character |
| any\_stewardship\_councillor | Iterate through all stewardship-based councillors | any\_stewardship\_councillor = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | character |
| any\_sub\_realm\_barony | Iterate through all baronies in sub-realm | any\_sub\_realm\_barony = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | landed title |
| any\_sub\_realm\_county | Iterate through all counties in sub-realm | any\_sub\_realm\_county = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | landed title |
| any\_sub\_realm\_duchy | Iterate through all duchies in sub-realm | any\_sub\_realm\_duchy = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | landed title |
| any\_sub\_realm\_empire | Iterate through all empires in sub-realm | any\_sub\_realm\_empire = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | landed title |
| any\_sub\_realm\_kingdom | Iterate through all kingdoms in sub-realm | any\_sub\_realm\_kingdom = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | landed title |
| any\_sub\_realm\_title | Iterate through all titles in sub-realm | any\_sub\_realm\_title = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | landed title |
| any\_targeting\_faction | Iterate through all factions targeting the scoped character | any\_targeting\_faction = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | faction |
| any\_targeting\_scheme | Iterate through all schemes targeting the character | any\_targeting\_scheme = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | scheme |
| any\_targeting\_secret | Iterate through all secrets that target the specified scope | any\_targeting\_secret = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | secret |
| any\_traveling\_family\_member | Iterate though all characters that should travel with the scoped one (when moving between courts for instance); includes the scoped character | any\_traveling\_family\_member = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | character |
| any\_truce\_holder | Iterate through all characters that have a truce with this character | any\_truce\_holder = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | character |
| any\_truce\_target | Iterate through all characters this character has a truce with | any\_truce\_target = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | character |
| any\_unspent\_known\_secret | Iterate through all unspent (not revealed/blackmailed) secrets known by the character | any\_unspent\_known\_secret = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | secret |
| any\_vassal | Iterate through all DIRECT vassals | any\_vassal = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | character |
| any\_vassal\_or\_below | Iterate through ALL vassals, not just direct vassals | any\_vassal\_or\_below = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | character |
| any\_war\_ally | Iterate through all direct war allies | any\_war\_ally = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | character |
| any\_war\_enemy | Iterate through all direct war enemies | any\_war\_enemy = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | character | character |
| attraction | Attraction value for the scoped character |  | <, <=, =, !=, >, >= | character |  |
| base\_weight | Base weight of the scoped character | base\_weight > 10 | <, <=, =, !=, >, >= | character |  |
| can\_add\_hook | Will trying to hook the target character override the current hook? (if no current hook, always returns true) | can\_add\_hook = {<br>target = <character><br>type = <hook type><br>days/months/year = whatever (optional; will use the duration from the type if not provided)<br>} |  | character |  |
| can\_attack\_in\_hierarchy | Can the scope character attack the given character based on their liege-vassal relations? |  | character target | character |  |
| can\_be\_child\_of | Would the target character have been able to have children at the time of the scoped character's birth? Only age is taken into account |  | character target | character |  |
| can\_be\_parent\_of | Would the scoped character have been able to have children at the time of the target character's birth? Only age is taken into account |  | character target | character |  |
| can\_create\_faction | Can the character create the faction of the specified type against the specified character? | can\_create\_faction = { type = X target = Y } |  | character |  |
| can\_execute\_decision | Is the scoped character able to execute the given decision? |  |  | character |  |
| can\_have\_children | Can the character have children? Only checks hard blocks from traits, not fertility | can\_have\_children = yes/no | yes/no | character |  |
| can\_join\_activities | Can the character join activities? |  | yes/no | character |  |
| can\_join\_faction | Can the scope character join the faction? | can\_join\_faction = faction |  | character |  |
| can\_join\_or\_create\_faction\_against | Can the scope character create if join a faction against the target? | can\_join\_or\_create\_faction\_against = scope:faction\_target<br>can\_join\_or\_create\_faction\_against = {<br>who = scope:faction\_target<br>faction = faction\_key # optional<br>check\_in\_a\_faction = no # default: yes<br>} | character target | character |  |
| can\_start\_scheme | Can the character start the given scheme against the given character? | can\_start\_scheme = { type = X target = Y } |  | character |  |
| character\_has\_commander\_trait\_scope\_does\_not | Does the character have a commander trait that the scope does not? |  | character target | character |  |
| character\_is\_land\_realm\_neighbor | Is the scoped character a realm neighbor of the target? Meaning they're independent or have the same liege, and border your realm. |  | character target | character |  |
| character\_is\_realm\_neighbor | Is the scoped character a realm neighbor of the target? Meaning they're independent or has the same liege, and border your realm. Including across two sea zones |  | character target | character |  |
| completely\_controls | Does the character control all counties and baronies inside de jure title (no hostile occupation either)? |  | landed title scope | character | landed title |
| completely\_controls\_region | Does the character control all counties and baronies inside the specified region (no hostile occupation either)? |  |  | character | geographical region |
| council\_task\_monthly\_progress | Is the scoped character's monthly progress on their assigned council task this big? |  | <, <=, =, !=, >, >= | character |  |
| create\_faction\_type\_chance | Check if the chance to create a faction against a target of the scope character is is true against the scripted value | create\_faction\_type\_chance = {<br>```<br>   type = faction_type #An ongoing faction<br>   target = target_character<br>   value <|<=|>=|> 0<br>```<br>} |  | character |  |
| current\_weight | Current weight of the scoped character | current\_weight > 10 | <, <=, =, !=, >, >= | character |  |
| current\_weight\_for\_portrait | Current weight of the scoped character as a value for portraits scaled between 0.0 and 1.0 | current\_weight\_for\_portrait > 0.1 | <, <=, =, !=, >, >= | character |  |
| days\_in\_prison | Number of days the character has been imprisoned for (0 if not imprisoned) |  | <, <=, =, !=, >, >= | character |  |
| days\_of\_continuous\_peace | Number of days the character has been at peace (0 if at war). Raids count as 'not peace' |  | <, <=, =, !=, >, >= | character |  |
| days\_of\_continuous\_war | Number of days the character has been at war (0 if at peace) |  | <, <=, =, !=, >, >= | character |  |
| death\_reason | Does the scoped character have the given death reason? | death\_reason = death\_natural\_causes |  | character |  |
| diplomacy | Does the character have the required diplomacy skill level? |  | <, <=, =, !=, >, >= | character |  |
| diplomacy\_diff | Does the character have the required diplomacy skill level difference against target? | diplomacy = { target = character value <= script\_value abs = yes/no(optional, default no) } | <, <=, =, !=, >, >= | character |  |
| diplomacy\_for\_portrait | Diplomacy skill scaled between 0.0 and 1.0 for portraits |  | <, <=, =, !=, >, >= | character |  |
| diplomacy\_lifestyle\_perk\_points | How many diplomacy perk points does the character have available? |  | <, <=, =, !=, >, >= | character |  |
| diplomacy\_lifestyle\_perks | How many diplomacy perks does the character have? |  | <, <=, =, !=, >, >= | character |  |
| diplomacy\_lifestyle\_xp | How much diplomacy lifestyle experience does the character have? |  | <, <=, =, !=, >, >= | character |  |
| does\_ai\_liege\_in\_vassal\_contract\_desire\_obligation\_change | Does the AI liege in a vassal contract desire changing an obligation level? |  | yes/no | character |  |
| does\_ai\_vassal\_in\_vassal\_contract\_desire\_obligation\_change | Does the AI vassal in a vassal contract desire changing an obligation level? |  | yes/no | character |  |
| domain\_limit | Is the scoped character's domain limit this big? |  | <, <=, =, !=, >, >= | character |  |
| domain\_limit\_available | Is there this much space left in the character's domain limit? Negative values also work for checking characters that are above their limit |  | <, <=, =, !=, >, >= | character |  |
| domain\_limit\_percentage | Is the scoped character's domain this big in comparison to their limit? |  | <, <=, =, !=, >, >= | character |  |
| domain\_size | Is the scoped character's domain this big? |  | <, <=, =, !=, >, >= | character |  |
| dread | Does the character have the required dread? |  | <, <=, =, !=, >, >= | character |  |
| dread\_modified\_ai\_boldness | AI boldness modified by the dread of the specified character | dread\_modified\_ai\_boldness = {<br>character = root # the character whose dread is affecting the target character<br>value >= 5<br>} |  | character |  |
| effective\_age | Age of character. If immortal, age they became immortal at |  | <, <=, =, !=, >, >= | character |  |
| fertility | Does the character have the required fertility? |  | <, <=, =, !=, >, >= | character |  |
| focus\_progress | Does the character have this much focus progress? |  | <, <=, =, !=, >, >= | character |  |
| gold | GHoes the character have the required gold? |  | <, <=, =, !=, >, >= | character |  |
| government\_allows | Checks if the government of the character allows something |  |  | character |  |
| government\_disallows | Checks if the government of the character disallows something |  |  | character |  |
| government\_has\_flag | Checks if the government of the character has a specific flag |  |  | character |  |
| has\_any\_cb\_on | Does the scope character have any casus belli on the target character? |  | character target | character |  |
| has\_any\_display\_cb\_on | Does the scope character have any casus belli on the target character that should be displayed? (Allowed to fail valid\_to\_start\_display\_regardless) |  | character target | character |  |
| has\_any\_focus | Does the character have any focus set? |  | yes/no | character |  |
| has\_any\_nickname | Does the scope character have a nickname? |  | yes/no | character |  |
| has\_any\_scripted\_relation | Does the scope character have any scripted relation with the target character? |  | character target | character |  |
| has\_any\_secret\_relation | Does the scope character have any secret relationship with the target character? |  | character target | character |  |
| has\_any\_secrets | Does the character have any secrets? |  | yes/no | character |  |
| has\_bad\_nickname | Does the scope character have a bad nickname? |  | yes/no | character |  |
| has\_banish\_reason | Does the character have the banish reason towards the target? |  | character target | character |  |
| has\_cb\_on | Does the scoped character have the specified casus belli on the taget character? Invalid target returns false | has\_cb\_on = { target = X casus\_belli/cb = Y } |  | character |  |
| has\_character\_flag | Does the character have this flag? |  |  | character |  |
| has\_character\_modifier | Does the scoped character have a given modifier? | has\_character\_modifier = name |  | character |  |
| has\_character\_modifier\_duration\_remaining | Does the scoped character have the duration remaining on a given modifier? | has\_character\_modifier\_duration\_remaining = name |  | character |  |
| has\_claim\_on | Does the character have a claim on the target title? |  | landed title target | character |  |
| has\_council\_position | Does the scoped character have the given position? |  |  | character |  |
| has\_councillor\_for\_skill | Does the scoped character have a councillor for the specified skill? | has\_councillor\_for\_skill = X, where X is a skill name or 'general' |  | character |  |
| has\_culture | Does the character have this culture? |  |  | character |  |
| has\_de\_jure\_claim\_on | Does the scope character have a de jure claim against the target? |  | character target | character |  |
| has\_disable\_non\_aggression\_pacts | Does the character have disabled non-aggression pacts with the target? |  | character target | character |  |
| has\_divorce\_reason | Does the character have the divorce reason towards the target? |  | character target | character |  |
| has\_dread\_level\_towards | How scared is the scope character of the target? 0 = not intimidated, 1 = intimidated, 2 = terrified. | has\_dread\_level\_towards = {<br>target = X <br>level >/</>=/<=/= Y <br>} |  | character |  |
| has\_dynasty | Does the character have a valid dynasty? |  | yes ("no" does not work) | character |  |
| has\_election\_vote\_of | Is the target character voting for the scoped character in the election of the target title | has\_election\_vote\_of = { who = scope:actor title = primary\_title } |  | character |  |
| has\_execute\_reason | Does the character have the execute reason towards the target? |  | character target | character |  |
| has\_faith | Does the character have this faith? | has\_faith = faith:baltic\_pagan | faith scope | character | faith |
| has\_father | does the character have a valid living father? |  | yes/no | character |  |
| has\_focus | Does the character have this focus? |  |  | character |  |
| has\_free\_council\_slot | Does the scope character have a council position to fill? (ignoring automatically filled positions) |  | yes/no | character |  |
| has\_gene | Does the character have the specified gene template? Only works for morph genes. An interface trigger, can only be used in specific places | has\_gene = { category = X template = Y } |  | character |  |
| has\_government | Checks if the character has a specific government type | has\_government = X<br>Where X is any government type (e.g. feudal\_government, clan\_government, tribal\_government, etc.) |  | character |  |
| has\_had\_focus\_for\_days | Has the character had a focus for the given amount of time? |  | <, <=, =, !=, >, >= | character |  |
| has\_hook | Does the character have a hook on the target? | has\_hook = <character> | character scope | character | character |
| has\_hook\_from\_secret | Does the character have a hook based on the target's secret? | has\_hook\_from\_secret = scope:saved\_secret |  | character |  |
| has\_hook\_of\_type | Does the character have a hook on the target of the given type? | has\_hook\_of\_type = { target = X type = Y } |  | character |  |
| has\_imprisonment\_reason | Does the character have an imprisonment reason towards the target? |  | character target | character |  |
| has\_inactive\_trait | Does the character have this trait or a trait of this trait group amongst their inactive traits? |  |  | character |  |
| has\_lifestyle | Does the character have this lifestyle? |  |  | character |  |
| has\_mother | Does the character have a valid living mother? |  | yes/no | character |  |
| has\_nickname | Does the character have this nickname? |  |  | character |  |
| has\_non\_aggression\_pact | Does the character have a non-aggression pact with the target? |  | character target | character |  |
| has\_non\_interference | Does the character have the non-interference reason towards the target? |  | character target | character |  |
| has\_opinion\_modifier | Does the character have the specified opinion modifier on the target? | has\_opinion\_modifier = { target = X modifier = Y } |  | character |  |
| has\_opposite\_relation | Does the scoped character have an opposite relationship of the relation value with the target character? target = , relation = |  |  | character |  |
| has\_owned\_scheme | Does this character own a scheme? |  | yes/no | character |  |
| has\_pending\_interaction\_of\_type | Does the character have a pending interaction of the type? Only works if the scope is player-controlled. | Example: has\_pending\_interaction = interaction\_key |  | character |  |
| has\_perk | Does the character have this perk? |  |  | character |  |
| has\_primary\_title | Does the character has specific title as his primary title? |  | landed title scope | character | landed title |
| has\_raid\_immunity\_against | Is the scoped character's (top-liege) realm immune to raiding by the target due to having defeated their raid army? | has\_raid\_immunity\_against = scope:character | character scope | character | character |
| has\_raised\_armies | Does the character have raised or gathering armies? |  | yes/no | character |  |
| has\_realm\_law | Does the scoped character have the given realm law? |  |  | character |  |
| has\_realm\_law\_flag | Does the scoped character have a law with the given flag? |  |  | character |  |
| has\_relation\_best\_friend | Checks for a scripted relationship with a target character |  | character target | character |  |
| has\_relation\_bully | Checks for a scripted relationship with a target character |  | character target | character |  |
| has\_relation\_court\_physician | Checks for a scripted relationship with a target character |  | character target | character |  |
| has\_relation\_crush | Checks for a scripted relationship with a target character |  | character target | character |  |
| has\_relation\_flag | Does the scope character have a specific flag on a relation with the target character? target = , relation = , flag = |  |  | character |  |
| has\_relation\_friend | Checks for a scripted relationship with a target character |  | character target | character |  |
| has\_relation\_guardian | Checks for a scripted relationship with a target character |  | character target | character |  |
| has\_relation\_intrigue\_mentor | Checks for a scripted relationship with a target character |  | character target | character |  |
| has\_relation\_intrigue\_student | Checks for a scripted relationship with a target character |  | character target | character |  |
| has\_relation\_lover | Checks for a scripted relationship with a target character |  | character target | character |  |
| has\_relation\_mentor | Checks for a scripted relationship with a target character |  | character target | character |  |
| has\_relation\_nemesis | Checks for a scripted relationship with a target character |  | character target | character |  |
| has\_relation\_oaf | Checks for a scripted relationship with a target character |  | character target | character |  |
| has\_relation\_potential\_friend | Checks for a scripted relationship with a target character |  | character target | character |  |
| has\_relation\_potential\_lover | Checks for a scripted relationship with a target character |  | character target | character |  |
| has\_relation\_potential\_rival | Checks for a scripted relationship with a target character |  | character target | character |  |
| has\_relation\_rival | Checks for a scripted relationship with a target character |  | character target | character |  |
| has\_relation\_soldier\_friend | Checks for a scripted relationship with a target character |  | character target | character |  |
| has\_relation\_soulmate | Checks for a scripted relationship with a target character |  | character target | character |  |
| has\_relation\_student | Checks for a scripted relationship with a target character |  | character target | character |  |
| has\_relation\_victim | Checks for a scripted relationship with a target character |  | character target | character |  |
| has\_relation\_ward | Checks for a scripted relationship with a target character |  | character target | character |  |
| has\_religion | Does the character have this religion? | has\_religion = religion:buddhism\_religion | religion scope | character | religion |
| has\_revoke\_title\_reason | Does the character have the revoke title reason towards the target? |  | character target | character |  |
| has\_same\_culture\_as | Does the character have the same culture as the target? |  | character target | character |  |
| has\_same\_focus\_as | Does the character have the same focus as the other? |  | character target | character |  |
| has\_same\_government | Checks if the character has the same government type as another character |  | character target | character |  |
| has\_secret\_relation\_best\_friend | Checks for a secret scripted relationship with a target character |  | character target | character |  |
| has\_secret\_relation\_bully | Checks for a secret scripted relationship with a target character |  | character target | character |  |
| has\_secret\_relation\_court\_physician | Checks for a secret scripted relationship with a target character |  | character target | character |  |
| has\_secret\_relation\_crush | Checks for a secret scripted relationship with a target character |  | character target | character |  |
| has\_secret\_relation\_friend | Checks for a secret scripted relationship with a target character |  | character target | character |  |
| has\_secret\_relation\_guardian | Checks for a secret scripted relationship with a target character |  | character target | character |  |
| has\_secret\_relation\_intrigue\_mentor | Checks for a secret scripted relationship with a target character |  | character target | character |  |
| has\_secret\_relation\_intrigue\_student | Checks for a secret scripted relationship with a target character |  | character target | character |  |
| has\_secret\_relation\_lover | Checks for a secret scripted relationship with a target character |  | character target | character |  |
| has\_secret\_relation\_mentor | Checks for a secret scripted relationship with a target character |  | character target | character |  |
| has\_secret\_relation\_nemesis | Checks for a secret scripted relationship with a target character |  | character target | character |  |
| has\_secret\_relation\_oaf | Checks for a secret scripted relationship with a target character |  | character target | character |  |
| has\_secret\_relation\_potential\_friend | Checks for a secret scripted relationship with a target character |  | character target | character |  |
| has\_secret\_relation\_potential\_lover | Checks for a secret scripted relationship with a target character |  | character target | character |  |
| has\_secret\_relation\_potential\_rival | Checks for a secret scripted relationship with a target character |  | character target | character |  |
| has\_secret\_relation\_rival | Checks for a secret scripted relationship with a target character |  | character target | character |  |
| has\_secret\_relation\_soldier\_friend | Checks for a secret scripted relationship with a target character |  | character target | character |  |
| has\_secret\_relation\_soulmate | Checks for a secret scripted relationship with a target character |  | character target | character |  |
| has\_secret\_relation\_student | Checks for a secret scripted relationship with a target character |  | character target | character |  |
| has\_secret\_relation\_victim | Checks for a secret scripted relationship with a target character |  | character target | character |  |
| has\_secret\_relation\_ward | Checks for a secret scripted relationship with a target character |  | character target | character |  |
| has\_sexuality | Does the character's sexuality match the scripted? (heterosexual, homosexual, bisexual, asexual, none). Characters that have yet to get a sexuality (children) have none set. |  |  | character |  |
| has\_strong\_claim\_on | Does the character have a pressed claim on the target title? |  | landed title target | character |  |
| has\_strong\_hook | Does the character have a strong hook on the target? | has\_strong\_hook = <character> | character scope | character | character |
| has\_strong\_usable\_hook | Does the character have a strong hook on the target that is not on cooldown? | has\_strong\_usable\_hook = <character> | character scope | character | character |
| has\_targeting\_faction | Is there a faction targeting the scoped character? |  | yes/no | character |  |
| has\_title | Does the character hold the title? |  | landed title scope | character | landed title |
| has\_trait | Does the character have this trait or a trait of this trait group? |  |  | character |  |
| has\_trait\_rank | Compare the trait rank of a character to a value or other character. | has\_trait\_rank = {<br>```<br> trait = TRAIT_GROUP<br> rank <=> number (can be script value) # need only one of rank or character<br> character <=> character target # need only one of rank or character<br>```<br>}<br>Note that not having the trait and having rank 0 count as the same thing. rank < X on its own will therefore return true for a character that does not have the trait. |  | character |  |
| has\_trait\_with\_flag | Does the scope character have a trait with a certain flag? | has\_trait\_with\_flag = can\_not\_marry |  | character |  |
| has\_truce | Does the scope character have a truce with the target character? Truces are one way, which means we ask if the scope character can't attack the target character |  | character target | character |  |
| has\_usable\_hook | Does the character have a hook on the target that isn't on cooldown | has\_usable\_hook = <character> | character scope | character | character |
| has\_weak\_claim\_on | Does the character have an unpressed claim on the target title? |  | landed title target | character |  |
| has\_weak\_hook | Does the character have a weak hook on the target? A strong hook will \*not\* count. | has\_weak\_hook = <character> | character scope | character | character |
| health | Does the character have the required health? |  | <, <=, =, !=, >, >= | character |  |
| highest\_held\_title\_tier | What is the highest held landed title tier of the character? |  | <, <=, =, !=, >, >= | character |  |
| highest\_skill | Is the skill the highest skill (excluding prowess) of the character? True if tied for highest |  |  | character |  |
| holds\_landed\_title | Is the scope character landed (holds a county or barony)? |  | yes/no | character |  |
| important\_action\_is\_valid\_but\_invisible | Is there an important action available to the character, but they dismissed it? | important\_action\_is\_valid\_but\_invisible = important\_action\_key |  | character |  |
| important\_action\_is\_visible | Is there an important action shown to the character? | important\_action\_is\_visible = important\_action\_key |  | character |  |
| in\_activity\_type | Is the character in an activity of the specified type? |  |  | character |  |
| in\_activity\_with | Is the character in the same activity? |  | character target | character |  |
| in\_diplomatic\_range | Are the scoped character and the target character within each other's diplomatic range? |  | character target | character |  |
| intrigue | Does the character have the required intrigue skill level? |  | <, <=, =, !=, >, >= | character |  |
| intrigue\_diff | Does the character have the required intrigue skill level difference against target? | intrigue = { target = character value <= script\_value abs = yes/no(optional, default no) } | <, <=, =, !=, >, >= | character |  |
| intrigue\_for\_portrait | Intrigue skill scaled between 0.0 and 1.0 for portraits |  | <, <=, =, !=, >, >= | character |  |
| intrigue\_lifestyle\_perk\_points | How many intrigue perk points does the character have available? |  | <, <=, =, !=, >, >= | character |  |
| intrigue\_lifestyle\_perks | How many intrigue perks does the character have? |  | <, <=, =, !=, >, >= | character |  |
| intrigue\_lifestyle\_xp | How much intrigue lifestyle experience does the character have? |  | <, <=, =, !=, >, >= | character |  |
| is\_a\_faction\_leader | Is the scoped character a leader of a faction? |  | yes/no | character |  |
| is\_a\_faction\_member | Is the scoped character a member of a faction? |  | yes/no | character |  |
| is\_adult | Is the scoped character adult? |  | yes/no | character |  |
| is\_agent\_exposed\_in\_scheme | Is the scoped character an exposed agent in the target scheme? |  |  | character |  |
| is\_ai | Is the character played by AI? |  | yes/no | character |  |
| is\_alive | Is the character alive? |  | yes/no | character |  |
| is\_allied\_in\_war | Is the scoped character allied to the target character in a war? |  | character target | character |  |
| is\_allied\_to | Is the scoped character allied to the target character? |  | character target | character |  |
| is\_at\_home | Is the character at home? |  | yes/no | character |  |
| is\_at\_location | Is the character currently in the target province? |  | province target | character |  |
| is\_at\_same\_location | Is the character currently in the same province as the target character? |  | character target | character |  |
| is\_at\_war | Is the character at war? Does not consider lieges' wars |  | yes/no | character |  |
| is\_at\_war\_as\_attacker | Is the character at war as an attacker? Does not consider lieges' wars |  | yes/no | character |  |
| is\_at\_war\_as\_defender | Is the character at war as a defender? Does not consider lieges' wars |  | yes/no | character |  |
| is\_at\_war\_with | Is the character at war with the target? Does not consider lieges' wars |  | character target | character |  |
| is\_at\_war\_with\_liege | Is the character at war with their liege? |  | yes/no | character |  |
| is\_attacker\_in\_war | Is the scope character in the target war as an attacker? |  |  | character |  |
| is\_attracted\_to\_gender\_of | Does the sexuality of the scope character make them attracted to the target character? |  | character target | character |  |
| is\_attracted\_to\_men | Is the character attracted to men? |  | yes/no | character |  |
| is\_attracted\_to\_women | Is the character attracted to women? |  | yes/no | character |  |
| is\_away\_from\_court | Is the character away from the court? |  | yes/no | character |  |
| is\_betrothed | Is the scope character betrothed? |  | yes/no | character |  |
| is\_causing\_raid\_hostility\_towards | Is the scoped character making the target hostile due to having raided their (top-liege's) realm? | is\_causing\_raid\_hostility\_towards = scope:character | character scope | character | character |
| is\_character\_interaction\_potentially\_accepted | Is the character interaction specified available and potentially accepted for the target character? | is\_character\_interaction\_potentially\_accepted = {<br>```<br>   recipient = character<br>   interaction = interaction_name<br>```<br>} |  | character |  |
| is\_character\_interaction\_shown | Is the character interaction specified shown for the target character? | is\_character\_interaction\_shown = {<br>```<br>   recipient = character<br>   interaction = interaction_name<br>```<br>} |  | character |  |
| is\_character\_interaction\_valid | Is the character interaction specified valid (shown and usable) for the target character? | is\_character\_interaction\_valid = {<br>```<br>   recipient = character<br>   interaction = interaction_name<br>```<br>} |  | character |  |
| is\_character\_window\_main\_character | Does the local player have knowledge about the secret? | An interface trigger, can only be used in specific places | yes/no | character |  |
| is\_child\_of | Is the character a child of the target character? |  | character target | character |  |
| is\_claimant | Is the character a claimant to any landed titles? |  | yes/no | character |  |
| is\_clergy | Is the scoped character clergy? |  | yes/no | character |  |
| is\_close\_family\_of | Is the character a close family \[parents, children, siblings, grandparents, grandchildren\] of the target character? |  | character target | character |  |
| is\_close\_or\_extended\_family\_of | Is the character a close or extended family \[parents, children, siblings, grandparents, grandchildren, cousins, uncles, aunts, nephews, nieces\] of the target character? |  | character target | character |  |
| is\_commanding\_army | Is the character commanding an army? |  | yes/no | character |  |
| is\_concubine | Is the scoped character a concubine? |  | yes/no | character |  |
| is\_concubine\_of | Is the target character a concubine of the scoped character? |  | character target | character |  |
| is\_consort\_of | Is the character a spouse or concubine of the target character? |  | character target | character |  |
| is\_councillor | Is the scoped character a councillor? |  | yes/no | character |  |
| is\_councillor\_of | Is the scoped character a councillor for the specified character? |  | character target | character |  |
| is\_courtier | Is the scope character a courtier? |  | yes/no | character |  |
| is\_courtier\_of | Is the scoped character a courtier of the target character? |  | character target | character |  |
| is\_cousin\_of | Is the character a cousin of the target character? |  | character target | character |  |
| is\_defender\_in\_war | Is the scoped character in the target war as a defender? |  |  | character |  |
| is\_employer\_of | Is the target character a courtier of the scope character? |  | character target | character |  |
| is\_extended\_family\_of | Is the character extended family \[cousins, uncles, aunts, nephews, nieces\] of the target character? |  | character target | character |  |
| is\_female | Is the scoped character female? |  | yes/no | character |  |
| is\_forbidden\_from\_scheme | Is the scoped character forbidden from joining the target scheme? |  |  | character |  |
| is\_forced\_into\_faction | Is the scope character forced to be part of a faction? |  | yes/no | character |  |
| is\_forced\_into\_scheme | Checks if the scope character is forced into the target scheme |  |  | character |  |
| is\_foreign\_court\_guest | Is the character a guest from another a court? In contrast to is\_pool\_guest the character has a liege |  | yes/no | character |  |
| is\_foreign\_court\_guest\_of | Is the character a guest from another a court, visiting the target character's court? In contrast to is\_pool\_guest\_of the character has a liege |  | character target | character |  |
| is\_foreign\_court\_or\_pool\_guest | Is the character a guest? (is\_pool\_guest or is\_foreign\_court\_guest) |  | yes/no | character |  |
| is\_foreign\_court\_or\_pool\_guest\_of | Is the character a guest? (is\_pool\_guest\_of or is\_foreign\_court\_guest\_of) |  | character target | character |  |
| is\_grandchild\_of | Is the character a grandchild of the target character? |  | character target | character |  |
| is\_grandparent\_of | Is the character a grandparent of the target character? |  | character target | character |  |
| is\_great\_grandchild\_of | Is the character a great grandchild of the target character? |  | character target | character |  |
| is\_great\_grandparent\_of | Is the character a great grandparent of the target character? |  | character target | character |  |
| is\_heir\_of | Is the character an heir of the target \[placeholder\]? |  | character target | character |  |
| is\_immortal | Is the character immortal? |  | yes/no | character |  |
| is\_imprisoned | is the character imprisoned? |  | yes/no | character |  |
| is\_imprisoned\_by | Is the scope character imprisoned by the target character? | is\_imprisoned\_by = TARGET | character target | character |  |
| is\_in\_an\_activity | Checks whether the character is currently in, or has joined an activity |  | yes/no | character |  |
| is\_in\_army | Is the character in an army (a commander or a knight)? |  | yes/no | character |  |
| is\_in\_civil\_war | Is the character at war with their liege, or one or more of their vassals? |  | yes/no | character |  |
| is\_in\_ongoing\_great\_holy\_war | Is the character in an ongoing (i.e. the war has started) great holy war? |  | yes/no | character |  |
| is\_in\_pool\_at | Is the character in the pool the target province is a part of |  | province target | character |  |
| is\_in\_prison\_type | Is the character imprisoned in a prison of the specified type? Accepts any static modifier (see also imprison effect). | is\_in\_prison\_type = house\_arrest |  | character |  |
| is\_in\_target\_activity | Is the scope character participating in the target activity? |  |  | character |  |
| is\_in\_the\_same\_court\_as | Is the character in the same court as the target character (they have the same court owner or one is a courtier of the other)? |  | character target | character |  |
| is\_in\_the\_same\_court\_as\_or\_guest | Is the character in the same court as the target character (they have the same court owner or one is a courtier of the other)? Includes guests in the court. |  | character target | character |  |
| is\_incapable | Is the character incapable? |  | yes/no | character |  |
| is\_independent\_ruler | Is the character an independent ruler? |  | yes/no | character |  |
| is\_knight | Is the scoped character a knight? |  | yes/no | character |  |
| is\_knight\_of | Is the scoped character a knight of the target character? |  | character target | character |  |
| is\_landed | Is the scoped character landed (holds a county or barony)? |  | yes/no | character |  |
| is\_leader\_in\_war | Is the scoped character leading one of the sides in the target war? |  |  | character |  |
| is\_leading\_faction\_type | Is the character leading a faction of the specified type? |  |  | character |  |
| is\_liege\_or\_above\_of | Is the scope character a liege or above of the target character? |  | character target | character |  |
| is\_local\_player | Is the character the local player? | An interface trigger, can only be used in specific places | yes/no | character |  |
| is\_lowborn | Is the character lowborn? |  | yes/no | character |  |
| is\_male | Is the scope character male? |  | yes/no | character |  |
| is\_married | Is the scope character married? |  | yes/no | character |  |
| is\_nibling\_of | Is the character a nibling (niece/nephew) of the target character? |  | character target | character |  |
| is\_normal\_councillor | Is the scoped character a regular councillor? |  | yes/no | character |  |
| is\_obedient | Is the character obedient towards the target? |  | character target | character |  |
| is\_overriding\_designated\_winner | Is the scoped character overriding the winner in the GHW they're pledged to (will put their beneficiary on the throne if they're top participant)? |  | yes/no | character |  |
| is\_parent\_of | Is the character a parent of the target character? |  | character target | character |  |
| is\_participant\_in\_war | Is the scope character participating in the target war as an attacker or defender? |  |  | character |  |
| is\_performing\_council\_task | Is the scoped character performing the given task? |  |  | character |  |
| is\_player\_heir\_of | Is the scope character the player heir of the target character? |  | character target | character |  |
| is\_pledged\_ghw\_attacker | Is the scoped character a pledged attacker in the current GHW? (it's an error to check this if there's no GHW around) |  | yes/no | character |  |
| is\_pool\_character | Is the character in the pool? (not a ruler, courtier or guest at any court) |  | yes/no | character |  |
| is\_pool\_guest | Is the character a guest from the pool? In contrast to is\_foreign\_court\_guest the character has no liege |  | yes/no | character |  |
| is\_pool\_guest\_of | Is the character a guest from the pool, visiting the target character's court? In contrast to is\_foreign\_court\_guest\_of the character has no liege |  | character target | character |  |
| is\_powerful\_vassal | Is the character a powerful vassal? |  | yes/no | character |  |
| is\_powerful\_vassal\_of | Is the character a powerful vassal of the target? |  | character target | character |  |
| is\_pregnant | Is the character pregnant? |  | yes/no | character |  |
| is\_primary\_heir\_of | Is the character the heir of the target's primary title? |  | character target | character |  |
| is\_ruler | Is the scope character a ruler (holds any title)? |  | yes/no | character |  |
| is\_scheming\_against | Checks whether the scope character is an owner or an owner agent in a scheme against the target. There are 3 possible ways to use it: | - is\_scheming\_against = { target = X type = Y } limits to schemes of type Y<br>- is\_scheming\_against = { target = X scheme\_skill = Y } limits to schemes of Y skill category<br>- is\_scheming\_against = { target = X } considers all schemes |  | character |  |
| is\_sibling\_of | Is the character a sibling of the target character? |  | character target | character |  |
| is\_spouse\_of | Is the character a spouse of the target character, and are both alive? |  | character target | character |  |
| is\_spouse\_of\_even\_if\_dead | Is the character a spouse of the target character, even if one or both are dead? |  | character target | character |  |
| is\_theocratic\_lessee | Is the scope character a theocratic lessee (bishop)? |  | yes/no | character |  |
| is\_travelling | Is the scope character travelling ? |  | yes/no | character |  |
| is\_twin\_of | Is the character a twin of the target character? |  | character target | character |  |
| is\_unborn\_child\_of\_concubine | Is the unborn a child of a concubine? |  | yes/no | character |  |
| is\_unborn\_known\_bastard | Is the unborn a known bastard? |  | yes/no | character |  |
| is\_uncle\_or\_aunt\_of | Is the character an uncle or aunt of the target character? |  | character target | character |  |
| is\_valid\_as\_agent\_in\_scheme | Is the scope character suitable as an agent for the target scheme? |  |  | character |  |
| is\_vassal\_of | Is the character a direct vassal of the target character? |  | character target | character |  |
| is\_vassal\_or\_below\_of | Is the scoped character a vassal or below of the target character? |  | character target | character |  |
| is\_visibly\_fertile | Is the scoped character visibly fertile, that is: not too old if a woman, not too young and has no traits blocking having children |  | yes/no | character |  |
| join\_faction\_chance | Check the chance of the scope character to join the faction against the scripted value | join\_faction\_chance = {<br>```<br>   faction = faction_target #An ongoing faction<br>   value <|<=|>=|> 0<br>```<br>} |  | character |  |
| join\_scheme\_chance | Check if the chance of the scope character to join the scheme is between the given range (being min and max exclusive) | join\_scheme\_chance = {<br>```<br>   scheme = scheme_target #An ongoing scheme<br>   max = 0<br>   min = -10<br>```<br>} |  | character |  |
| learning | Does the character have the required learning skill level? |  | <, <=, =, !=, >, >= | character |  |
| learning\_diff | Does the character have the required learning skill level difference against target? | learning = { target = character value <= script\_value abs = yes/no(optional, default no) } | <, <=, =, !=, >, >= | character |  |
| learning\_for\_portrait | Learning skill scaled between 0.0 and 1.0 for portraits |  | <, <=, =, !=, >, >= | character |  |
| learning\_lifestyle\_perk\_points | How many learning lifestyle perk points does the character have available? |  | <, <=, =, !=, >, >= | character |  |
| learning\_lifestyle\_perks | How many learning lifestyle perks does the character have? |  | <, <=, =, !=, >, >= | character |  |
| learning\_lifestyle\_xp | How much learning lifestyle experience does the character have? |  | <, <=, =, !=, >, >= | character |  |
| long\_term\_gold | Does the character have the required gold? (AI category long term) |  | <, <=, =, !=, >, >= | character |  |
| martial | Does the character have the required martial skill level? |  | <, <=, =, !=, >, >= | character |  |
| martial\_diff | Does the character have the required martial skill level difference against target? | martial = { target = character value <= script\_value abs = yes/no(optional, default no) } | <, <=, =, !=, >, >= | character |  |
| martial\_for\_portrait | Martial skill scaled between 0.0 and 1.0 for portraits |  | <, <=, =, !=, >, >= | character |  |
| martial\_lifestyle\_perk\_points | How many martial perk points does the character have available? |  | <, <=, =, !=, >, >= | character |  |
| martial\_lifestyle\_perks | How many martial lifestyle perks does the character have? |  | <, <=, =, !=, >, >= | character |  |
| martial\_lifestyle\_xp | How much martial lifestyle experience does the character have? |  | <, <=, =, !=, >, >= | character |  |
| matrilinear\_betrothal | Is this character's betrothal matrilinear? False if there's no betrothal. |  | yes/no | character |  |
| matrilinear\_marriage | Is the marriage with the spouse matrilinear? |  | yes/no | character |  |
| max\_military\_strength | Is the scoped character's max military strength this big? |  | <, <=, =, !=, >, >= | character |  |
| max\_number\_maa\_soldiers\_of\_base\_type | Does the scope character have value amount of max soldiers of men at arms of the base type? |  | <, <=, =, !=, >, >= | character |  |
| max\_number\_maa\_soldiers\_of\_type | Does the scope character have value amount of max soldiers of men at arms of the type? |  | <, <=, =, !=, >, >= | character |  |
| max\_number\_of\_concubines | The maximum number of concubines a character can have | max\_number\_of\_concubines > 2 | <, <=, =, !=, >, >= | character |  |
| max\_number\_of\_knights | Check how many knights the scoped character can potentially have |  | <, <=, =, !=, >, >= | character |  |
| missing\_unique\_ancestors | The amount of missing unique ancestors from the character's real father and mother | Traverses the family tree for NDefines::NChildbirth::INBREEDING\_ANCESTOR\_GENERATIONS amount of generations. By default this means that we're traversing 62 ancestors and report the number of duplicates we find.<br>calc\_missing\_unique\_ancestors > 10 | <, <=, =, !=, >, >= | character |  |
| monthly\_character\_balance | Is the scoped character's monthly balance this big? |  | <, <=, =, !=, >, >= | character |  |
| monthly\_character\_expenses | Is the scoped character's monthly expenses this big? |  | <, <=, =, !=, >, >= | character |  |
| monthly\_character\_income | Is the scoped character's monthly income this big? |  | <, <=, =, !=, >, >= | character |  |
| num\_of\_bad\_genetic\_traits | Compare the number of bad genetic traits | <charater> = { num\_of\_bad\_genetic\_traits = 0 } | <, <=, =, !=, >, >= | character |  |
| num\_of\_good\_genetic\_traits | Compare the number of good genetic traits | <charater> = { num\_of\_good\_genetic\_traits >= 2 } | <, <=, =, !=, >, >= | character |  |
| num\_of\_relation\_best\_friend | Compares the number of scripted relations a character has of the type |  | <, <=, =, !=, >, >= | character |  |
| num\_of\_relation\_bully | Compares the number of scripted relations a character has of the type |  | <, <=, =, !=, >, >= | character |  |
| num\_of\_relation\_court\_physician | Compares the number of scripted relations a character has of the type |  | <, <=, =, !=, >, >= | character |  |
| num\_of\_relation\_crush | Compares the number of scripted relations a character has of the type |  | <, <=, =, !=, >, >= | character |  |
| num\_of\_relation\_friend | Compares the number of scripted relations a character has of the type |  | <, <=, =, !=, >, >= | character |  |
| num\_of\_relation\_guardian | Compares the number of scripted relations a character has of the type |  | <, <=, =, !=, >, >= | character |  |
| num\_of\_relation\_intrigue\_mentor | Compares the number of scripted relations a character has of the type |  | <, <=, =, !=, >, >= | character |  |
| num\_of\_relation\_intrigue\_student | Compares the number of scripted relations a character has of the type |  | <, <=, =, !=, >, >= | character |  |
| num\_of\_relation\_lover | Compares the number of scripted relations a character has of the type |  | <, <=, =, !=, >, >= | character |  |
| num\_of\_relation\_mentor | Compares the number of scripted relations a character has of the type |  | <, <=, =, !=, >, >= | character |  |
| num\_of\_relation\_nemesis | Compares the number of scripted relations a character has of the type |  | <, <=, =, !=, >, >= | character |  |
| num\_of\_relation\_oaf | Compares the number of scripted relations a character has of the type |  | <, <=, =, !=, >, >= | character |  |
| num\_of\_relation\_potential\_friend | Compares the number of scripted relations a character has of the type |  | <, <=, =, !=, >, >= | character |  |
| num\_of\_relation\_potential\_lover | Compares the number of scripted relations a character has of the type |  | <, <=, =, !=, >, >= | character |  |
| num\_of\_relation\_potential\_rival | Compares the number of scripted relations a character has of the type |  | <, <=, =, !=, >, >= | character |  |
| num\_of\_relation\_rival | Compares the number of scripted relations a character has of the type |  | <, <=, =, !=, >, >= | character |  |
| num\_of\_relation\_soldier\_friend | Compares the number of scripted relations a character has of the type |  | <, <=, =, !=, >, >= | character |  |
| num\_of\_relation\_soulmate | Compares the number of scripted relations a character has of the type |  | <, <=, =, !=, >, >= | character |  |
| num\_of\_relation\_student | Compares the number of scripted relations a character has of the type |  | <, <=, =, !=, >, >= | character |  |
| num\_of\_relation\_victim | Compares the number of scripted relations a character has of the type |  | <, <=, =, !=, >, >= | character |  |
| num\_of\_relation\_ward | Compares the number of scripted relations a character has of the type |  | <, <=, =, !=, >, >= | character |  |
| num\_sinful\_traits | Does the scoped character have this many virtuous traits? | - num\_virtuous\_traits > 5<br>- num\_virtuous\_traits = { value > 5 faith = scope:faith } to base it on what a specific faith considers virtuous | <, <=, =, !=, >, >= | character |  |
| num\_virtuous\_traits | Does the scoped character have this many virtuous traits? | - num\_virtuous\_traits > 5<br>- num\_virtuous\_traits = { value > 5 faith = scope:faith } to base it on what a specific faith considers virtuous | <, <=, =, !=, >, >= | character |  |
| number\_maa\_regiments\_of\_base\_type | Does the scoped character have value amount of men at arms of the base type? |  | <, <=, =, !=, >, >= | character |  |
| number\_maa\_regiments\_of\_type | Does the scoped character have value amount of men at arms of the type? |  | <, <=, =, !=, >, >= | character |  |
| number\_maa\_soldiers\_of\_base\_type | Does the scoped character have value amount of soldiers of men at arms of the base type? |  | <, <=, =, !=, >, >= | character |  |
| number\_maa\_soldiers\_of\_type | Does the scoped character have value amount of soldiers of men at arms of the type? |  | <, <=, =, !=, >, >= | character |  |
| number\_of\_commander\_traits | Does the character have this many commander traits? |  | <, <=, =, !=, >, >= | character |  |
| number\_of\_commander\_traits\_in\_common | Does the character and the target have a number of commander traits in common? | number\_of\_personality\_traits\_in\_common = { target = X value >/</>=/<= Y } |  | character |  |
| number\_of\_concubines | The number of concubines the scoped character has | number\_of\_concubines > 2 | <, <=, =, !=, >, >= | character |  |
| number\_of\_desired\_concubines | The number of fertile concubines the scoped character should have to not get penalties | number\_of\_desired\_concubines > 2 | <, <=, =, !=, >, >= | character |  |
| number\_of\_election\_votes | Check the number of votes the scoped character has in the target title | number\_of\_election\_votes = { title = scope:actor.primary\_title value = 0 } | <, <=, =, !=, >, >= | character |  |
| number\_of\_fertile\_concubines | The number of visibly fertile concubines the scoped character has | number\_of\_fertile\_concubines > 2 | <, <=, =, !=, >, >= | character |  |
| number\_of\_knights | Check how many knights the scoped character has at the moment |  | <, <=, =, !=, >, >= | character |  |
| number\_of\_lifestyle\_traits | Does the character have this many lifestyle traits? |  | <, <=, =, !=, >, >= | character |  |
| number\_of\_maa\_regiments | The number of men at arms the scoped character has |  | <, <=, =, !=, >, >= | character |  |
| number\_of\_opposing\_personality\_traits | Does the character and the target have a number of opposing personality traits? | number\_of\_opposing\_personality\_traits = { target = X value >/</>=/<= Y } |  | character |  |
| number\_of\_opposing\_traits | Does the character and the target have a number of opposing traits? | number\_of\_opposing\_traits = { target = X value >/</>=/<= Y } |  | character |  |
| number\_of\_personality\_traits | Does the character have this many personality traits? |  | <, <=, =, !=, >, >= | character |  |
| number\_of\_personality\_traits\_in\_common | Does the character and the target have a number of personality traits in common? | number\_of\_personality\_traits\_in\_common = { target = X value >/</>=/<= Y } |  | character |  |
| number\_of\_powerful\_vassals | Does the character have a specified number of powerful vassals? |  | <, <=, =, !=, >, >= | character |  |
| number\_of\_traits | Does the character have this many traits? |  | <, <=, =, !=, >, >= | character |  |
| number\_of\_traits\_in\_common | Does the character and the target have a number of traits in common? | number\_of\_traits\_in\_common = { target = X value >/</>=/<= Y } |  | character |  |
| opinion | Is the character's opinion of the target greater or equal than the value? | opinion = { target = X \[\*value >/</>=/<= Y\* or \*value = { min max }\* } |  | character |  |\
| owns\_a\_story | Ćhecks whether the scope character is the owner of any currently active story |  | yes/no | character |  |\
| owns\_an\_activity | Checks whether the scope character is the owner of any currently active activity |  | yes/no | character |  |\
| owns\_story\_of\_type | Does the character own a story of this type? |  |  | character |  |\
| patrilinear\_betrothal | Is this character's betrothal patrilinear? False if there's no betrothal. |  | yes/no | character |  |\
| patrilinear\_marriage | Is the marriage with the spouse patrilinear? |  | yes/no | character |  |\
| perk\_points | Does the character have this many perk points across all lifestyles combined? |  | <, <=, =, !=, >, >= | character |  |\
| perk\_points\_assigned | Does the character have this many perks across all lifestyles combined? |  | <, <=, =, !=, >, >= | character |  |\
| perks\_in\_tree | Does the character have this many perk points assigned to this tree? perks\_in\_tree = { tree = tree\_key value > 5 } |  | <, <=, =, !=, >, >= | character |  |\
| piety | Does the character have the required piety? |  | <, <=, =, !=, >, >= | character |  |\
| piety\_level | Does the character have the required devotion level? |  | <, <=, =, !=, >, >= | character |  |\
| player\_heir\_position | Check where the target character is in the scoped character's player heir list. | player\_heir\_position = { target = scope:actor position = 0 } | <, <=, =, !=, >, >= | character |  |\
| pregnancy\_days | How long has the character been pregnant? Counts from impregnation, not reveal |  | <, <=, =, !=, >, >= | character |  |\
| prestige | Does the character have the required prestige? |  | <, <=, =, !=, >, >= | character |  |\
| prestige\_level | Does the character have the required fame level? |  | <, <=, =, !=, >, >= | character |  |\
| prowess | Does the character have the required prowess skill level? |  | <, <=, =, !=, >, >= | character |  |\
| prowess\_diff | Does the character have the required prowess skill level difference against target? | prowess = { target = character value <= script\_value abs = yes/no(optional, default no) } | <, <=, =, !=, >, >= | character |  |\
| prowess\_for\_portrait | Prowess skill scaled between 0.0 and 1.0 for portraits |  | <, <=, =, !=, >, >= | character |  |\
| ransom\_cost | What is the ransom cost of the character? |  | <, <=, =, !=, >, >= | character |  |\
| realm\_size | Is the scoped character's top liege's realm this big (# of counties)? |  | <, <=, =, !=, >, >= | character |  |\
| realm\_to\_title\_distance\_squared | Is the character's realm within this distance of the title? Distance is in pixels, squared for performance reasons. | realm\_to\_title\_distance\_squared = { title = some\_title value > 10000 } | <, <=, =, !=, >, >= | character |  |\
| reverse\_has\_opinion\_modifier | <=\|=\|>=\|\> X\* or \*value = { MIN MAX }\* inclusive) |  |  | character |  |\
| reverse\_opinion | What is the target character's opinion of the scope character? opinion = { target = X value >/</>=/<= Y } |  |  | character |  |\
| scriptedtests\_can\_marry\_character | Can the character marry the target character? |  | character target | character |  |\
| scriptedtests\_dread\_base | Does the character have the specified natural dread? |  | <, <=, =, !=, >, >= | character |  |\
| scriptedtests\_piety\_income | does the character have the specified piety income? |  | <, <=, =, !=, >, >= | character |  |\
| sex\_opposite\_of | Are the scope character and the target character of opposite sex? |  | character target | character |  |\
| sex\_same\_as | Are the scope character and the target character of the same sex? |  | character target | character |  |\
| short\_term\_gold | Does the character have the required gold? (AI category short term) |  | <, <=, =, !=, >, >= | character |  |\
| should\_show\_disturbing\_portrait\_modifiers | Is the character the local player? | An interface trigger, can only be used in specific places | yes/no | character |  |\
| stewardship | Does the character have the required stewardship skill level? |  | <, <=, =, !=, >, >= | character |  |\
| stewardship\_diff | Does the character have the required stewardship skill level difference against target? | stewardship = { target = character value <= script\_value abs = yes/no(optional, default no) } | <, <=, =, !=, >, >= | character |  |\
| stewardship\_for\_portrait | Stewardship skill scaled between 0.0 and 1.0 for portraits |  | <, <=, =, !=, >, >= | character |  |\
| stewardship\_lifestyle\_perk\_points | How many perk points available does the character have? |  | <, <=, =, !=, >, >= | character |  |\
| stewardship\_lifestyle\_perks | How many perks from this lifestyle does the character have? |  | <, <=, =, !=, >, >= | character |  |\
| stewardship\_lifestyle\_xp | How many stewardship perk points does the character have available? |  | <, <=, =, !=, >, >= | character |  |\
| stress | Does the character have the required stress? |  | <, <=, =, !=, >, >= | character |  |\
| stress\_level | Does the character have the required stress level? |  | <, <=, =, !=, >, >= | character |  |\
| sub\_realm\_size | Is the scoped character's sub-realm this big (# of counties)? |  | <, <=, =, !=, >, >= | character |  |\
| target\_is\_liege\_or\_above | Is the target character the liege or above the scoped character? |  | character target | character |  |\
| target\_is\_same\_character\_or\_above | Is the target character the scoped character or above them in the vassal hierarchy? |  | character target | character |  |\
| target\_is\_vassal\_or\_below | Is the target character a vassal or below of the scope character? |  | character target | character |  |\
| target\_weight | Target weight of the scoped character | target\_weight > 10 | <, <=, =, !=, >, >= | character |  |\
| tier\_difference | What is the difference in highest held title tier between the scoped character and the target character? (-5 to 5) | For example, this is true:<br>scope:a\_baron = {<br>```<br>   tier_difference = {<br>       target = scope:a_king<br>       value = -3<br>   }<br>```<br>} |  | character |  |\
| time\_in\_prison | How long has the character been imprisoned? time\_in\_prison = { days/months/years =,>,< X } |  |  | character |  |\
| time\_in\_prison\_type | How long has the character been imprisoned with the current imprisonment type? time\_in\_prison\_type = { days/months/years =,>,< X } |  |  | character |  |\
| trait\_compatibility | target = other character value >/</= sum of trait compatibility values |  |  | character |  |\
| tyranny | Does the character have the required tyranny? |  | <, <=, =, !=, >, >= | character |  |\
| vassal\_contract\_has\_flag | Do any of the current active obligations in the scoped character's vassal contract have the given flag? |  |  | character |  |\
| vassal\_contract\_has\_modifiable\_obligations | Can the scoped character's contract be modified at all? That is: they have one, they use obligation levels, and are count or above |  | yes/no | character |  |\
| vassal\_contract\_is\_blocked\_from\_modification | Has the scoped character's contract been blocked from modification by script via 'set\_vassal\_contract\_modification\_blocked'? |  | yes/no | character |  |\
| vassal\_contract\_obligation\_level\_can\_be\_decreased | Can the obligation level of the scoped character's vassal contract be decreased? |  |  | character |  |\
| vassal\_contract\_obligation\_level\_can\_be\_increased | Can the obligation level of the scoped character's vassal contract be increased? |  |  | character |  |\
| vassal\_count | Does the scoped character have this many vassals (excluding barons)? |  | <, <=, =, !=, >, >= | character |  |\
| vassal\_limit | Is the scoped character's vassal limit this big? |  | <, <=, =, !=, >, >= | character |  |\
| vassal\_limit\_available | Is there this much space left in the character's vassal limit? Negative values also work for checking characters that are above their limit |  | <, <=, =, !=, >, >= | character |  |\
| vassal\_limit\_percentage | Is the scoped character's vassal count this big in comparison to their limit? |  | <, <=, =, !=, >, >= | character |  |\
| yearly\_character\_balance | Is the scoped character's yearly balance this big? |  | <, <=, =, !=, >, >= | character |  |\
| yearly\_character\_expenses | Is the scoped character's yearly expenses this big? |  | <, <=, =, !=, >, >= | character |  |\
| yearly\_character\_income | Is the scoped character's yearly income this big? |  | <, <=, =, !=, >, >= | character |  |\
| yields\_alliance | Checks if the character would get an alliance with the target character through such a marriage. |  |  | character |  |\
| any\_faction\_county\_member | Iterate through all faction county members | any\_faction\_county\_member = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | faction | landed title |\
| any\_faction\_member | Iterate through all faction character members | any\_faction\_member = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | faction | character |\
| average\_faction\_opinion | Average opinion of all the characters of the faction scope target |  | <, <=, =, !=, >, >= | faction |  |\
| average\_faction\_opinion\_not\_powerful\_vassal | Average opinion of the character that are _not_ powerful vassals of the faction scope target |  | <, <=, =, !=, >, >= | faction |  |\
| average\_faction\_opinion\_powerful\_vassal | Average opinion of the character that are powerful vassals of the faction scope target |  | <, <=, =, !=, >, >= | faction |  |\
| faction\_can\_press\_demands | Can the scoped faction press demands? |  | yes/no | faction |  |\
| faction\_discontent | Current discontent of the faction |  | <, <=, =, !=, >, >= | faction |  |\
| faction\_is\_at\_war | Is the scoped faction at war? |  | yes/no | faction |  |\
| faction\_is\_type | Is the faction of this type? |  |  | faction |  |\
| faction\_power | Current power of the faction. Uses percentages as whole numbers. | faction\_power >= 80 | <, <=, =, !=, >, >= | faction |  |\
| faction\_power\_threshold | Current power threshold of the faction |  | <, <=, =, !=, >, >= | faction |  |\
| has\_special\_character | Does the faction have a special character assigned? |  | yes/no | faction |  |\
| has\_special\_title | Does the faction have a special title assigned? |  | yes/no | faction |  |\
| number\_of\_faction\_members\_in\_council | Current number of faction members in faction |  | <, <=, =, !=, >, >= | faction |  |\
| any\_war\_attacker | Iterate through all attackers in the war | any\_war\_attacker = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | war | character |\
| any\_war\_defender | Iterate through all defenders in the war | any\_war\_defender = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | war | character |\
| any\_war\_participant | Iterate through all participants in the war | any\_war\_participant = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | war | character |\
| attacker\_war\_score | Compares the attacker war score |  | <, <=, =, !=, >, >= | war |  |\
| days\_since\_max\_war\_score | Number of days since the war score has been at max (+100 or −100). Returns -1 if the war score is not +100 or −100 |  | <, <=, =, !=, >, >= | war |  |\
| defender\_war\_score | Compares the defender war score |  | <, <=, =, !=, >, >= | war |  |\
| has\_valid\_casus\_belli | Does the war interaction still have a valid casus belli? (Those should be automatically removed on daily tick, but can exist for a tick) |  | yes/no | war |  |\
| is\_attacker | Is the target character in the scope war as an attacker? |  | character target | war |  |\
| is\_civil\_war | Check if the scope war is a civil war or not |  | yes/no | war |  |\
| is\_defender | Is the target character in the scoped war as a defender? |  | character target | war |  |\
| is\_participant | Is the target character participating in the scope war as either an attacker or defender? |  | character target | war |  |\
| is\_war\_leader | Is the target character leading one of the sides in the scoped war? |  | character target | war |  |\
| is\_white\_peace\_possible | Check if the scoped war's CB allows white peace (is\_white\_peace\_possible = yes) |  | yes/no | war |  |\
| using\_cb | Is the scope war using the specified CB? | using\_cb = religious\_war |  | war |  |\
| war\_contribution | Checks how much a character has contributed to the scoped war | war\_contribution = {<br>target = some character<br>value > 5<br>} |  | war |  |\
| war\_days | Compares the number of days the war has gone on for |  | <, <=, =, !=, >, >= | war |  |\
| was\_called | Has the target character been called to the scope war already? |  | character target | war |  |\
| any\_defensive\_great\_holy\_wars | Iterate through all great holy wars this faith is defending against | any\_defensive\_great\_holy\_wars = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | faith | great holy war |\
| any\_faith\_holy\_order | Iterate through all holy orders of the faith | any\_faith\_holy\_order = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | faith | holy order |\
| any\_holy\_site | Iterate through all holy site baronies of a faith | any\_holy\_site = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | faith | landed title |\
| controls\_holy\_site | Does the faith control a holy site? controls\_holy\_site = key\_of\_holy\_site |  |  | faith |  |\
| controls\_holy\_site\_with\_flag | Does the faith control a holy site with the given flag? controls\_holy\_site\_with\_flag = some flag |  |  | faith |  |\
| estimated\_faith\_strength | How strong is the scoped faith? \*Expensive\*, if you're gonna use the value repeatedly, save it to a scope first! This is scaled by a factor of 1000, so '1' means 1000 men. This is due to the cap of ~2 million, which would be too low in many cases |  | <, <=, =, !=, >, >= | faith |  |\
| faith\_hostility\_level | What is the faith's hostility level towards the target faith? | faith\_hostility\_level { target = scope:some\_faith value > 1 }<br>The levels are<br>- 0 righteous<br>- 1 astray<br>- 2 hostile<br>- 3 evil | <, <=, =, !=, >, >= | faith |  |\
| faith\_hostility\_level\_comparison | Compares the scoped faith's hostility level towards two other faiths. | faith\_hostility\_level\_comparison { faith1 > faith2 } |  | faith |  |\
| fervor | What is the faith's fervor? |  | <, <=, =, !=, >, >= | faith |  |\
| has\_allowed\_gender\_for\_clergy | Is the target character of the allowed gender to be clergy of the faith? |  | character target | faith |  |\
| has\_doctrine | Does the given faith have the given doctrine? | has\_doctrine = doctrine\_key |  | faith |  |\
| has\_doctrine\_parameter | Does the given faith have the given doctrine parameter? Can only check for bool parameters. | has\_doctrine\_parameter = parameter\_key |  | faith |  |\
| has\_dominant\_ruling\_gender | Is the target character's gender of the dominant gender of the faith? True if there's no dominant gender |  | character target | faith |  |\
| has\_graphical\_faith | Does the faith have this graphical faith? | <faith> = { has\_graphical\_faith = orthodoxgfx } |  | faith |  |\
| has\_icon | Does the faith have the given icon? | has\_icon = some\_cool\_custom\_icon |  | faith |  |\
| has\_preferred\_gender\_for\_clergy | Is the target character of the preferred gender to be clergy of the faith? |  | character target | faith |  |\
| holy\_sites\_controlled | How many holy sites does the faith control? | holy\_sites\_controlled > 1 | <, <=, =, !=, >, >= | faith |  |\
| num\_character\_followers | How many characters follow the scoped faith? | num\_character\_followers > 0 | <, <=, =, !=, >, >= | faith |  |\
| num\_county\_followers | How many counties follow the scoped faith? | num\_county\_followers > 0 | <, <=, =, !=, >, >= | faith |  |\
| religion\_tag | Checks the tag of the religion of the current faith | religion\_tag = christianity\_religion |  | faith |  |\
| trait\_is\_sin | Does the scoped faith consider the given trait sinful? | trait\_is\_sin = lustful |  | faith |  |\
| trait\_is\_virtue | Does the scoped faith consider the given trait virtuous? | trait\_is\_virtue = lustful |  | faith |  |\
| any\_secret\_knower | Iterate through all characters who know the scoped secret | any\_secret\_knower = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | secret | character |\
| any\_secret\_participant | Iterate through participants in a secret | any\_secret\_participant = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | secret | character |\
| can\_be\_exposed\_by | Can the scope secret be exposed by the target character? | can\_be\_exposed\_by = target | character target | secret |  |\
| is\_criminal\_for | Is this secret criminal for the target participant? | is\_criminal\_for = <character> | character scope | secret | character |\
| is\_known\_by | Is the scoped secret known by the target character? |  | character target | secret |  |\
| is\_shunned\_for | Is this secret shunned for the target participant? | is\_shunned\_for = <character> | character scope | secret | character |\
| is\_shunned\_or\_criminal\_for | Is this secret shunned or criminal for the target participant? | is\_shunned\_or\_illegal\_for = <character> | character scope | secret | character |\
| is\_spent\_by | Has the scoped secret been spent by the target character? | is\_spent\_by = target | character target | secret |  |\
| local\_player\_knows\_this\_secret | Does the local player know about the secret? | An interface trigger, can only be used in specific places | yes/no | secret |  |\
| same\_secret\_type\_as | Is the scoped secret of the same type as the target secret? | same\_secret\_type\_as = scope:some\_secret |  | secret |  |\
| secret\_type | Is the scoped secret of the specified type? |  |  | secret |  |\
| available\_loot | How much gold is available to loot for raiding armies? | available\_loot >= 7 | <, <=, =, !=, >, >= | province |  |\
| building\_slots | How many building slots exist (including occupied ones)? | building\_slots > 3 | <, <=, =, !=, >, >= | province |  |\
| combined\_building\_level | How many levels of normal buildings are there? Duchy and such buildings do not count. Building under construction does not count. The capital building does count | combined\_building\_level > 10 | <, <=, =, !=, >, >= | province |  |\
| fort\_level | Compares the fort level of a province |  | <, <=, =, !=, >, >= | province |  |\
| free\_building\_slots | How many free building slots exist? A building under construction is considered to be taking a slot | free\_building\_slots > 3 | <, <=, =, !=, >, >= | province |  |\
| geographical\_region | Checks if a province is in a certain geographical region |  |  | province |  |\
| has\_building | Does the scoped province have a particular building? | has\_building = temple\_01 |  | province |  |\
| has\_building\_or\_higher | Does the scoped province have a particular building or one of its upgrades? | has\_building\_or\_higher = temple\_01 |  | province |  |\
| has\_building\_with\_flag | Does the scoped province have a building with a certain flag? | - has\_building\_with\_flag = { flag = temple count >= 2 }<br>- has\_building\_with\_flag = temple # count >= 1 |  | province |  |\
| has\_construction\_with\_flag | Does the scoped province have a construction of a building with the specified flag? | has\_construction\_with\_flag = temple |  | province |  |\
| has\_free\_building\_slot | Does the scoped province have a free building slot? | has\_free\_building\_slot = yes | yes/no | province |  |\
| has\_holding\_type | Does the scope province have a holding of particular type? | has\_holding\_type = castle\_holding |  | province |  |\
| has\_ongoing\_construction | Does the scoped province have a construction ongoing? | has\_ongoing\_construction = yes | yes/no | province |  |\
| has\_province\_modifier | Does the scoped province have a given modifier? | has\_province\_modifier = name |  | province |  |\
| has\_province\_modifier\_duration\_remaining | Does the scoped province have the duration remaining on a given modifier? | has\_province\_modifier\_duration\_remaining = name |  | province |  |\
| has\_special\_building | Does the province (holding) have a special building? |  | yes/no | province |  |\
| has\_special\_building\_slot | Does the province (holding) have a special building slot? |  | yes/no | province |  |\
| is\_coastal | is the province a coastal province? |  | yes/no | province |  |\
| is\_county\_capital | Is the province the county capital? |  | yes/no | province |  |\
| monthly\_income | Check the income of the scoped province | monthly\_income > 10 | <, <=, =, !=, >, >= | province |  |\
| num\_buildings | How many normal buildings are there? Duchy and such buildings do not count. A building under construction does count | num\_buildings > 3 | <, <=, =, !=, >, >= | province |  |\
| number\_of\_characters\_in\_pool | Check the number of characters in the pool the scoped province is a part of |  | <, <=, =, !=, >, >= | province |  |\
| terrain | Checks if a province is of a specific terrain type |  |  | province |  |\
| any\_leased\_title | Iterate through all titles leased to the scoped holy order | any\_leased\_title = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | holy order | landed title |\
| num\_leased\_titles | How many holdings the holy order has under lease |  | <, <=, =, !=, >, >= | holy order |  |\
| activity\_has\_been\_activated | Is the activity activated? |  | yes/no | activity |  |\
| any\_activity\_declined | Iterate through all characters who declined an activity invite to a specific activity | any\_activity\_declined = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | activity | character |\
| any\_activity\_invited | Iterate through all characters who have unanswered invites to a specific activity | any\_activity\_invited = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | activity | character |\
| any\_participant | Iterate through all participants in an activity | any\_participant = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | activity | character |\
| is\_target\_participating | Is the target character participating in the scoped activity? |  | character target | activity |  |\
| number\_of\_participants | The number of activity participants (including the owner) |  | <, <=, =, !=, >, >= | activity |  |\
| any\_target\_title | Iterate through all casus belli's target titles | any\_target\_title = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | casus belli | landed title |\
| army\_is\_moving | Is this army moving? |  | yes/no | army |  |\
| army\_max\_size | What is this army's max size? |  | <, <=, =, !=, >, >= | army |  |\
| army\_size | what size is this army? |  | <, <=, =, !=, >, >= | army |  |\
| is\_army\_in\_combat | Is the scoped army in combat? |  | yes/no | army |  |\
| is\_army\_in\_raid | Is the scoped army in a raid (this includes a raid interrupted by combat)? |  | yes/no | army |  |\
| is\_army\_in\_siege | Is the scoped army in a siege (this includes a siege interrupted by combat)? |  | yes/no | army |  |\
| is\_army\_in\_siege\_relevant\_for | Is the scoped army in a siege that is relevant to the target character? | is\_army\_in\_siege\_relevant\_for = scope:character | character scope | army | character |\
| is\_raid\_army | Is the scoped army a raid army? |  | yes/no | army |  |\
| raid\_loot | How much raid loot is the army carrying? |  | <, <=, =, !=, >, >= | army |  |\
| building\_max\_garrison | The max amount of garrison in a county or province from buildings | building\_max\_garrison > 100 | <, <=, =, !=, >, >= | landed title, province |  |\
| building\_levies | The amount of levies in a county or province from buildings | levies > 100 | <, <=, =, !=, >, >= | landed title, province |  |\
| squared\_distance | How far away is the province/barony/county from the target? Measured in map pixels. Squared for performance reasons (square root is expensive). squared\_distance = { target = some province/barony/county value > 10000 } |  | <, <=, =, !=, >, >= | landed title, province |  |\
| add\_to\_temporary\_list | Saves a temporary target for use during the trigger execution | This is used to build lists in triggers.<br>If used within an any-trigger, placement within the trigger is quite important. The game will iterate through every instance of the any-trigger until it finds a single instance that fulfills the requirements, and then it will stop.<br>In order to add every instance of a scope that fulfills certain conditions, use "count = all" while also placing this "effect" at the very end of the any-trigger (so that every condition is evaluated for every iteration). |  | none |  |\
| any\_barony | Iterate through all baronies in the game | any\_barony = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | none | landed title |\
| any\_county | Iterate through all counties in the game | any\_county = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | none | landed title |\
| any\_county\_in\_region | Iterate through all counties in the region. Put 'region = region\_name' inside it | any\_county\_in\_region = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | none | landed title |\
| any\_duchy | Iterate through all duchies in the game | any\_duchy = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | none | landed title |\
| any\_empire | Iterate through all empires in the game | any\_empire = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | none | landed title |\
| any\_in\_global\_list | Iterate through all items in global list. list = name or variable = name | any\_in\_global\_list = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | none |  |\
| any\_in\_list | Iterate through all items in list. list = name or variable = name | any\_in\_list = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | none |  |\
| any\_in\_local\_list | Iterate through all items in local list. list = name or variable = name | any\_in\_local\_list = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | none |  |\
| any\_independent\_ruler | Iterate through independent rulers of count tier or above | any\_independent\_ruler = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | none | character |\
| any\_kingdom | Iterate through all kingdoms in the game | any\_kingdom = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | none | landed title |\
| any\_living\_character | Iterate through all living characters | any\_living\_character = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | none | character |\
| any\_player | Iterate through all player characters | any\_player = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | none | character |\
| any\_pool\_character | Iterate through all characters in the pool of the given province | any\_pool\_character = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | none | character |\
| any\_province | Iterate through all provinces (skips non-land and impassable provinces) | any\_province = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | none | province |\
| any\_religion\_global | Iterate through all religions in the game | any\_religion\_global = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | none | religion |\
| any\_ruler | Iterate through all rulers of count tier or above | any\_ruler = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | none | character |\
| assert\_if | Conditionally cause an assert during run time | assert\_if = { limit = { X } text = Y }, where X is a trigger and Y is an optional string |  | none |  |\
| assert\_read | Conditionally cause an assert during read time | assert\_read = X, where X is yes or the string to be printed in the assert |  | none |  |\
| calc\_true\_if | Returns true if the specified number of sub-triggers return true | calc\_true\_if = { amount = 2 <trigger> <trigger> <trigger> } |  | none |  |\
| can\_start\_tutorial\_lesson | Can the specified tutorial lesson be started? | can\_start\_tutorial\_lesson = reactive\_advice\_succession<br>An interface trigger, can only be used in specific places |  | none |  |\
| current\_computer\_date | Compare the current computer date. | An interface trigger, can only be used in specific places | <, =, \> valid date | none |  |\
| current\_computer\_date\_day | Compare the current computer day. | An interface trigger, can only be used in specific places | <, <=, =, !=, >, >= | none |  |\
| current\_computer\_date\_month | Compare the current computer month. | An interface trigger, can only be used in specific places | <, <=, =, !=, >, >= | none |  |\
| current\_computer\_date\_year | Compare the current computer year. | An interface trigger, can only be used in specific places | <, <=, =, !=, >, >= | none |  |\
| current\_date | Compare the current ingame date. |  | <, =, \> valid date | none |  |\
| current\_month | Compare the current ingame month (1..12) |  | <, <=, =, !=, >, >= | none |  |\
| current\_tooltip\_depth | What is number of tooltips open rigth now? | An interface trigger, can only be used in specific places | <, <=, =, !=, >, >= | none |  |\
| custom\_description | Wraps triggers that get a custom description instead of the auto-generated one | custom\_description = {<br>text = <trigger\_localization\_key><br>subject = <optional subject scope> #defaults to current scope<br>object = <optional object scope><br>value = <optional script value><br>... triggers ...<br>} |  | none |  |\
| custom\_tooltip | Replaces the tooltips for the enclosed triggers with a custom text | custom\_tooltip = {<br>text = <text><br><trigger><br>} |  | none |  |\
| debug\_only | Checks if the game is in debug mode or not. |  | yes/no | none |  |\
| exists | Checks whether the specified socope target exists (check for not being the null object) | exists = from.owner.var:cool\_var.mother |  | none |  |\
| game\_start\_date | Compare the date of the bookmarked game launched. |  | <, =, \> valid date | none |  |\
| global\_variable\_list\_size | Checks the size of a variable list | variable\_list\_size = { name = X value >= Y }<br>- X is the name of the variable<br>- Y is a script value or number |  | none |  |\
| has\_dlc | Does the host have this DLC? |  |  | none |  |\
| has\_game\_rule | Is the given game rule setting enabled? | has\_game\_rule = faster\_conversion |  | none |  |\
| has\_global\_variable | Checks whether the current scope has the specified variable set | has\_variable = name |  | none |  |\
| has\_global\_variable\_list | Checks whether the current scope has the specified variable list set | has\_variable\_list = name |  | none |  |\
| has\_local\_variable | Checks whether the current scope has the specified variable set | has\_variable = name |  | none |  |\
| has\_local\_variable\_list | Checks whether the current scope has the specified variable list set | has\_variable\_list = name |  | none |  |\
| has\_map\_mode | Checks if the current map mode is the specified one | has\_map\_mode = realms<br>An interface trigger, can only be used in specific places |  | none |  |\
| has\_multiple\_players | Does the game have at least two players currently connected? |  | yes/no | none |  |\
| has\_variable | Checks whether the current scope has the specified variable set | has\_variable = name |  | none |  |\
| has\_variable\_list | Checks whether the current scope has the specified variable list set | has\_variable\_list = name |  | none |  |\
| has\_war\_result\_message\_with\_outcome | Is there a war result message with the specified outcome? | has\_war\_result\_message\_with\_outcome = victory/defeat/white\_peace/invalidated/any<br>An interface trigger, can only be used in specific places |  | none |  |\
| is\_bad\_nickname | Is the nickname bad? |  |  | none |  |\
| is\_frontend\_character\_selected | is the specified front end character selected (also can be used with "= yes" and "= no")? | An interface trigger, can only be used in specific places |  | none |  |\
| is\_game\_view\_open | is the specified in-game view open? | An interface trigger, can only be used in specific places |  | none |  |\
| is\_gamestate\_tutorial\_active | Is the gamestate tutorial active? See save\_progress\_in\_gamestate in tutorial\_lesson\_chains documentation. | An interface trigger, can only be used in specific places | yes/no | none |  |\
| is\_in\_list | Checks if a target in in a list |  |  | none |  |\
| is\_player\_selected | is the player playing a character? | An interface trigger, can only be used in specific places | yes/no | none |  |\
| is\_target\_in\_global\_variable\_list | Checks if a target is in a variable list | is\_target\_in\_variable\_list = { name = X target = Y }<br>- X is the name of the variable<br>- Y is an event target |  | none |  |\
| is\_target\_in\_local\_variable\_list | Checks if a target is in a variable list | is\_target\_in\_variable\_list = { name = X target = Y }<br>- X is the name of the variable<br>- Y is an event target |  | none |  |\
| is\_target\_in\_variable\_list | Checks if a target is in a variable list | is\_target\_in\_variable\_list = { name = X target = Y }<br>- X is the name of the variable<br>- Y is an event target |  | none |  |\
| is\_tooltip\_with\_name\_open | Is the tooltip with the specified name open? | An interface trigger, can only be used in specific places |  | none |  |\
| is\_tutorial\_active | Is the tutorial active? | An interface trigger, can only be used in specific places | yes/no | none |  |\
| is\_tutorial\_lesson\_active | Is this the current tutorial lesson? | is\_tutorial\_lesson\_active = reactive\_advice\_succession<br>An interface trigger, can only be used in specific places |  | none |  |\
| is\_tutorial\_lesson\_chain\_completed | Has the tutorial lesson chain with the specified key been finished? | An interface trigger, can only be used in specific places |  | none |  |\
| is\_tutorial\_lesson\_completed | has the tutorial lesson with the specified name been finished? | An interface trigger, can only be used in specific places |  | none |  |\
| is\_tutorial\_lesson\_step\_completed | Has the tutorial lesson step been finished? | is\_tutorial\_lesson\_step\_completed = lesson\_key:step\_key<br>An interface trigger, can only be used in specific places |  | none |  |\
| is\_war\_overview\_tab\_open | is the war overview open at a specified tab (victory, defeat, white\_peace)? | An interface trigger, can only be used in specific places |  | none |  |\
| is\_widget\_open | is the widget with the specified name open? | Separting strings with dots will search for specific children of children e.g. appa.foo vs baz.foo<br>An interface trigger, can only be used in specific places |  | none |  |\
| list\_size | Checks the size of a list | list\_size = { name = X value >= Y }<br>- X is the name of the list<br>- Y is a script value | <, <=, =, !=, >, >= | none |  |\
| local\_variable\_list\_size | Checks the size of a variable list | variable\_list\_size = { name = X value >= Y }<br>- X is the name of the variable<br>- Y is a script value or number |  | none |  |\
| monarchs\_journey\_unlock |  | An interface trigger, can only be used in specific places |  | none |  |\
| release\_only | Checks if the game is in release mode or not. |  | yes/no | none |  |\
| save\_temporary\_scope\_as | Saves a temporary target for use during the trigger execution |  |  | none |  |\
| save\_temporary\_scope\_value\_as | Saves a numerical or bool value as an arbitrarily-named temporary target to be referenced later in the same effect | save\_temporary\_scope\_value\_as = { name = <string> value = x } |  | none |  |\
| scripted\_tests | Checks if the game is currently running scripted tests. |  | yes/no | none |  |\
| time\_of\_year | Check if the current date is within the bounds | time\_of\_year = {<br>```<br>   min = 11.1 # default: beginning of year<br>   max = 2.29 # default: end of year<br>```<br>}<br>Dates are formatted as "<month>.<day>" or just "<month>".<br>The check includes the min and max dates.<br>min can be larger than max, in this case we wrap around to the next year (i.e., February is between October and March). |  | none |  |\
| variable\_list\_size | Checks the size of a variable list | variable\_list\_size = { name = X value >= Y }<br>- X is the name of the variable<br>- Y is a script value or number |  | none |  |\
| weighted\_calc\_true\_if | Returns true if the sum of weights of fulfilled sub-triggers amount to the specified sum | weighted\_calc\_true\_if = { amount = 10 5 = { <trigger> } 15 = { <trigger> } 7 = { <trigger> } } |  | none |  |\
| years\_from\_game\_start | How many years it has been since the start of the game | years\_from\_game\_start > 5 | <, <=, =, !=, >, >= | none |  |\
| any\_side\_commander | Iterate through all commanders (the commanders of every army on the side, not just the one leading the battle) | any\_side\_commander = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | combat side | character |\
| any\_side\_knight | Iterate through all knights | any\_side\_knight = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | combat side | character |\
| has\_maa\_of\_type | Does this combat side have at least one regiment of men at arms of the given type? | has\_maa\_of\_type = onager |  | combat side |  |\
| is\_combat\_side\_attacker | Was the combat side the attacker? |  | yes/no | combat side |  |\
| is\_combat\_side\_pursuing | Is this side the winner of the combat? |  | yes/no | combat side |  |\
| is\_combat\_side\_retreating | Is this side defeated in the combat? |  | yes/no | combat side |  |\
| side\_soldiers | How many soldiers does this side have still fighting? |  | <, <=, =, !=, >, >= | combat side |  |\
| side\_strength | How strong is this side (based on soldiers still fighting)? Scaled down by a factor of 1000 so it doesn't get too large to do math on |  | <, <=, =, !=, >, >= | combat side |  |\
| any\_pledged\_attacker | Iterate through all pledged attackers within a great holy war | any\_pledged\_attacker = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | great holy war | character |\
| any\_pledged\_defender | Iterate through all pledged defenders within a great holy war | any\_pledged\_defender = { <count=num/all> / <percent=fixed\_point> <triggers> } |  | great holy war | character |\
| days\_until\_ghw\_launch | How many days is it until the given GHW launches? |  | <, <=, =, !=, >, >= | great holy war |  |\
| ghw\_attackers\_strength | What is the max (if all levies were fully reinforced) military strength of the pledged attackers in the given hreat holy war? |  | <, <=, =, !=, >, >= | great holy war |  |\
| ghw\_defenders\_strength | What is the max (if all levies were fully reinforced) military strength of the pledged defenders in the given great holy war? |  | <, <=, =, !=, >, >= | great holy war |  |\
| has\_forced\_defender | Is the target character forced to be a defender in the given great holy war? |  | character scope | great holy war | character |\
| has\_pledged\_attacker | Is the target character pledged as an attacker in the given great holy war? |  | character scope | great holy war | character |\
| has\_pledged\_defender | Is the target character pledged as a defender in the given great holy war? |  | character scope | great holy war | character |\
| is\_directed\_ghw | Is the scoped GHW a directed GHW? |  | yes/no | great holy war |  |\
| ghw\_war\_chest\_gold | How much gold is in the great holy war's war chest? |  | <, <=, =, !=, >, >= | great holy war |  |\
| ghw\_war\_chest\_piety | How much piety is in the great holy war's war chest? |  | <, <=, =, !=, >, >= | great holy war |  |\
| ghw\_war\_chest\_prestige | How much prestige is in the great holy war's war chest? |  | <, <=, =, !=, >, >= | great holy war |  | = | (unknown) |\
\
**[Modding](https://ck3.paradoxwikis.com/Modding "Modding")**\
\
|     |     |\
| --- | --- |\
| Documentation | [Scripting](https://ck3.paradoxwikis.com/Scripting "Scripting") • [Scopes](https://ck3.paradoxwikis.com/Scopes "Scopes") • [Effects](https://ck3.paradoxwikis.com/Effects "Effects") • [Triggers](https://ck3.paradoxwikis.com/Triggers "Triggers") • [Variables](https://ck3.paradoxwikis.com/Variables "Variables") • [Modifiers](https://ck3.paradoxwikis.com/Modifier_list "Modifier list") |\
\
|     |     |\
| --- | --- |\
| Scripting | [AI](https://ck3.paradoxwikis.com/AI_modding "AI modding") • [Bookmarks](https://ck3.paradoxwikis.com/Bookmarks_modding "Bookmarks modding") • [Characters](https://ck3.paradoxwikis.com/Characters_modding "Characters modding") • [Commands](https://ck3.paradoxwikis.com/Commands "Commands") • [Council](https://ck3.paradoxwikis.com/Council_modding "Council modding") • [Culture](https://ck3.paradoxwikis.com/Culture_modding "Culture modding") • [Decisions](https://ck3.paradoxwikis.com/Decisions_modding "Decisions modding") • [Dynasties](https://ck3.paradoxwikis.com/Dynasties_modding "Dynasties modding") • [Events](https://ck3.paradoxwikis.com/Event_modding "Event modding") • [Governments](https://ck3.paradoxwikis.com/Governments_modding "Governments modding") • [History](https://ck3.paradoxwikis.com/History_modding "History modding") • [Holdings](https://ck3.paradoxwikis.com/Holdings_modding "Holdings modding") • [Lifestyles](https://ck3.paradoxwikis.com/Lifestyles_modding "Lifestyles modding") • [Regiments](https://ck3.paradoxwikis.com/Regiments_modding "Regiments modding") • [Religions](https://ck3.paradoxwikis.com/Religions_modding "Religions modding") • [Script Values](https://ck3.paradoxwikis.com/Script_values "Script values") • [Story cycles](https://ck3.paradoxwikis.com/Story_cycles_modding "Story cycles modding") • [Struggles](https://ck3.paradoxwikis.com/Struggle_modding "Struggle modding") • [Titles](https://ck3.paradoxwikis.com/Title_modding "Title modding") • [Traits](https://ck3.paradoxwikis.com/Trait_modding "Trait modding") |\
\
|     |     |\
| --- | --- |\
| Interface | [Interface](https://ck3.paradoxwikis.com/Interface "Interface") • [Data types](https://ck3.paradoxwikis.com/Data_types "Data types") • [Localization](https://ck3.paradoxwikis.com/Localization "Localization") • [Customizable localization](https://ck3.paradoxwikis.com/Customizable_localization "Customizable localization") • [Flavorization](https://ck3.paradoxwikis.com/Flavorization "Flavorization") |\
\
|     |     |\
| --- | --- |\
| Map | [Map](https://ck3.paradoxwikis.com/Map_modding "Map modding") • [Terrain](https://ck3.paradoxwikis.com/Terrain_modding "Terrain modding") |\
\
|     |     |\
| --- | --- |\
| Graphics | [3D models](https://ck3.paradoxwikis.com/3D_models "3D models") • [Exporters](https://ck3.paradoxwikis.com/Exporters "Exporters") • [Coat of arms](https://ck3.paradoxwikis.com/Coat_of_arms_modding "Coat of arms modding") • [Graphical assets](https://ck3.paradoxwikis.com/Graphical_assets "Graphical assets") • [Fonts](https://ck3.paradoxwikis.com/Fonts "Fonts") • [Particles](https://ck3.paradoxwikis.com/index.php?title=Particles&action=edit&redlink=1 "Particles (page does not exist)") • [Shaders](https://ck3.paradoxwikis.com/index.php?title=Shaders&action=edit&redlink=1 "Shaders (page does not exist)") • [Unit models](https://ck3.paradoxwikis.com/index.php?title=Unit_models&action=edit&redlink=1 "Unit models (page does not exist)") |\
\
|     |     |\
| --- | --- |\
| Audio | [Music](https://ck3.paradoxwikis.com/Music_modding "Music modding") • [Sound](https://ck3.paradoxwikis.com/Sound_modding "Sound modding") |\
\
|     |     |\
| --- | --- |\
| Other | [Console commands](https://ck3.paradoxwikis.com/Console_commands "Console commands") • [Checksum](https://ck3.paradoxwikis.com/Checksum "Checksum") • [Mod structure](https://ck3.paradoxwikis.com/Mod_structure "Mod structure") • [Mod compatibility](https://ck3.paradoxwikis.com/Mod_compatibility "Mod compatibility") • [Modding tools](https://ck3.paradoxwikis.com/Modding_tools "Modding tools") • [Troubleshooting](https://ck3.paradoxwikis.com/Mod_troubleshooting "Mod troubleshooting") |\
\
Retrieved from " [https://ck3.paradoxwikis.com/index.php?title=Triggers\_list&oldid=33864](https://ck3.paradoxwikis.com/index.php?title=Triggers_list&oldid=33864)"\
\
[Category](https://ck3.paradoxwikis.com/Special:Categories "Special:Categories"):\
\
- [Modding](https://ck3.paradoxwikis.com/Category:Modding "Category:Modding")