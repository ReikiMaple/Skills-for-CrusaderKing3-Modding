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

# Commands

From CK3 Wiki

[Jump to navigation](https://ck3.paradoxwikis.com/Commands#mw-head) [Jump to search](https://ck3.paradoxwikis.com/Commands#searchInput)

Please help with verifying or updating older sections of this article.

At least some were last verified for [version](https://ck3.paradoxwikis.com/CK3_Wiki:Versioning "CK3 Wiki:Versioning") 1.0.

This article is for the PC version of Crusader Kings 3 only.

**Commands** or **effects** are used in [scripting](https://ck3.paradoxwikis.com/Scripting "Scripting") to alter the target that was selected with [scopes](https://ck3.paradoxwikis.com/Scopes "Scopes") and [conditions](https://ck3.paradoxwikis.com/Conditions "Conditions").

They appear in:

- command blocks (the _immediate_ and _option_ sections of [events](https://ck3.paradoxwikis.com/Events "Events"), or similar: effect, creation\_effect, gain\_effect, success, ...)
- [scripted effects](https://ck3.paradoxwikis.com/Scripted_effect "Scripted effect"), which can be used to group commands into re-usable macro.

(Scripting) commands are different from [console commands](https://ck3.paradoxwikis.com/Console_commands "Console commands"), though some console commands have a scripting equivalent.

Available commands depend on the current [scope](https://ck3.paradoxwikis.com/Scope "Scope") type.

## List of Commands\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Commands&veaction=edit&section=1 "Edit section: List of Commands") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Commands&action=edit&section=1 "Edit section: List of Commands")\]

| Command | Used in vanilla | Used from scope | Value type | Description | Example | Category |
| --- | --- | --- | --- | --- | --- | --- |
| add\_dynasty\_modifier |  | dynasty |  | Adds a modifier to a dynasty. | add\_dynasty\_modifier = name<br>add\_dynasty\_modifier = { modifier = name days/weeks/months/years = int } | Modifiers |
| add\_dynasty\_perk |  | dynasty | key | Adds dynasty perk. | add\_dynasty\_perk = key | Lifestyles |
| dynasty\_prestige \[amount\] |  | dynasty | int | Adds \[amount\] dynasty prestige. |  | Dynasty |
| add\_dynasty\_prestige\_level |  | dynasty |  | Adds dynasty prestige levels. |  | Dynasty |
| remove\_all\_dynasty\_modifier\_instances |  | dynasty | modifier | Remove all instances of a modifier from a dynasty. | remove\_all\_dynasty\_modifier\_instances = name | Modifiers |
| remove\_dynasty\_modifier |  | dynasty | modifier | Remove a modifier from a dynasty. | remove\_dynasty\_modifier = name | Modifiers |
| add\_house\_modifier |  | dynasty/house | modifier | Add a modifier to a house. | add\_house\_modifier = name | Modifiers |
| remove\_all\_house\_modifier\_instances |  | dynasty/house | modifier | Remove all instances of a modifier from a house. | remove\_all\_house\_modifier\_instances = name | Modifiers |
| remove\_house\_modifier |  | dynasty/house | modifier | Remove a modifier from a house. | remove\_house\_modifier = name | Modifiers |
| add\_scheme\_modifier |  | scheme | modifier for "type" and int for "days" | Adds the specified scheme modifier. | add\_scheme\_modifier = { type = X days = Y }<br>(Days are optional, the modifier will expire in Y days if specified) | Modifiers |
| add\_scheme\_progress |  | scheme | int | Add progress to the scope scheme. (Progress is in 0.0 - 100.0 range) | add\_scheme\_progress = X | Schemes |
| end\_scheme |  | scheme | bool | Ends a specific scheme and removes it without any other effect. | end\_scheme = yes | Schemes |
| expose\_scheme |  | scheme |  | Exposes the scheme to the defender |  | Schemes |
| expose\_scheme\_agent |  | scheme | character | Exposes the target character as an agent of the current scheme. |  | Schemes |
| remove\_scheme\_modifier |  | scheme | modifier | Removes the specified scheme modifier. |  | Modifiers |
| scheme\_freeze\_days |  | scheme | int | freezes the scheme for X days (0 unfreezes the scheme) | scheme\_freeze\_days = X | Schemes |
| add\_county\_modifier |  | landed title | modifier/int | Add a modifier to a county. | add\_county\_modifier = name<br>add\_county\_modifier = { modifier = name days/weeks/months/years = int } | Modifiers |
| change\_county\_control |  | landed title | int | Changes the county control of a title. If the title has higher tier than county, the effect will propagate down to all counties below it. |  | Control |
| change\_de\_jure\_drift\_progress |  | landed title | title/int | Change the progress of de jure drift of a title. | <drifting\_title> = { change\_de\_jure\_drift\_progress = { target = <drift\_target\_title> value = <progress\_change\_value> } } | Title |
| change\_development\_level |  | landed title | int | Changes the development level of a title. If the title has higher tier than county, the effect will propagate down to all counties below it. |  | Title |
| change\_development\_progress |  | landed title | int | Changes the development progress of a title. If the title has higher tier than county, the effect will propagate down to all counties below it. |  | Development |
| change\_development\_progress\_with\_overflow |  | landed title | int | Changes the development progress of a title. If the title has higher tier than county, the effect will propagate down to all counties below it. Will overflow, so adding +100 to a county with 50 progress left will increase the level by 1 and result in 50 progress towards the next level. |  | Development |
| clear\_title\_laws |  | landed title | bool | Remove all title laws from the scoped title. DOES NOT apply law removal costs and effects. | clear\_title\_laws = yes | Laws |
| clear\_title\_laws\_effects |  | landed title | bool | Remove all title laws from the scoped title. DOES apply law removal costs and effects. | clear\_title\_laws\_effects = yes | Laws |
| copy\_title\_history |  | landed title | title | Copy title history from another title. | copy\_title\_history = source\_title | Titles |
| remove\_all\_county\_modifier\_instances |  | landed title | modifier | Remove all instances of a modifier from a county. | remove\_all\_county\_modifier\_instances = name | Modifiers |
| remove\_county\_modifier |  | landed title | modifier | Remove a modifier from a county. | remove\_county\_modifier = name | Modifiers |
| reset\_title\_name |  | landed title | bool | Sets the name and adjective of the scoped title back to being based on its key. Won't cause the prefix to change. | reset\_title\_name = yes | Title |
| reset\_title\_prefix |  | landed title | bool | Sets the prefix of the scoped title back to being based on its key. Won't cause its adjective or name to change. | reset\_title\_prefix = yes | Title |
| revoke\_lease |  | landed title | bool | Revoke the lease of the scoped title. | revoke\_lease = yes | Title |
| set\_always\_follows\_primary\_heir |  | landed title | bool | Sets if the title should always go to the primary heir in partition succession. | set\_always\_follows\_primary\_heir = yes | Title |
| set\_capital\_county |  | landed title | title | Sets the capital county of the title to the target county. | set\_capital\_county = <some county title> | Title |
| set\_color\_from\_title |  | landed title | title | Sets the color of the title to the same as the target title (shifted very slightly to not be identical). | set\_color\_from\_title = <some title> | Title |
| set\_county\_culture |  | landed title | culture/title | Sets the culture of a county. | set\_county\_culture = english/root.character\_culture | Title |
| set\_county\_faith |  | landed title | faith | Changes what faith a county has. |  | Title |
| set\_de\_jure\_liege\_title |  | landed title | title | Set a new DeJure liege title. | set\_de\_jure\_liege\_title = new\_de\_jure\_liege | Title |
| set\_definitive\_form |  | landed title | bool | Sets if the title should use a definitive form name (no 'Kingdom of'). | set\_definitive\_form = yes | Title |
| set\_delete\_on\_destroy |  | landed title | bool | Sets if the title should be deleted from the gamestate completely when it is destroyed. | set\_delete\_on\_destroy = yes | Title |
| set\_destroy\_if\_invalid\_heir |  | landed title | bool | Sets if the title should be destroyed on succession if there's no heir matching its restrictions. | set\_destroy\_if\_invalid\_heir = yes | Title |
| set\_destroy\_on\_succession |  | landed title | bool | Sets if the title should be destroyed on succession. | set\_destroy\_on\_succession = yes | Title |
| set\_landless\_title |  | landed title | bool | Sets if the title is landless (can be held by rulers with no land) | set\_landless\_title = yes | Title |
| set\_no\_automatic\_claims |  | landed title | bool | Sets if the title should disallow automatic claims (meaning claims will only be added by script, and by pressed claims being inherited). | set\_no\_automatic\_claims = yes | Title |
| set\_title\_name |  | landed title | key | sets the name (localization key) of the scoped title. The adjective will be constructed by adding '\_adj' to the localisation key. Won't cause the prefix to change. | set\_title\_name = TEST\_NAME\_PLEASE\_IGNORE | Title |
| set\_title\_prefix |  | landed title | key | sets the prefix of the scoped title. Won't cause its name or adjective to change. | set\_title\_prefix = PREFIX\_THE | Title |
| title\_create\_faction |  | landed title | faction<br>character/title | The scoped landed title creates a faction of the specified type against the specified target. | title\_create\_faction = { type = X target = Y } | Factions |
| title\_join\_faction |  | landed title | faction | The landed title in the scope joins the assigned faction. |  | Factions |
| title\_leave\_faction |  | landed title | faction | The title in the scope leaves the assigned faction |  | Factions |
| end\_story |  | story cycle |  | Ends a story and executes it's on\_end effect, the story can no longer be accessed after this. |  | Stories |
| make\_story\_owner |  | story cycle | character | Makes the character the new owner of the story. | make\_story\_owner = character\_target | Stories |
| add\_innovation |  | culture | innovation | Add innovation to a culture. |  | Innovations |
| add\_random\_innovation |  | culture | innovation/bool | Add random available innovation | <culture> = { add\_random\_innovation = culture\_group\_military/culture\_group\_civic/culture\_group\_regional/yes } | Innovations |
| get\_all\_innovations\_from |  | culture | culture | Discover all innovations from the target culture. | get\_all\_innovations\_from = <culture> | Innovations |
| get\_random\_innovation\_from |  | culture |  | Get random available innovation from another culture. |  | Innovations |
| add\_character\_flag |  | character | flag | Adds a character flag. | add\_character\_flag = X<br>add\_character\_flag = { flag = X days/weeks/years = Y } X is the name of the flag and Y is a value or value interval "{ min max }". | Flags |
| add\_character\_modifier |  | character | modifier/int | Add a modifier to a character. | add\_character\_modifier = name<br>add\_character\_modifier = { modifier = name days/weeks/months/years = int } | Modifiers |
| add\_courtier |  | character | character | Add the target character to the scope character's court.(It doesn't work) |  | Characters |
| add\_diplomacy\_lifestyle\_perk\_points |  | character | int | Adds lifestyle per points to the given character. |  | Lifestyles |
| add\_diplomacy\_lifestyle\_xp |  | character | int | Adds lifestyle XP to the given character. |  | Lifestyles |
| add\_dread |  | character | int | Adds (or removes) dread to a character. |  | Characters |
| add\_gold |  | character |  | Adds gold to a character. |  | Characters |
| add\_hook |  | character | hook/character/secret/int | Adds a hook on a character. Does send a toast to the player if it's involved. | add\_hook = { type = X, target = Y, secret = Z, days/months/years = W }<br>days/months/years optional (taken from hook type otherwise) and can be a value or an interval, secret required for hook types that require it. | Hooks and Secrets |
| add\_hook\_no\_toast |  | character | hook/character/secret/int | Adds a hook on a character. Does NOT send a toast to the player. | add\_hook = { type = X, target = Y, secret = Z, days/months/years = W }<br>days/months/years optional (taken from hook type otherwise) and can be a value or an interval, secret required for hook types that require it. | Hooks and Secrets |
| add\_intrigue\_lifestyle\_perk\_points |  | character | int | Adds lifestyle per points to the given character. |  | Lifestyles |
| add\_intrigue\_lifestyle\_xp |  | character | int | Adds lifestyle XP to the given character. |  | Lifestyles |
| add\_joined\_faction\_discontent |  | character | int | Adds (or subtracts) discontent to the factions the scope character is in. | add\_joined\_faction\_discontent = X | Factions |
| add\_knows\_of\_killer |  | character | character | Adds the right hand side character as knowing of the killer of the scoped object. | dead\_person = { add\_knows\_of\_killer = root } | Characters |
| add\_learning\_lifestyle\_perk\_points |  | character | int | Adds lifestyle per points to the given character. |  | Lifestyles |
| add\_learning\_lifestyle\_xp |  | character | int | Adds lifestyle XP to the given character |  | Lifestyles |
| add\_martial\_lifestyle\_perk\_points |  | character | int | Adds lifestyle per points to the given character. |  | Lifestyles |
| add\_martial\_lifestyle\_xp |  | character | int | Adds lifestyle XP to the given character. |  | Lifestyles |
| add\_opinion |  | character | modifier/int/character | Adds a temporary opinion modifier. | add\_opinion = { modifier = X days/months/years = Y target = Z } | Characters |
| add\_perk |  |  | character | Adds the perk for this character |  | Lifestyles |
| add\_piety |  | character |  | Gives (or takes) piety to a character. |  | Characters |
| add\_piety\_experience |  | character |  | Gives (or takes) piety experience to a character. |  | Characters |
| add\_piety\_level |  | character |  | Increases (or decreases) the piety level of a character. |  | Characters |
| add\_pressed\_claim |  | character | landed title | Gives a pressed claim to a character. |  | Title |
| add\_prestige |  | character |  | Gives (or takes) prestige to a character. |  | Characters |
| add\_prestige\_experience |  | character |  | Gives (or takes) prestige experience to a character. |  | Characters |
| add\_prestige\_level |  | character |  | Increases (or decreases) the prestige level of a character. |  | Characters |
| add\_realm\_law |  | character |  | Adds the given law to the scoped character. |  | Laws |
| add\_realm\_law\_skip\_effects |  | character |  | Adds the given law to the scoped character. Skips the cost and the pass effect, and the revoke effects of the current law. |  | Laws |
| add\_relation\_flag |  | character |  | Adds a flag to an existing relation. | add\_relation\_flag = { relation = scripted\_relation flag = flag\_name (declared in the relation's script) target = other\_character } | Flags |
| add\_scheme\_cooldown |  | character | character/scheme/int | Sets a scheme cooldown for the scoped character. | <scoped\_character> = { target=target\_character type=scheme\_type days/weeks/months/years = duration } | Hooks and Schemes |
| add\_secret |  | character | secret/character | Adds a secret.<br>Note that if you create a Secret in the immediate effect, the tooltips for other effects run in that Secret's scope (such as reveal\_to) are likely to be displayed incorrectly, or not to be displayed at all. This is due to the game generating the tooltip before it actually has a Secret that exists to work off of. Test rigorously and use custom tooltips if necessary. Creating a Secret in the immediate and then running effects on it in an event option should produce perfectly normal tooltips. | add\_secret = { type = X target = Y } | Hooks and Secrets |
| add\_stewardship\_lifestyle\_perk\_points |  | character | int | Adds lifestyle per points to the given character. |  | Lifestyles |
| add\_stewardship\_lifestyle\_xp |  | character | int | Adds lifestyle XP to the given character. |  | Lifestyles |
| add\_stress |  | character | int | Increases (or decreases) stress of a character. |  | Characters |
| add\_targeting\_factions\_discontent |  | character | int | Adds (or subtracts) discontent to all the factions that are targeting the scope character. | add\_targeting\_factions\_discontent = X | Factions |
| add\_to\_scheme |  | character | cheme | Adds a character as an agent to the scheme. |  | Hooks and Schemes |
| add\_trait |  | character |  | Adds a trait to a character (the trait will not be added and no tooltip will be shown if the character isn't eligible for the trait, i.e. when already having the trait, having an opposing trait, not fulfilling the trait's is\_potential trigger or being outside of the trait's range). |  | Characters |
| add\_trait\_force\_tooltip |  | character |  | Adds a trait to a character (if the add\_trait effect would not add the trait - i.e. when already having the trait, having an opposing trait, not fulfilling the trait's is\_potential trigger or being outside of the trait's range - a tooltip will be shown but the trait will not be added). |  | Characters |
| add\_truce\_both\_ways |  | character | character/string/bool/war result | Sets the both-way truce against the specified character.<br>'character' specifies the target character<br>'override' says whether it should replace the previous truce even if shorter<br>'years / months / days' sets the duration of the truce<br>'result' specifies the result from the scope character's point of view ('white\_peace' by default)<br>'casus\_belli' sets the casus belli scope that caused the truce, mutually exclusive with 'name'<br>'name' sets a custom description. Dynamic description with the current scope<br>'war' sets the war that caused the truce, mutually exclusive with 'casus\_belli' | add\_truce\_both\_ways = { character = X years/months/days = Y override = yes/no result = victory/defeat/white\_peace casus\_belli/war = Z } | Characters |
| add\_truce\_one\_way |  | character | character/string/bool/war result | Sets the truce against the specified character.<br>'character' specifies the target character<br>'override' says whether it should replace the previous truce even if shorter<br>'years / months / days' sets the duration of the truce<br>'result' specifies the result from the scope character's point of view ('white\_peace' by default)<br>'casus\_belli' sets the casus belli scope that caused the truce, mutually exclusive with 'name'<br>'name' sets a custom description. Dynamic description with the current scope<br>'war' sets the war that caused the truce, mutually exclusive with 'casus\_belli' | add\_truce\_one\_way = { character = X years/months/days = Y override = yes/no result = victory/defeat/white\_peace casus\_belli/war = Z } | Characters |
| add\_tyranny |  | character | int | Adds (or removes) tyranny to (or from) a character. |  | Characters |
| add\_unpressed\_claim |  | character | landed title | Gives an unpressed claim to a character. |  | Titles |
| add\_visiting\_courtier |  | character | character | Add the target character as the scope character's guest.(It doesn't work) |  | Characters |
| allow\_alliance |  | character | character | Allows an alliance with the target character after the alliance has been broken or when no familial relation exists. |  | Characters |
| allow\_in\_scheme |  |  | character | Allow the character to join the scheme as an agent. |  | Hooks and Schemes |
| apply\_ai\_vassal\_obligation\_liege\_most\_desired |  | character |  | Apply the new level for the most desired AI obligation level the liege in the contract wants |  | Laws |
| apply\_ai\_vassal\_obligation\_vassal\_most\_desired |  | character |  | Apply the new level for the most desired AI obligation level the vassal in the contract wants. |  | Laws |
| assign\_council\_task |  | character |  | Assigns the target character to the council task. | assign\_council\_task = { council\_task = council\_task\_scope target = character\_taking\_the\_position fire\_on\_actions = yes/no } | Jobs |
| assign\_councillor\_type |  | character |  | Assigns the target character to the first available council position of the type available. | assign\_councillor\_type = { type = council\_position\_type\_key target = character\_taking\_the\_position fire\_on\_actions = yes/no } | Jobs |
| banish |  | character |  | The character gets banished. |  | Characters |
| becomes\_independent |  | character |  | Becomes and independent ruler. | becomes\_independent = { change = 'previously created title\_and\_vassal\_change' } | Vassalage |
| break\_alliance |  | character | character | Breaks the alliance with the target character. |  | Relations |
| cancel\_truce\_both\_ways |  | character | character | Ends the truce against the specified character, and theirs against the scoped character. | cancel\_truce\_both\_ways = scope:character | Relations |
| cancel\_truce\_one\_way |  | character | character | Ends the truce against the specified character. | cancel\_truce\_one\_way = scope:character | Relations |
| change\_current\_weight |  | character | int | Change the current weight of the scoped character | change\_current\_weight = 20 | Characters |
| change\_first\_name |  | character | key/character | Change the first name of a character. | change\_first\_name = <localization\_key><br>change\_first\_name = scope:name/var:name<br>change\_first\_name = { template\_character = scope:character } | Characters |
| change\_government |  | character | key | Changes the government of a character. |  | Characters |
| change\_liege |  | character |  | Adds a liege change. | change\_liege = { liege = 'Character that should become the new liege' change = 'previously created title\_and\_vassal\_change'} | Vassalage |
| change\_prison\_type |  | character | key | Changes the charater's prison type. Scoped character is the prisoner. Accepts any static modifier (see also improson effect). | change\_prison\_type = house\_arrest | Characters |
| change\_target\_weight |  | character | int | Change the target weight of the scoped character. | change\_target\_weight = 20 | Characters |
| clear\_forced\_vote |  | character | bool | clear\_forced\_vote = yes |  | Characters |
| consume\_banish\_reasons |  | character | character | 'Consume' all banish reasons that the scoped character has on the target character. Until they get a new reason, they cannot banish the target again. |  | Characters |
| consume\_divorce\_reasons |  | character | character | 'Consume' all divorce reason that the scoped character has on the target character. Until they get a new reason, they cannot divorce the target again. |  | Characters |
| consume\_execute\_reasons |  | character | character | 'Consume' all execute reasons that the scoped character has on the target character. Until they get a new reason, they cannot execute the target again. |  | Characters |
| consume\_imprisonment\_reasons |  | character | character | 'Consume' all imprisonment reasons that the scoped character has on the target character. Until they get a new reason, they cannot imprison the target again. |  | Characters |
| consume\_revoke\_title\_reason |  | character | character | 'Consume' 1 revoke title reason that the scoped character has on the target character. |  | Characters |
| copy\_inheritable\_appearance\_from |  | character | character | Copies the inheritable appearance attributes (inheritable genes in the character's DNA string) from the target character to the scoped character. |  | Titles |
| create\_alliance |  | character | character | Create an alliance between the scoped character and the target. The allied through characters determine who gets checked against for if the alliance should persist or not. | create\_alliance = scope<br>create\_alliance = { target = scope allied\_through\_owner = scope allied\_through\_target = scope } | Relations |
| create\_cadet\_branch |  | character | bool | The scope character creates a cadet branch of the house he is in. |  | Characters |
| create\_faction |  | key/character |  | The scoped character creates a faction of the specified type against the specified target. | create\_faction = { type = X target = Y } | Factions |
| create\_story |  | character | key/character | Creates and initializes a story cycle with the current character as owner. | create\_story = story\_type<br>create\_story = { type = story\_type save\_scope\_as/save\_temporary\_scope\_as = scope\_name # optional way to get a reference to the new story } | Stories |
| death |  | character | character/key | Kills a character. Where X is a character and Y is one of the death reason keys. Or death = natural which will pick a natural death reason to kill the character from. | death = { killer = X death\_reason = Y } | Characters |
| depose |  | character | bool | The character gets deposed. |  | Vassalage |
| destroy\_title |  | character | title | Destroys a title. |  | Titles |
| end\_pregnancy |  | character |  | End a pregnancy (It doesn't work) |  | Characters |
| execute\_decision |  | character |  | Execute the specified decision for the scoped character |  | Characters |
| finish\_council\_task |  | character |  | The councillor finish the current assigned task successfully. |  | Jobs |
| fire\_councillor |  | character | character | The scope character fires the target character from the council. |  | Jobs |
| forbid\_from\_scheme |  | character |  | Forbid the scope character from joining the target scheme as an agent (and kick the character out if already in the scheme) |  | Hooks and Schemes |
| force\_add\_to\_scheme |  | character | key/int | Adds a character as an agent to the scheme and forces them to stay. | force\_add\_to\_scheme = { scheme = target\_Scheme days/months/years = duration } | Hooks and Schemes |
| force\_vote\_as |  | character |  | Forces the character to vote the same as the target. | force\_vote\_as = { target = someone days/months/years = x } | Characters |
| get\_title |  | character | title | Gives a title to a character. |  | Titles |
| give\_nickname |  | character | key | Give a nickname to this character. |  | Characters |
| join\_faction |  | character |  | The character in the scope joins the assigned faction. |  | Factions |
| join\_faction\_forced |  | character | key/character/int | The character in the scope is forced to join a faction by a character for a defined time. | join\_faction\_forced = { faction = X forced\_by = Y days/months/years = duration } | Factions |
| join\_faction\_skip\_check |  | character |  | The character in the scope joins the assigned faction skiping the can\_character\_join trigger. |  | Factions |
| leave\_faction |  | character |  | The charcter in the scope leaves the assigned faction. |  | Factions |
| make\_claim\_strong |  | character | title | Makes a claim strong (character adds the claim if not having it already). |  | Titles |
| make\_claim\_weak |  | character | title | Makes a claim weak (character adds the claim if not having it already). |  | Titles |
| make\_concubine |  | character | character | Makes the target character a concubine of the scope character, the target should not be imprisoned. |  | Characters |
| make\_pregnant |  | character | character/int/bool | Makes a character pregnant. | make\_pregnant = { father= 'the real father' number\_of\_children= X known\_bastard=yes/no } | Characters |
| make\_trait\_active |  | character |  | Activates an inactive trait. Tooltip will not be shown if the character cannot have the trait. |  | Characters |
| make\_trait\_active\_force\_tooltip |  | character |  | Activates an inactive trait. Tooltip will be shown even if the character cannot have the trait. |  | Characters |
| make\_trait\_inactive |  | character |  | Makes a current trait of a character inactive. Tooltip will not be shown if the character doesn't have the trait. |  | Characters |
| make\_trait\_inactive\_force\_tooltip |  | character |  | Makes a current trait of a character inactive. Tooltip will be shown even if the character doesn't have the trait. |  | Characters |
| make\_unprunable |  | character |  | The scope character will no longer be prunable after their death. Use with care, as this will make everyone related to them unprunable too. So you should only use this if someone absolutely \*needs\* to stick around several years after their death. | make\_unprunable = yes | Characters |
| marry |  | character | character | Marries the scoped character to the target character. | marry = target | Characters |
| marry\_matrilineal |  | character | character | Marries the scoped character to the target character matrilineally | marry\_matrilineal = target | Characters |
| move\_to\_pool |  | character | bool | The scoped character (courtier or guest) leaves their current court and moves into the pool. | scope:guest = { move\_to\_pool = yes } | Characters |
| move\_to\_pool\_at |  | character | province | The scoped character (courtier/guest/pool character) leaves their current court (if any) and moves into the pool of the specified province | scope:guest = { move\_to\_pool\_at = scope:some\_province } | Characters |
| pay\_long\_term\_gold |  | character | character/int | The scope character pays gold to the target character. (AI budget category long term). | pay\_gold = { target = X gold = Y } | Characters |
| pay\_short\_term\_gold |  | character |  | The scope character pays gold to the target character. (AI budget category short term). | pay\_gold = { target = X gold = Y } | Characters |
| pay\_short\_term\_income |  | character | character/int | The scope character immediately pays gold corresponding to their income to the target character. (AI budget short term). | pay\_income = { target = X days/months/years = Y } | Characters |
| play\_music\_cue |  | character |  | Plays the specified music cue. |  | Music |
| recalculate\_scripted\_relation |  | character |  | Recalculates the effect of a scripted relation. | recalculate\_scripted\_relation = friend | Relations |
| recruit\_courtier |  | character | character | Recruits the target to become a courtier.(It doesn't work) | scope:liege = { recruit\_courtier = scope:new\_courtier } | Characters |
| refund\_all\_perks |  | character | bool | Refunds all perks of the character. | refund\_all\_perks = yes | Lifestyles |
| refund\_perks |  | character | key | Refunds all perks of the RHS lifestyle. | refund\_perks = intrigue\_lifestyle | Lifestyles |
| release\_from\_prison |  | character | bool | Releases the character from the prison. | release\_from\_prison = yes | Characters |
| remove\_all\_character\_modifier\_instances |  | character | modifier | Remove all instances of a modifier from a character | remove\_all\_character\_modifier\_instances = name | Modifiers |
| remove\_character\_flag |  | character | flag | Removes a character flag. |  | Flags |
| remove\_character\_modifier |  | character | modifier | Remove a modifier from a character. | remove\_character\_modifier = name | Modifiers |
| remove\_claim |  | character | landed title | Removes an explicit (not from a living parent/grand parent) claim. |  | Title |
| remove\_concubine |  | character | character | Removes the target character as a concubine of the scope character. |  | Relations |
| remove\_courtier\_or\_guest |  | character | character | Removes the target character (guest or courtier) from the scope character's court. | scope:host = { remove\_courtier\_or\_guest = scope:guest }<br>scope:host = {<br>remove\_courtier\_or\_guest = {<br>character = scope:guest<br>new\_location = scope:some\_province # optionally specify a new location<br>}<br>} | Characters |
| remove\_decision\_cooldown |  | character | key | Remove the cooldown on taking a decision for the scoped character. | remove\_decision\_cooldown = decision\_name | Decisions |
| remove\_hook |  | character | character/hook\_type | Removes a hook on a character. If type is specified, the hook will only be removed if it is of that type. | remove\_hook = { target = X, type = Y } | Hooks and Schemes |
| remove\_interaction\_cooldown |  | character | interaction | Remove the cooldown on using an interaction for the scoped character. | remove\_interaction\_cooldown = interaction\_name | Interactions |
| remove\_interaction\_cooldown\_against |  | character | interaction/character | Remove the cooldown on using an interaction against the target character for the scoped character. | remove\_interaction\_cooldown\_against = { interaction = interaction\_name target = character } | Interactions |
| remove\_long\_term\_gold |  | character |  | Removes gold from a character (AI's long term budget). |  | Characters |
| remove\_nickname |  | character | bool | Removes any nickname from the current character. |  | Characters |
| remove\_opinion |  | character | character/modifier/bool | Removes a temporary opinion modifier. Where X is a character, Y is the opinion modifier, Z tells whether to remove all instances of the modifier or just one. | remove\_opinion = { target = X modifier = Y single = Z (no by default) } | Modifiers |
| remove\_perk |  | character |  | Remove the perk for this character |  | Characters |
| remove\_realm\_law |  | character | law | Removes the given law from the scoped character. This will leave the law group empty, so only do this if you're getting rid of a law group. |  | Laws |
| remove\_relation\_best\_friend |  | character | character | Removes scripted relationship. |  | Relations |
| remove\_relation\_bully |  | character | character | Removes scripted relationship. |  | Relations |
| remove\_relation\_court\_physician |  | character | character | Removes scripted relationship. |  | Relations |
| remove\_relation\_crush |  | character | character | Removes scripted relationship. |  | Relations |
| remove\_relation\_flag |  | flag/character/relation | Removed a flag from an existing relation. |  | remove\_relation\_flag = { flag = flag\_name (declared in scripted\_relation) target = other\_character relation = scripted\_relation } | Flags |
| remove\_relation\_friend |  | character | character | Removes scripted relationship. |  | Relations |
| remove\_relation\_guardian |  | character | character | Removes scripted relationship |  | Relations |
| remove\_relation\_intrigue\_mentor |  | character | character | Removes scripted relationship. |  | Relations |
| remove\_relation\_intrigue\_student |  | character | character | Removes scripted relationship. |  | Relations |
| remove\_relation\_lover |  | character | character | Removes scripted relationship. |  | Relations |
| remove\_relation\_mentor |  | character | character | Removes scripted relationship. |  | Relations |
| remove\_relation\_nemesis |  | character | character | Removes scripted relationship. |  | Relations |
| remove\_relation\_oaf |  | character | character | Removes scripted relationship |  | Relations |
| remove\_relation\_potential\_friend |  | character | character | Removes scripted relationship. |  | Relations |
| remove\_relation\_potential\_lover |  | character | character | Removes scripted relationship. |  | Relations |
| remove\_relation\_potential\_rival |  | character | character | Removes scripted relationship. |  | Relations |
| remove\_relation\_rival |  | character | character | Removes scripted relationship. |  | Relations |
| remove\_relation\_soldier\_friend |  | character | character | Removes scripted relationship. |  | Relations |
| remove\_relation\_soulmate |  | character | character | Removes scripted relationship. |  | Relations |
| remove\_relation\_student |  | character | character | Removes scripted relationship. |  | Relations |
| remove\_relation\_victim |  | character | character | Removes scripted relationship. |  | Relations |
| remove\_relation\_ward |  | character | character | Removes scripted relationship. |  | Relations |
| remove\_scheme\_cooldown\_against |  | character | scheme/character | Remove the cooldown on using a scheme against the target character for the scoped character | remove\_scheme\_cooldown\_against = { scheme = scheme\_name target = character } | Hooks and Schemes |
| remove\_short\_term\_gold |  | character |  | Removes gold from a character (AI's short term budget). |  | Characters |
| remove\_trait |  | character |  | Removes a trait from a character. Tooltip will not be shown if the character doesn't have the trait. |  | Characters |
| remove\_trait\_force\_tooltip |  | character |  | Removes a trait from a character. Tooltip will be shown even if the character doesn't have the trait. |  | Characters |
| reset\_beneficiary |  | character | bool | The target character stops having a beneficiary. | reset\_beneficiary = yes | Holy Wars |
| return\_to\_court |  | character |  | Returns the scope character to the employers court. |  | Characters |
| reverse\_add\_opinion |  | character | modifier/int/character | Adds a temporary reverse opinion modifier. X is a scripted modifier name. Y can be a value or a range "{ A B }" If no timeout are specified, the modifier's scripted default timeout will be used. | reverse\_add\_opinion = { modifier = X days/months/years = Y target = Z } | Modifiers |
| scriptedtests\_recalculate\_character\_modifier |  | character |  | Recalculates the modifier of the scoped character. |  | Modifiers |
| scriptedtests\_recalculate\_succession |  | character |  | Recalculates the line of succession of the scoped character. |  | Succession |
| send\_interface\_message |  | character |  | Sends a message to the player playing the character in the scope and then executes any effects inside.<br>For the message text and tooltip, $EFFECT$ contains the text description of the effects in the past tense and $DESC$ contains the text from the desc field. | send\_interface\_message = {<br>type = message\_type # default: send\_interface\_message<br>title = LOCALIZATION # optional, otherwise takes it from the message type<br>desc = LOCALIZATION # optional, otherwise takes it from the message type<br>tooltip = LOCALIZATION # optional, otherwise takes it from the message type<br>left\_icon = scope:recipient # optional, character or title<br>right\_icon = scope:the\_title # optional, character or title<br>goto = scope:the\_title # optional, character, barony title, province will add a goto button<br>\# optional effects...<br>add\_dread = 5<br>scope:someone = { add\_gold = 5 }<br>} | Notifications |
| send\_interface\_toast |  | character |  | Sends a message to the player playing the character in the scope and then executes any effects inside.<br>For the message text and tooltip, $EFFECT$ contains the text description of the effects in the past tense.<br>And $DESC$ contains the text from the desc field. | send\_interface\_toast = {<br>type = message\_type # default: send\_interface\_toast<br>title = LOCALIZATION # optional, otherwise takes it from the message type<br>desc = LOCALIZATION # optional, otherwise takes it from the message type<br>left\_icon = scope:recipient # optional, character or title<br>right\_icon = scope<br>goto = scope:the\_title # optional, character, barony title, province will add a goto button<br>\# optional effects...<br>add\_dread = 5<br>scope:someone = { add\_gold = 5 }<br>} | Notifications |
| set\_absolute\_country\_control |  | character |  | Sets if this character has absolute country control. |  | Control |
| unlock\_character\_movement |  |  | bool/character |  |  | Characters |
| set\_beneficiary |  | character | character | The target character becomes the beneficiary of the scoped character. | set\_beneficiary = some character | Holy Wars |
| set\_character\_faith |  | character | faith | Changes what faith a character has executing the effects for it. For history setup use 'set\_character\_faith\_history' instead. |  | Characters |
| set\_character\_faith\_history |  | character | faith | Changes what faith a character has NOT executing the effects for it. USE ONLY IN HISOTRY SETUP! |  | Characters |
| set\_character\_faith\_with\_conversion |  | character | faith | Changes what faith a character has, as if they used the faith-view interaction (minus the piety cost). So vassals who'd accept will get converted, as will capitals |  | Characters |
| set\_child\_of\_concubine\_on\_pregnancy |  | character |  | Sets the child to be (or not be) a child of a concubine during pregnancy |  | Characters |
| set\_council\_task |  | character | key/character | Sets the task of the scope councillor | set\_council\_task = { task\_type = council\_position\_type\_key target = for\_targeted\_tasks } | Jobs |
| set\_culture |  | character | culture | Set the culture for this character |  | Characters |
| set\_culture\_same\_as |  | character | character | Sets the culture of the character to be the same as the culture of the target. |  | Characters |
| set\_death\_reason |  | character |  | Sets the death reason and the killer of a dead character. | set\_death\_reason = { killer = X death\_reason = Y }, both parameters are optional | Characters |
| set\_default\_education |  |  | character | Sets the default education focus for this character. |  | Lifestyles |
| set\_designated\_heir |  | character | character | Sets the given character as designated heir. |  | Succession |
| set\_employer |  | character | character | Add the scope character to the target character's court. |  | Characters |
| set\_father |  | character | character | Sets the father of a character. |  | Characters |
| set\_focus |  | character |  | Set the focus for this character |  | Lifestyles |
| set\_house |  | character | dynasty house | Sets the dynasty house of the character. |  | Characters |
| set\_immortal\_age |  | character | int | Changes what age the character became immortal at. Only works if already immortal. | set\_immortal\_age = 20 | Characters |
| set\_killer\_public |  | character |  | Sets the scoped character's killer as being publicly known | set\_killer\_public = bool | Hooks and Schemes |
| set\_known\_bastard\_on\_pregnancy |  | character |  | Sets the child to a known or unknown bastard during pregnancy. |  | Characters |
| set\_num\_pregnancy\_children |  | character | int | Set the number of children |  | Characters |
| set\_override\_designated\_winner |  | character | bool | The scoped character will put their beneficiary on the throne if they're the #1 participant if this is called with 'yes'. Call with 'no' to turn it off again. | set\_override\_designate\_winner = yes | Holy Wars |
| set\_player\_character |  | character | character | The scope character's player will now play as the target character. Scope must be player-controlled. Target cannot be player-controlled. |  | Characters |
| set\_pregnancy\_assumed\_father |  | character | character | Set the assumed father of the pregnancy. |  | Characters |
| set\_primary\_spouse |  | character | character | Set the primary spouse of a character. | set\_primary\_spouse = scope | Characters |
| set\_primary\_title\_to |  | character | landed title | Sets the primary title for a character. | set\_primary\_title\_to = <title> | Titles |
| set\_real\_father |  | character | character | Changes the real father of the character scope. |  | Characters |
| set\_realm\_capital |  | character | landed title | Set a new realm capital | character = { set\_realm\_capital = new\_title } | Realm |
| set\_relation\_best\_friend |  | character | character | Sets scripted relationship. |  | Relations |
| set\_relation\_bully |  | character | character | Sets scripted relationship. |  | Relations |
| set\_relation\_court\_physician |  | character | character | Sets scripted relationship. |  | Relations |
| set\_relation\_crush |  | character | character | Sets scripted relationship. |  | Relations |
| set\_relation\_friend |  | character | character | Sets scripted relationship. |  | Relations |
| set\_relation\_guardian |  | character | character | Sets scripted relationship. |  | Relations |
| set\_relation\_intrigue\_mentor |  | character | character | Sets scripted relationship. |  | Relations |
| set\_relation\_intrigue\_student |  | character | character | Sets scripted relationship. |  | Relations |
| set\_relation\_lover |  | character | character | Sets scripted relationship. |  | Relations |
| set\_relation\_mentor |  | character | character | Sets scripted relationship. |  | Relations |
| set\_relation\_nemesis |  | character | character | Sets scripted relationship. |  | Relations |
| set\_relation\_oaf |  | character | character | Sets scripted relationship. |  | Relations |
| set\_relation\_potential\_friend |  | character | character | Sets scripted relationship. |  | Relations |
| set\_relation\_potential\_lover |  | character | character | Sets scripted relationship. |  | Relations |
| set\_relation\_potential\_rival |  | character | character | Sets scripted relationship. |  | Relations |
| set\_relation\_rival |  | character | character | Sets scripted relationship. |  | Relations |
| set\_relation\_soldier\_friend |  | character | character | Sets scripted relationship. |  | Relations |
| set\_relation\_soulmate |  | character | character | Sets scripted relationship. |  | Relations |
| set\_relation\_student |  | character | character | Sets scripted relationship. |  | Relations |
| set\_relation\_victim |  | character | character | Sets scripted relationship. |  | Relations |
| set\_relation\_ward |  | character | character | Sets scripted relationship. |  | Relations |
| set\_sexuality |  | character |  | Sets the sexuality of the character |  | Characters |
| set\_to\_lowborn |  | character |  | Set the character to lowborn. |  | Characters |
| set\_vassal\_contract\_modification\_blocked |  | character |  | Blocks the vassal contract from being modified with regards to being checked by 'vassal\_contract\_is\_blocked\_from\_modification' |  | Vassalage |
| spawn\_army |  | character |  | Spawns an army for this character. If the character is not at war, the regiments will be created, but the army will not be spawned. | spawn\_army = {<br>levies = int/script value # optional, number of men<br>men\_at\_arms = { # optional, multiple can be specified. Need either levies or MAA<br>type = key<br>men/stacks = int/script value<br>}<br>location = province<br>origin = province # optional, location used if not set. This is used for where to base bonuses and the like on<br>war = war # optional. If set, the stack will disband after the war ends<br>inheritable = yes/no # Default: yes<br>uses\_supply = yes/no # Default: yes<br>army = army # optional. If set, the stack will merge into this army<br>save\_scope\_as/save\_temporary\_scope\_as = new\_army # optional way to get a reference to the new army. Note this might not be set if the army wasn't spawned (e.g. if the character is not at war)<br>name = description # gives the troops a specific name that shows up in interfaces<br>} | Armies |
| start\_default\_task |  | character |  | Force the Councillor to revert to the default task. Any relevant percentage progress will be lost (even if the councillor was performing the default task already). |  | Jobs |
| start\_scheme |  | character |  |  | starts a scheme = { type = X target = Y } | Hooks and Schemes |
| start\_war |  | character |  | Starts a war. X is a casus belli type, Y is the target character, Z i the (optional) claimant, W1, W2.... are targeted titles. | start\_war = { casus\_belli/cb = X target = Y claimant = Z target\_title = W1 target\_title = W2 ... } | Wars |
| stress\_impact |  | character |  | Stress impact according to specified traits (trait = value), use base = value for a base value that's always added. | stress\_impact = { sadistic = medium\_stress\_impact\_loss }<br>stress\_impact = { compassionate = medium\_stress\_impact\_gain } | Characters |
| use\_hook |  | character | character | Uses a hook a character has (removes if weak, puts on cooldown if strong). | use\_hook = some\_character | Hooks and Schemes |
| vassal\_contract\_decrease\_obligation\_level |  | character |  | Decrease the obligation level of the scoped character's vassal contract. |  | Vassalage |
| vassal\_contract\_increase\_obligation\_level |  | character |  | Increase the obligation level of the scoped character's vassal contract. |  | Vassalage |
| vassal\_contract\_set\_obligation\_level |  | character |  | Change the obligation level of the scoped character's vassal contract. | vassal\_contract\_set\_obligation\_level = { type = name level = 1 } # index to obligation level<br>vassal\_contract\_set\_obligation\_level = { type = name level = feudal\_obligation\_low } | Vassalage |
| visit\_court\_of |  | character | character | Add the scope character as the target character's guest. |  | Characters |
| add\_faction\_discontent |  | faction |  | Adds (or subtracts) discontent to the scope faction. | add\_faction\_discontent = X | Factions |
| destroy\_faction |  | faction |  | The scope faction is destroyed. | destroy\_faction = yes | Factions |
| faction\_remove\_war |  | faction |  | Removes the war currently associated with the faction. | faction\_remove\_war = yes | Factions |
| faction\_start\_war |  | faction |  | The scope faction starts the war agains their target. | faction\_start\_war = {<br>title = \[optional\]<br>} | Factions |
| remove\_special\_character |  | faction |  | Removes the special character for the scope faction |  | Factions |
| remove\_special\_title |  | faction |  | Removes the special character for the scope faction. |  | Factions |
| set\_special\_character |  | faction | character | Sets the special character for the scope faction. |  | Factions |
| set\_special\_title |  | faction | landed title | Sets the special title for the scope faction |  | Factions |
| add\_attacker |  | war | character | Adds the target character to the scope war as an attacker. |  | Wars |
| add\_defender |  | war | character | Adds the target character to the scope war as a defender. |  | Wars |
| end\_war |  | war |  | Ends the war with the specified winner. | end\_war = attacker/defender/white\_peace | Wars |
| remove\_participant |  | war | character | Removes the target character from the scope war. |  | Wars |
| set\_called\_to |  | war | character | Sets the target character as already called to the scope war. |  | Wars |
| set\_casus\_belli |  | war |  | Sets the casus belli of the scope war. |  | Wars |
| activate\_holy\_site |  | faith |  | Activate an inactive holy site. | <faith\_scope> = { activate\_holy\_site = <holy\_site\_name> } | Faiths |
| add\_doctrine |  | faith | doctrines | Add doctrine to faith. | <faith\_scope> = { add\_doctrine = <doctrine\_name> } | Faiths |
| change\_fervor |  | faith | int | Changes the fervor of the faith by the given value. | change\_fervor = script value | Faiths |
| remove\_doctrine |  | faith | doctrines | Remove doctrine from faith. | <faith\_scope> = { remove\_doctrine = <doctrine\_name> } | Faiths |
| remove\_religious\_head\_title |  | faith | bool | Removes the religious head title of the faith. | remove\_religious\_head\_title = yes | Faiths |
| set\_religious\_head\_title |  | faith | landed title | Sets the religious head title of the faith to the given title. | set\_religious\_head\_title = scope | Faiths |
| start\_great\_holy\_war |  | faith |  | Starts a great holy war. | start\_great\_holy\_war = {<br>target\_character = someone<br>target\_title = some<br>titledelay = script value# Number of days until the war should<br>startwar = some war # Optional. Will make this a directed GHW instead of undirected, and tie it to this specific war<br>} | Faiths |
| set\_add\_claim\_on\_loss |  | title/vassal change |  | If set, any title losses will result in claims being added to the previous holder. |  | Titles |
| set\_title\_and\_vassal\_change\_type |  | title/vassal change | conquest, conquest\_holy\_war, conquest\_claim, conquest\_populist, inheritance, abdication, destroyed, created, usurped, granted, revoked, election, independency, returned, leased\_out, lease\_revoked, faction\_demand | Sets the type of change. |  | Titles |
| add\_secret\_participant |  | secret | character | Adds an participant to the secret. |  | Hooks and Schemes |
| disable\_exposure\_by |  | secret | character | Forbids the target character from exposing the secret | disable\_exposure\_by = target\_character | Hooks and Schemes |
| add\_building\_slot |  | title/holding | int | Adds adds number of building slots to holding. |  | Buildings |

**[Modding](https://ck3.paradoxwikis.com/Modding "Modding")**

|     |     |
| --- | --- |
| Documentation | [Scripting](https://ck3.paradoxwikis.com/Scripting "Scripting") • [Scopes](https://ck3.paradoxwikis.com/Scopes "Scopes") • [Effects](https://ck3.paradoxwikis.com/Effects "Effects") • [Triggers](https://ck3.paradoxwikis.com/Triggers "Triggers") • [Variables](https://ck3.paradoxwikis.com/Variables "Variables") • [Modifiers](https://ck3.paradoxwikis.com/Modifier_list "Modifier list") |

|     |     |
| --- | --- |
| Scripting | [AI](https://ck3.paradoxwikis.com/AI_modding "AI modding") • [Bookmarks](https://ck3.paradoxwikis.com/Bookmarks_modding "Bookmarks modding") • [Characters](https://ck3.paradoxwikis.com/Characters_modding "Characters modding") • Commands • [Council](https://ck3.paradoxwikis.com/Council_modding "Council modding") • [Culture](https://ck3.paradoxwikis.com/Culture_modding "Culture modding") • [Decisions](https://ck3.paradoxwikis.com/Decisions_modding "Decisions modding") • [Dynasties](https://ck3.paradoxwikis.com/Dynasties_modding "Dynasties modding") • [Events](https://ck3.paradoxwikis.com/Event_modding "Event modding") • [Governments](https://ck3.paradoxwikis.com/Governments_modding "Governments modding") • [History](https://ck3.paradoxwikis.com/History_modding "History modding") • [Holdings](https://ck3.paradoxwikis.com/Holdings_modding "Holdings modding") • [Lifestyles](https://ck3.paradoxwikis.com/Lifestyles_modding "Lifestyles modding") • [Regiments](https://ck3.paradoxwikis.com/Regiments_modding "Regiments modding") • [Religions](https://ck3.paradoxwikis.com/Religions_modding "Religions modding") • [Script Values](https://ck3.paradoxwikis.com/Script_values "Script values") • [Story cycles](https://ck3.paradoxwikis.com/Story_cycles_modding "Story cycles modding") • [Struggles](https://ck3.paradoxwikis.com/Struggle_modding "Struggle modding") • [Titles](https://ck3.paradoxwikis.com/Title_modding "Title modding") • [Traits](https://ck3.paradoxwikis.com/Trait_modding "Trait modding") |

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

Retrieved from " [https://ck3.paradoxwikis.com/index.php?title=Commands&oldid=25990](https://ck3.paradoxwikis.com/index.php?title=Commands&oldid=25990)"

[Categories](https://ck3.paradoxwikis.com/Special:Categories "Special:Categories"):

- [Potentially outdated](https://ck3.paradoxwikis.com/Category:Potentially_outdated "Category:Potentially outdated")
- [1.0](https://ck3.paradoxwikis.com/Category:1.0 "Category:1.0")
- [Modding](https://ck3.paradoxwikis.com/Category:Modding "Category:Modding")