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

# Localization

From CK3 Wiki

[Jump to navigation](https://ck3.paradoxwikis.com/Localization#mw-head) [Jump to search](https://ck3.paradoxwikis.com/Localization#searchInput)

Please help with verifying or updating older sections of this article.

At least some were last verified for [version](https://ck3.paradoxwikis.com/CK3_Wiki:Versioning "CK3 Wiki:Versioning") 1.4.

This article is for the PC version of Crusader Kings 3 only.

Localization is the text presented to the player in the game in their selected language. It's used everywhere: events, UI, tooltips, etc.

Script uses localization keys, like text\_example, which is then turned to real text in a localization file like this:

`text_example: "Example text"`

Localization files:

- use .yml format
- must use UTF-8 BOM encoding. It is often displayed at the bottom right in text editors. Look also for Select Encoding or Save With Encoding options.
- are saved to `localization/` folder, and the right language subfolder. E.g `localization/english`
- must include `l_<language>` in their name. E.g. `my_locs_l_english.yml` or `my_locs_l_french.yml`
- must start with the same `l_<language>:` on the first line. E.g.


```
l_english:
text_example: "Example text"
```


Note `l_` is a small L, not 1 or capital i. `localization` is also spelled with a z, not s.

Localized text must be surrounded by quotation marks: "". Dialog inside it may also use quotation marks, it won't end the string early.

A line break is done with `\n`, and using two of them will yield you an empty line for paragraph separation. For example, `"Hello\n\nWorld"` would be displayed as:

```
Hello

World
```

`\n` only works in localization files, not when put directly in UI.

If a mod doesn't include localization for other languages, the game will display unlocalized keys for those playing in another language. To prevent this, copy all locs to other language folders, replacing l\_english in both file names and on the first line. Modding discord has a script to do it quickly.

A space before a new loc line is optional and speeds up loading of big files, as discovered by modders through testing.

Most localization keys can be overwritten individually without replacing the whole file, if your file is placed in a folder called "replace".

Both `localization/replace/english` and `localization/english/replace` work, but the first path takes precedence over the other (which may matter if multiple mods try to overwrite the same files).

Localization entries may also look like this:

```
 murder_successful_roll_tt:0 "[target.GetShortUINameNoTooltip] is killed!"
 murder_become_discovered_roll_tt:0 "#N My involvement is discovered#!"
```

The number after the: is optional and it does nothing for modders. Paradox used to use those numbers for their translation teams to indicate new versions of localization. This is now completely deprecated, you do not need to add any numbers.

The part between \[ \] is code that looks up something in the game (in this case a character's name) and puts it in the text. The `#N` and `#!` control how the text is displayed; in this case as something "negative" (bad for the player). See the sections below for more details on those.

Most of the formatting styles can be found in `gui/preload/textformatting.gui`. That's also where you can add your own styles for your mod.

A few more are defined in `Crusader Kings III/jomini/gui/jomini/basetextformatting.gui`.

## Contents

- [1Formatting](https://ck3.paradoxwikis.com/Localization#Formatting)
- [2Re-use other entries](https://ck3.paradoxwikis.com/Localization#Re-use_other_entries)
- [3Data Types](https://ck3.paradoxwikis.com/Localization#Data_Types)
  - [3.1Gender](https://ck3.paradoxwikis.com/Localization#Gender)
  - [3.2Character names](https://ck3.paradoxwikis.com/Localization#Character_names)
  - [3.3Arguments](https://ck3.paradoxwikis.com/Localization#Arguments)
- [4Special Characters](https://ck3.paradoxwikis.com/Localization#Special_Characters)
- [5Linking](https://ck3.paradoxwikis.com/Localization#Linking)
  - [5.1Game Concepts](https://ck3.paradoxwikis.com/Localization#Game_Concepts)
  - [5.2Example Custom Game Concept](https://ck3.paradoxwikis.com/Localization#Example_Custom_Game_Concept)
  - [5.3Traits](https://ck3.paradoxwikis.com/Localization#Traits)
  - [5.4Titles](https://ck3.paradoxwikis.com/Localization#Titles)
- [6Number formatting](https://ck3.paradoxwikis.com/Localization#Number_formatting)
- [7Icons](https://ck3.paradoxwikis.com/Localization#Icons)
- [8Usage of special characters & Line breaks](https://ck3.paradoxwikis.com/Localization#Usage_of_special_characters_&_Line_breaks)
- [9Chinese punctuation](https://ck3.paradoxwikis.com/Localization#Chinese_punctuation)
- [10References](https://ck3.paradoxwikis.com/Localization#References)

## Formatting\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Localization&veaction=edit&section=1 "Edit section: Formatting") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Localization&action=edit&section=1 "Edit section: Formatting")\]

[![](https://ck3.paradoxwikis.com/images/thumb/f/f9/Text_formatting_1.11.png/300px-Text_formatting_1.11.png)](https://ck3.paradoxwikis.com/File:Text_formatting_1.11.png)

[Enlarge](https://ck3.paradoxwikis.com/File:Text_formatting_1.11.png "Enlarge")

Example of all formatting styles in the game

Localization strings can contain formatting directives. Text formatting should begin with a `#` character and end with `#!`.

Make sure to add a space before the text!

```
#<formatting code> <text>#!

Example:
#P Green#!
```

See Special Characters below for more details.

## Re-use other entries\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Localization&veaction=edit&section=2 "Edit section: Re-use other entries") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Localization&action=edit&section=2 "Edit section: Re-use other entries")\]

Insert other localization keys: $<other key>$

Example:

```
 special_contract_march_short:0 "March"
 unlock_march_contract:0 "Unlocks the #high $special_contract_march_short$#! [feudal_contract|E]"
```

This is useful both to avoid duplication, and to make sure that entries stay in sync with each other; for example if you ever change the description of `special_contract_march_short`, the `unlock_march_contract` message will automatically change with it.

The same $ notation is used to refer to special values supplied by the game engine. For example:

```
 tooltip_feudal_elector_anti_vote_ruler_lunatic:1 "I do not trust the judgment of a [GetTrait('lunatic_1').GetName( candidate.Self )] ruler: $VALUE|=+0$"
```

Here `$VALUE$` is a number supplied by the game, and the `|=+0` part controls how that number is shown (see "Rounding numbers" below for details). Special values like this can only be used in localization entries that are shown in specific contexts; in this case, on the elective title voting screen.

## Data Types\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Localization&veaction=edit&section=3 "Edit section: Data Types") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Localization&action=edit&section=3 "Edit section: Data Types")\]

Data types are used to make localization dynamic and change based on certain conditions. Invoking a type will print out a specific string of text.

Data types need to be scoped, usually to a character. Example:

```
[ROOT.Char.GetLadyLord] [ROOT.Char.GetNamePossessiveRegnal] [ROOT.Char.GetFirstNameNicknamed]
```

Use console command `dump_data_types` to print out all data types to your logs folder: Documents\\Paradox Interactive\\Crusader Kings III\\logs\\data\_types.

The logs will show where certain types can be used and what they return: another type, a string, an integer, etc.

The logs will be split into different files. To make it easier to search through them, you can merge them by creating a .bat file with the following code:

`type *.txt > ALL_DATA_TYPES.txt`

Then run the .bat inside the data\_types folder.

Data types can also be looked up in the game with `data_types_explorer` console command. Note that it makes the distinction between promotes and functions, but it's not important when using them. The main difference seems to be that promotes return a scope, like Character or Title (similar to event targets in script) and functions return a value or perform an action (like effects and triggers).

### Gender\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Localization&veaction=edit&section=4 "Edit section: Gender") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Localization&action=edit&section=4 "Edit section: Gender")\]

These functions will show text that vary based on the gender of the character in scope.

| Function |
| --- |
| GetHerHim |
| GetHerHis |
| GetHerHisMy |
| GetHersHis |
| GetHerselfHimself |
| GetLadyLord |
| GetSheHe |
| GetDaughterSon |
| GetDaughterSonPossessive |

### Character names\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Localization&veaction=edit&section=5 "Edit section: Character names") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Localization&action=edit&section=5 "Edit section: Character names")\]

These functions will show some variation of the name of the character. This is not a complete list.

| Function |
| --- |
| GetFirstName |
| GetFirstNameBase |
| GetFirstNameNicknamed |
| GetFirstNameNicknamedNoTooltip |
| GetFirstNameNicknamedNoTooltipRegnal |
| GetFirstNameNicknamedOrMe |
| GetFirstNameNicknamedOrMeNoTooltip |
| GetFirstNameNicknamedOrMeNoTooltipRegnal |
| GetFirstNameNicknamedOrMeRegnal |
| GetFirstNameNicknamedPossessive |
| GetFirstNameNicknamedPossessiveNoTooltip |
| GetFirstNameNicknamedPossessiveNoTooltipRegnal |
| GetFirstNameNicknamedPossessiveOrMy |
| GetFirstNameNicknamedPossessiveOrMyNoTooltip |
| GetFirstNameNicknamedPossessiveOrMyNoTooltipRegnal |
| GetFirstNameNicknamedPossessiveOrMyRegnal |
| GetFirstNameNicknamedPossessiveRegnal |
| GetFirstNameNicknamedRegnal |
| GetFirstNameNoTooltip |
| GetFirstNameNoTooltipRegnal |
| GetFirstNameOrMe |
| GetFirstNameOrMeNoTooltip |
| GetFirstNameOrMeNoTooltipRegnal |
| GetFirstNameOrMeRegnal |
| GetFirstNamePossessive |
| GetFirstNamePossessiveNoTooltip |
| GetFirstNamePossessiveNoTooltipRegnal |
| GetFirstNamePossessiveOrMy |
| GetFirstNamePossessiveOrMyNoTooltip |
| GetFirstNamePossessiveOrMyNoTooltipRegnal |
| GetFirstNamePossessiveOrMyRegnal |
| GetFirstNamePossessiveRegnal |
| GetFirstNameRegnal |
| GetTitledFirstName |
| GetFullName |
| GetFullNameNicknamed |
| GetFullNameNicknamedNoTooltip |
| GetFullNameNicknamedNoTooltipRegnal |
| GetFullNameNicknamedOrMe |
| GetFullNameNicknamedOrMeNoTooltip |
| GetFullNameNicknamedOrMeNoTooltipRegnal |
| GetFullNameNicknamedOrMeRegnal |
| GetFullNameNicknamedPossessive |
| GetFullNameNicknamedPossessiveNoTooltip |
| GetFullNameNicknamedPossessiveNoTooltipRegnal |
| GetFullNameNicknamedPossessiveOrMy |
| GetFullNameNicknamedPossessiveOrMyNoTooltip |
| GetFullNameNicknamedPossessiveOrMyNoTooltipRegnal |
| GetFullNameNicknamedPossessiveOrMyRegnal |
| GetFullNameNicknamedPossessiveRegnal |
| GetFullNameNicknamedRegnal |
| GetFullNameNoTooltip |
| GetFullNameNoTooltipRegnal |
| GetFullNameOrMe |
| GetFullNameOrMeNoTooltip |
| GetFullNameOrMeNoTooltipRegnal |
| GetFullNameOrMeRegnal |
| GetFullNamePossessive |
| GetFullNamePossessiveNoTooltip |
| GetFullNamePossessiveNoTooltipRegnal |
| GetFullNamePossessiveOrMy |
| GetFullNamePossessiveOrMyNoTooltip |
| GetFullNamePossessiveOrMyNoTooltipRegnal |
| GetFullNamePossessiveOrMyRegnal |
| GetFullNamePossessiveRegnal |
| GetFullNameRegnal |
| GetName |
| GetNameNicknamed |
| GetNameNicknamedNoTooltip |
| GetNameNicknamedNoTooltipRegnal |
| GetNameNicknamedOrMe |
| GetNameNicknamedOrMeNoTooltip |
| GetNameNicknamedOrMeNoTooltipRegnal |
| GetNameNicknamedOrMeRegnal |
| GetNameNicknamedPossessive |
| GetNameNicknamedPossessiveNoTooltip |
| GetNameNicknamedPossessiveNoTooltipRegnal |
| GetNameNicknamedPossessiveOrMy |
| GetNameNicknamedPossessiveOrMyNoTooltip |
| GetNameNicknamedPossessiveOrMyNoTooltipRegnal |
| GetNameNicknamedPossessiveOrMyRegnal |
| GetNameNicknamedPossessiveRegnal |
| GetNameNicknamedRegnal |
| GetNameNoTooltip |
| GetNameNoTooltipRegnal |
| GetNameOrMe |
| GetNameOrMeNoTooltip |
| GetNameOrMeNoTooltipRegnal |
| GetNameOrMeRegnal |
| GetNamePossessive |
| GetNamePossessiveNoTooltip |
| GetNamePossessiveNoTooltipRegnal |
| GetNamePossessiveOrMy |
| GetNamePossessiveOrMyNoTooltip |
| GetNamePossessiveOrMyNoTooltipRegnal |
| GetNamePossessiveOrMyRegnal |
| GetNamePossessiveRegnal |
| GetNameRegnal |

### Arguments\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Localization&veaction=edit&section=6 "Edit section: Arguments") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Localization&action=edit&section=6 "Edit section: Arguments")\]

Arguments are used to modify the output of a function. They always go at the end of a function.

| Argument | Description | Example | Without Argument | With Argument |
| --- | --- | --- | --- | --- |
| ```<br>|U<br>``` | Sets first letter to uppercase | ```<br>Tea is ready, my [ROOT.Char.GetLadyLord|U].<br>``` | Tea is ready, my lady. | Tea is ready, my Lady. |
| ```<br>|L<br>``` | Sets first letter to lowecase | ```<br>Tea is ready. [ROOT.Char.GetSheHe|L] said.<br>``` | Tea is ready. He said. | Tea is ready. he said. |

## Special Characters\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Localization&veaction=edit&section=7 "Edit section: Special Characters") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Localization&action=edit&section=7 "Edit section: Special Characters")\]

Some sets of characters perform special functions.

The full list of available formatting styles can be found in `gui/preload/textformatting.gui`. That's also where you can add your own styles for your mod.

You can also combine formatting codes with a `;` (semicolon), like `#high;bold` to get both. However, if you find yourself doing that it may be better to define a new style.

| Characters | Description | Example |
| --- | --- | --- |
| \\n | Line break. Works only in certain cases. |  |
| #P | Formats text green, as "positive" | ```<br>#P A very good thing has happened#!<br>```<br> OR <br>```<br>[GetFullName|P]<br>``` |
| #N | Formats text red, as "negative" | ```<br>#N A rather bad thing has happened#!<br>```<br> OR <br>```<br>[GetFullName|N]<br>``` |
| #help | Text is shown using a help style, with blue gray and italic | ```<br>#help If you do not give either Gold or Soldiers to the war effort, your [head_of_faith|E] will condemn you and you will lose [piety|E].#!<br>``` |
| #I | Text is displayed in an informational style, green and italic | ```<br>#I Click to view your [GetPlayer.GetCouncillorPosition( 'councillor_court_chaplain' ).GetPositionName]#!<br>``` |
| #warning | Text is displayed as a warning, red and italic | ```<br>#warning Only your younger children lacks [guardians|E]#!<br>``` |
| #X | Text is displayed as a warning,same as above | ```<br>#X Choosing a New Appearance will discard ALL previous changes!#!<br>``` |
| #T | Text is displayed as a title, bold and large | ```<br>#T Randomize Dynasty Name#!<br>``` |
| #E | Text is displayed as a game concept, light blue | ```<br>#E Randomize#!<br>``` |
| #S | Formats text bold and italic | ```<br>#S Occupying Counties:#!<br>``` |
| #V | Formats text white | ```<br>#V This text is white #!<br>```<br> OR <br>```<br>[GetFullName|V]<br>``` |
| #EMP | Text is emphasized, italic | ```<br>#EMP Emphasis here #!<br>``` |
| #weak | Text is darker and italic | ```<br>#weak footnote or aside #!<br>``` |
| #bold | Text is displayed in bold | ```<br>You have #bold NOT #! done this<br>``` |
| #italic | Text is displayed in italics | ```<br>You #italic will #! do this<br>``` |
| #indent\_newline:N | (N being a number)<br>How many spaces to put after line breaks | ```<br>#indent_newline:2<br>``` |

## Linking\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Localization&veaction=edit&section=8 "Edit section: Linking") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Localization&action=edit&section=8 "Edit section: Linking")\]

### Game Concepts\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Localization&veaction=edit&section=9 "Edit section: Game Concepts") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Localization&action=edit&section=9 "Edit section: Game Concepts")\]

Localization strings can link to game concepts as follows:

```
[concept_key|E]

# So for example
[faith|E]
```

By default the concept starts with first letter in upper case, you can set the first letter in lower case as follows:

```
[concept_key|El]

# So for example
"The word [faith|El] is now starting by a lower case letter"
```

The expression linking to the game concept can be customized as follows:

```
[Concept('concept_key','Customized expression')|E]

# So for example
"The game concept link [Concept('faith','religion')|E] is now written as religion."
```

### Example Custom Game Concept\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Localization&veaction=edit&section=10 "Edit section: Example Custom Game Concept") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Localization&action=edit&section=10 "Edit section: Example Custom Game Concept")\]

If you want to add custom game concept and show it's description:

```
###
### common\game_concepts\MY_game_concepts.txt
###
my_custom_concept = {
}
```

```
###
### localization\english\MY_l_english.yml
###
l_english:
  game_concept_my_custom_concept:0 "My Name"
  game_concept_my_custom_concept_desc:0 "My Description"
  # example override description for government
  game_concept_government_desc:2 "[my_custom_concept|E]"
```

### Traits\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Localization&veaction=edit&section=11 "Edit section: Traits") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Localization&action=edit&section=11 "Edit section: Traits")\]

Similarly, you can link to a trait with:

```
[GetTrait('trait_name').GetName(GetNullCharacter)]
```

This will cause the trait to have a tooltip which shows the trait information. You can also pass an actual character into the `GetName` function, so that any conditional descriptions display properly. For example, the localization text for adding a trait passes in the character who will receive the trait:

```
# note that the [trait|E] links to the game concept of a trait, as described above, while the [TRAIT.GetName( Character.Self )|LV] links to the actual trait which will be gained
# from localization/english/effects_l_english.yml
ADD_MY_TRAIT:2 "You gain the [trait|E] [TRAIT.GetName( CHARACTER.Self )|LV]"
```

Note that the `|LV`, which will cause the trait to be written as lowercase and in a white font (see the above sections on [Command Arguments](https://ck3.paradoxwikis.com/Localization#Command_Arguments "Localization") and [Special Characters](https://ck3.paradoxwikis.com/Localization#Special_Characters "Localization"), respectively), appears to be idiomatic in the vanilla game files.

### Titles\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Localization&veaction=edit&section=12 "Edit section: Titles") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Localization&action=edit&section=12 "Edit section: Titles")\]

You can also link to a specific title with:

```
[GetTitleByKey('title_name').GetName]
```

This will cause the title to have a tooltip which shows the title information. You can also use `GetNameNoTier` so that only the title's name will appear.

## Number formatting\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Localization&veaction=edit&section=13 "Edit section: Number formatting") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Localization&action=edit&section=13 "Edit section: Number formatting")\]

Numeric values can be formatted in different ways using a number of codes, which can sometimes be combined.

| Character/Code | Description | Code Example | Code Example Output |
| --- | --- | --- | --- |
| Digit (0-9) | Rounds to the given number decimal places, including trailing zeroes if necessary. Note that the value is **always** rounded down. | ```<br>['(CFixedPoint)0.12'|0]<br>``` | 0 |
| ```<br>['(CFixedPoint)0.12'|1]<br>``` | 0.1 |
| ```<br>['(CFixedPoint)0.12'|3]<br>``` | 0.120 |
| = | Always display sign, even if positive, and round to two decimal places<br>Note that this can be combined with the digit, e.g. `=0` will display the sign and round to 0 decimal places | ```<br>['(CFixedPoint)1'|=]<br>``` | +1.00 |
| ```<br>['(CFixedPoint)-1'|=]<br>``` | -1.00 |
| ```<br>['(CFixedPoint)1'|=0]<br>``` | +1 |
| k OR K | Display as thousands | ```<br>['(CFixedPoint)1200'|k]<br>``` | 1.20K |
| + | Colour as positive modifier (colour green if positive, red if negative, white if zero) | ```<br>['(CFixedPoint)1.5'|+]<br>``` | 1.5 |
| ```<br>['(CFixedPoint)0'|+]<br>``` | 0 |
| ```<br>['(CFixedPoint)-1.5'|+]<br>``` | -1.5 |
| - | Colour as negative modifier (colour red if positive, green if negative, white if zero) | ```<br>['(CFixedPoint)1.5'|-]<br>``` | 1.5 |
| ```<br>['(CFixedPoint)0'|-]<br>``` | 0 |
| ```<br>['(CFixedPoint)-1.5'|-]<br>``` | -1.5 |
| % | Display as percentage (multiplies the value by 100 and appends a percentage sign) and round the percentage to two decimal places<br>Note that this can be combined with the digit, e.g. `%0` will display as a percentage rounded to 0 decimal places | ```<br>['(CFixedPoint)0.2'|%]<br>``` | 20.00% |
| ```<br>['(CFixedPoint)0.2'|%0]<br>``` | 20% |
| O | Display as ordinal. Only works on positive integers. | ```<br>['(int32)'1|O]<br>``` | 1st |
| v OR V | Display in white with 2 decimal points | ```<br>[1.5|v]<br>``` | 1.50 |

## Icons\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Localization&veaction=edit&section=14 "Edit section: Icons") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Localization&action=edit&section=14 "Edit section: Icons")\]

[![](https://ck3.paradoxwikis.com/images/5/57/Example_image_for_icons_in_modded_loc.png)](https://ck3.paradoxwikis.com/File:Example_image_for_icons_in_modded_loc.png)

This is the resulting output of the example string besides this image

Icons can be displayed in loc keys by using `@icon_name!` to render them.

```
Careful! @warning_icon!, you are going to drop all your @gold_icon! gold if you keep running like that! @piety_icon_islam! Allah will judge you for that!
```

If you want to try customizing icons, go game/gui/texticons.gui

| Icon Addresses |
| --- |
| Generic Icons | Military Icons | Faith Icons | Terrain Icons |
| warning\_icon | skill\_martial\_icon | unspent\_strong\_hook\_icon | friend\_icon | soldier\_icon | heavy\_cavalry\_icon | pikemen\_icon | catholic\_icon | plains |
| gold\_icon | skill\_stewardship\_icon | crime\_icon | best\_friend\_icon | bombard\_icon | heavy\_infantry\_icon | skirmishers\_icon | orthodox\_icon | forest |
| prestige\_icon | skill\_intrigue\_icon | intimidated\_icon | rival\_icon | bondi\_icon | horse\_archers\_icon | trebuchet\_icon | custom\_faith\_1\_icon (10) | mountains |
| time\_icon | skill\_learning\_icon | terrified\_icon | nemesis\_icon | bowmen\_icon | jomsviking\_pirates\_icon | varangian\_veterans\_icon | virtue\_icon |  |
| cross\_icon | skill\_prowess\_icon | weak\_hook\_icon | lover\_icon | camel\_riders\_icon | light\_cavalry\_icon | vigmen\_icon | sin\_icon |  |
| stress\_icon | stress\_gain\_icon | pending\_court\_events | soulmate\_icon | crossbowmen\_icon | mangonel\_icon | war\_elephants\_icon | fervor\_icon |  |
| dread\_icon | stress\_critical\_icon | realm\_capital\_icon |  | danish\_huskarls\_icon | onager\_icon | advantage\_icon |  |  |
| exposed\_icon | stress\_loss\_icon | alliance\_icon |  | countered\_icon | supply\_icon | gathering\_icon |  |  |
| portrait\_punishment\_icon | death\_icon | prestige\_level\_0\_icon (5) |  | fort\_icon | garrison\_icon | army\_quality\_icon\_1 (5) |  |  |
| skill\_diplomacy\_icon | scheme\_icon | dynasty\_prestige\_icon (5) |  | knight\_icon | embarked\_icon | no\_siege\_weapon\_icon |  |  |

## Usage of special characters & Line breaks\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Localization&veaction=edit&section=15 "Edit section: Usage of special characters & Line breaks") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Localization&action=edit&section=15 "Edit section: Usage of special characters & Line breaks")\]

If you wish to input characters such as **"** in a string, utilize **\** before every usage:

```
Hello, I am \"totally\" not going to stab you!
Hello, I am #weak\"totally\" not# going to stab you!
```

If you want to break line, you can use **\\n**:

```
This is line one, which will show up above,\nWhile this is line two, coming right at you from below.
```

Avoid adding spaces before or after the line break to preserve the text's alignment.

When adding multiple paragraphs, keep in mind that you can assign multiple keys to the same desc, which is particularly useful if you want to customize just one paragraph. For example, you can have a localization file with:

```
paragraph_separator:0 "\n\n"

first_paragraph:0 "Generic intro text"

maybe_second_paragraph:0 "Conditional text"
alternative_second_paragraph:0 "Alternative text"

final_paragraph:0 "Generic outro text"
```

Then, you can define an event like this:

```
event_name.100 = {
  desc = {
    desc = first_paragraph
    desc = paragraph_separator
    first_valid = {
      triggered_desc = {
        limit = { some_trigger = yes }
        desc = maybe_second_paragraph
      }
      triggered_desc = {
        limit = { some_trigger = no }
        desc = alternative_second_paragraph
      }
    }
    desc = paragraph_separator
    desc = final_paragraph
  }
}
```

This will be much easier to maintain than keeping 2 different entries in sync, and will be easier to read in the localization file.

## Chinese punctuation\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Localization&veaction=edit&section=16 "Edit section: Chinese punctuation") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Localization&action=edit&section=16 "Edit section: Chinese punctuation")\]

A common issue with Chinese text in earlier versions of the game is that lines were broken apart in the the wrong places, such as in the middle of words. This is caused by the game engine not recognising the Chinese ideographic punctuation marks as punctuation, so it treated lines of Chinese text as single words and inserted breaks wherever it wanted.

Sadly an engine fix was impossible, so to ensure proper line breaking in Chinese text, you need to use a half-width versions of the punctiation, followed by a space. Using the right character substitutions, the visual change should be minimal and the line breaks do end up in the proper places.

[![](https://ck3.paradoxwikis.com/images/0/04/Chinese_text_issue.png)](https://ck3.paradoxwikis.com/File:Chinese_text_issue.png)

A sample from the CK3 interface, demonstrating the effect of the substitutions. Left uses the original punctuation, right uses the substitutions.

| Original | Codepoint | Substitution | Codepoint | Note |
| --- | --- | --- | --- | --- |
| ```<br>。<br>``` | U+3002 Ideographic Full Stop | ```<br>｡ <br>``` | U+FF61 Halfwidth Ideographic Full Stop (and space) |  |
| ```<br>，<br>``` | U+FF0C Fullwidth Comma | ```<br>, <br>``` | U+002C Comma (and space) | Since there is no Chinese-style halfwidth comma, a Latin one may be an acceptable substitute. |
| ```<br>，<br>``` | U+FF0C Fullwidth Comma | ```<br>､ <br>``` | U+FF64 Halfwidth Ideographic Comma (and space) | This can also be used for the comma, but note the visual difference. |
| ```<br>-<br>``` | U+002D Hyphen-Minus | ```<br>‑<br>``` | U+2011 Non-Breaking Hyphen | This is a wholly optional substitution to prevent a hyphen from being detected as a word boundary; use this to lessen the chance of line breaks there. |

## References\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Localization&veaction=edit&section=17 "Edit section: References") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Localization&action=edit&section=17 "Edit section: References")\]

**[Modding](https://ck3.paradoxwikis.com/Modding "Modding")**

|     |     |
| --- | --- |
| Documentation | [Scripting](https://ck3.paradoxwikis.com/Scripting "Scripting") • [Scopes](https://ck3.paradoxwikis.com/Scopes "Scopes") • [Effects](https://ck3.paradoxwikis.com/Effects "Effects") • [Triggers](https://ck3.paradoxwikis.com/Triggers "Triggers") • [Variables](https://ck3.paradoxwikis.com/Variables "Variables") • [Modifiers](https://ck3.paradoxwikis.com/Modifier_list "Modifier list") |

|     |     |
| --- | --- |
| Scripting | [AI](https://ck3.paradoxwikis.com/AI_modding "AI modding") • [Bookmarks](https://ck3.paradoxwikis.com/Bookmarks_modding "Bookmarks modding") • [Characters](https://ck3.paradoxwikis.com/Characters_modding "Characters modding") • [Commands](https://ck3.paradoxwikis.com/Commands "Commands") • [Council](https://ck3.paradoxwikis.com/Council_modding "Council modding") • [Culture](https://ck3.paradoxwikis.com/Culture_modding "Culture modding") • [Decisions](https://ck3.paradoxwikis.com/Decisions_modding "Decisions modding") • [Dynasties](https://ck3.paradoxwikis.com/Dynasties_modding "Dynasties modding") • [Events](https://ck3.paradoxwikis.com/Event_modding "Event modding") • [Governments](https://ck3.paradoxwikis.com/Governments_modding "Governments modding") • [History](https://ck3.paradoxwikis.com/History_modding "History modding") • [Holdings](https://ck3.paradoxwikis.com/Holdings_modding "Holdings modding") • [Lifestyles](https://ck3.paradoxwikis.com/Lifestyles_modding "Lifestyles modding") • [Regiments](https://ck3.paradoxwikis.com/Regiments_modding "Regiments modding") • [Religions](https://ck3.paradoxwikis.com/Religions_modding "Religions modding") • [Script Values](https://ck3.paradoxwikis.com/Script_values "Script values") • [Story cycles](https://ck3.paradoxwikis.com/Story_cycles_modding "Story cycles modding") • [Struggles](https://ck3.paradoxwikis.com/Struggle_modding "Struggle modding") • [Titles](https://ck3.paradoxwikis.com/Title_modding "Title modding") • [Traits](https://ck3.paradoxwikis.com/Trait_modding "Trait modding") |

|     |     |
| --- | --- |
| Interface | [Interface](https://ck3.paradoxwikis.com/Interface "Interface") • [Data types](https://ck3.paradoxwikis.com/Data_types "Data types") • Localization • [Customizable localization](https://ck3.paradoxwikis.com/Customizable_localization "Customizable localization") • [Flavorization](https://ck3.paradoxwikis.com/Flavorization "Flavorization") |

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

Retrieved from " [https://ck3.paradoxwikis.com/index.php?title=Localization&oldid=32485](https://ck3.paradoxwikis.com/index.php?title=Localization&oldid=32485)"

[Categories](https://ck3.paradoxwikis.com/Special:Categories "Special:Categories"):

- [Pages using deprecated enclose attributes](https://ck3.paradoxwikis.com/index.php?title=Category:Pages_using_deprecated_enclose_attributes&action=edit&redlink=1 "Category:Pages using deprecated enclose attributes (page does not exist)")
- [Potentially outdated](https://ck3.paradoxwikis.com/Category:Potentially_outdated "Category:Potentially outdated")
- [1.4](https://ck3.paradoxwikis.com/Category:1.4 "Category:1.4")
- [Modding](https://ck3.paradoxwikis.com/Category:Modding "Category:Modding")