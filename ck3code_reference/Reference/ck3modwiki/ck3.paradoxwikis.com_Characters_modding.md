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

# Characters modding

From CK3 Wiki

[Jump to navigation](https://ck3.paradoxwikis.com/Characters_modding#mw-head) [Jump to search](https://ck3.paradoxwikis.com/Characters_modding#searchInput)

Please help with verifying or updating older sections of this article.

At least some were last verified for [version](https://ck3.paradoxwikis.com/CK3_Wiki:Versioning "CK3 Wiki:Versioning") 1.1.

This article is for the PC version of Crusader Kings 3 only.

Modding characters involves changing their appearance, data and behaviour. This can vary from small tweaks like adding gold or piety, to complex changes like scripting new visual effects and more.

## Contents

- [1Changing appearance through scripts](https://ck3.paradoxwikis.com/Characters_modding#Changing_appearance_through_scripts)
- [2Outfit Tags](https://ck3.paradoxwikis.com/Characters_modding#Outfit_Tags)
  - [2.1Using outfit\_tags](https://ck3.paradoxwikis.com/Characters_modding#Using_outfit_tags)
  - [2.2Creating outfit\_tags](https://ck3.paradoxwikis.com/Characters_modding#Creating_outfit_tags)
- [3Adding new characters or changing existing](https://ck3.paradoxwikis.com/Characters_modding#Adding_new_characters_or_changing_existing)
  - [3.1Advanced use of date blocks](https://ck3.paradoxwikis.com/Characters_modding#Advanced_use_of_date_blocks)
  - [3.2Hairstyles and beards for scripted characters](https://ck3.paradoxwikis.com/Characters_modding#Hairstyles_and_beards_for_scripted_characters)
- [4Calling characters from other scripts](https://ck3.paradoxwikis.com/Characters_modding#Calling_characters_from_other_scripts)
- [5References](https://ck3.paradoxwikis.com/Characters_modding#References)

## Changing appearance through scripts\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Characters_modding&veaction=edit&section=1 "Edit section: Changing appearance through scripts") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Characters_modding&action=edit&section=1 "Edit section: Changing appearance through scripts")\]

Crusader Kings 3 uses a DNA system to define a character's appearance, which has changed from the one used in Crusader Kings 2. These changes allow for more specific and realistic appearances.

You can change a character's DNA through dna\_modifiers. Create a file in `gfx/portraits/portrait_modifiers` with any filename and add this:

```
dna_change_example_modifier = {
    usage = game
    priority = 50 # priority line seems to be mandatory to display accessory.
    dna_change_example_modifier = {
        dna_modifiers = {
            accessory = {
                mode = add
                gene = headgear
                template = western_imperial
                value = 1.0
            }
            color = {
                mode = modify
                gene = hair_color
                x = 0.5
                y = -0.5
            }
        }
        weight = {
            base = 0
            modifier = {
                add = 100
                has_character_flag = dna_change_example_modifier
            }
        }
    }
}
```

(The higher the priority, the later the modifier will be applied (and overwrites previous ones). Set to 0 by default. If two groups have the same priority, they will be applied based on file order where these groups are.)

This will add the western\_imperial headgear and change the hair color of any character with the "dna\_change\_example\_modifier" flag. You can add a flag to a character with the add\_character\_flag command, like this:

```
add_character_flag = {
    flag = dna_change_example_modifier
}
```

If you encounter any issues, check the error.log of the game for any specific error messages and correct your script accordingly.

## Outfit Tags\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Characters_modding&veaction=edit&section=2 "Edit section: Outfit Tags") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Characters_modding&action=edit&section=2 "Edit section: Outfit Tags")\]

Playing dress-up with characters is a very important part of selling the medieval fantasy presented by Crusader Kings 3.

Outfit tags help us sell that fantasy by letting us force specific clothing or clothing groups on characters during an event.

Be warned that you should not apply armor to characters thorugh outfit tags. Instead you should set the `single_combat_duel_armor` character flag in `immediate` and then remove it in the `after` block of your event.

### Using outfit\_tags\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Characters_modding&veaction=edit&section=3 "Edit section: Using outfit tags") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Characters_modding&action=edit&section=3 "Edit section: Using outfit tags")\]

There are currently no compiled lists of valid outfit tags, therefore, the standard method of locating outfit tags is to search the `..game\events` and `..game\gfx\portraits\portrait_modifiers` folders for the keyword `outfit_tags`.

Once you have found an outfit tag you wish to use, you can either add it directly to the portrait.

```
right_portrait = {
	character = scope:undercover_thief
	animation = scheme
	outfit_tags = { # These tags all cover different parts of the body, so they will not overwrite one another
		western_stealth_hood		# A hood that covers the head
		sub_saharan_high_nobility	# Main clothing for torso and legs
		mena_war_legwear			# Some shoes
	}
}
```

Or use a `triggered_outfit` to make it conditional (such as, only if your gold is over a specific threshold, or if your spouse is dead).

```
right_portrait = {
	character = scope:merchant_with_funny_wooden_statues_for_sale
	animation = personality_rational
	triggered_outfit = {
		trigger = {} # Your trigger goes here, if it fails, the outfit won't be overridden
		outfit_tags = {} # Insert the tags you wish to use here
		remove_default_outfit = # Use yes/no, if set to yes, portrait modifier categories in which nothing matches any of the event tags will be disabled completely (no by default)
		hide_info = # Use yes/no, only the portrait will be shown, with no identifiable elements (no CoA, tooltips, clicks...) (no by default)
	}
}
```

### Creating outfit\_tags\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Characters_modding&veaction=edit&section=4 "Edit section: Creating outfit tags") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Characters_modding&action=edit&section=4 "Edit section: Creating outfit tags")\]

[![](https://ck3.paradoxwikis.com/images/thumb/d/d4/Modding_portrait_editor_button_and_UI_sample.jpg/287px-Modding_portrait_editor_button_and_UI_sample.jpg)](https://ck3.paradoxwikis.com/File:Modding_portrait_editor_button_and_UI_sample.jpg)

[Enlarge](https://ck3.paradoxwikis.com/File:Modding_portrait_editor_button_and_UI_sample.jpg "Enlarge")

Image showcasing how to open and use the portrait editor.

Before we get to scripting anything, we're going to want to preview the clothes in the portrait editor so we can get an idea of what it is that we want to add an outfit tag to.

First, open the portrait editor (small right-hand green button in the [console menu](https://ck3.paradoxwikis.com/Mod_troubleshooting#Getting_Access_to_the_Debug_Tools)).

Optionally, you can click "randomize DNA" to get a character that looks more human. Afterwards, click on the field right under "gene" to display a dropdown menu, select (or type in) the category you desire to preview.

Once selected, click on the button right under "subgroup" and do the same to select a specific article of clothing (gene).

Congratulations! You are now able to preview genes in the portrait editor. Be sure to keep an eye on the subgroup names and write down the ones you want to use.

The next step is to find or create our subgroup's outfit tag.

All clothing (actually genes, which includes hair) that can be worn by characters is stored inside files located at `..game\gfx\portraits\portrait_modifiers`.

The clothing templates will look more or less like this:

```
deal_with_it_sunglasses = {
  dna_modifiers = {
    accessory = {
      mode = add
      gene = clothes
      template = deal_with_it_sunglasses_headgear     # This is the subgroup with the refs to the 3D models it will load
      range = { 0 1 } # For the randomness to work correctly
    }
  }
  outfit_tags = { deal_with_it_sunglasses_headgear }  # This is the tag that you use in the portrait window. If this line is not here, just add it and use an appropriate name.
  weight = {                                          # ..It is usually good practice to name the new outfit tag after the subroup it comes from (which is why this one is named deal_with_it_sunglasses_headgear).
    base = 200
  }
}
```

As mentioned in the comment, if the article of clothing does not have an `outfit_tags` line, you can go ahead and add one.

If you can not find the clothing you wanted in any of the files based on the subgroup name, then you can create a full template instead.

First, pick a template that is similar to what you are trying to include, then you make a copy.

Afterwards, under `dna_modifiers` and `accessory`, replace the `template = some_name_here` with the subgroup name shown in the portrait editor, then update the names and outfit tags on your template so that they are unique (and somewhat matches the subgroup name for consistency reasons). If you do not like using the portrait editor, you can go to `..game\common\genes`, these files contain all the genes in the game.

## Adding new characters or changing existing\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Characters_modding&veaction=edit&section=5 "Edit section: Adding new characters or changing existing") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Characters_modding&action=edit&section=5 "Edit section: Adding new characters or changing existing")\]

For some mods, for example total conversions, new characters are needed. In Crusader Kings 3 this kind of character modding is pretty easy.
After creating your mod (which is explained in a corresponding article), you have to edit an existing or create a new txt.-file in the folder `example-mod/history/characters`.
In our example the file will be named `example.txt`. An example character will look like this:

```
999001 = {
	name = "Henri"	#Henri de Lyon
	dna = lyon_twin_dna_entry
	dynasty = 2100001 #Lyon
	martial = 14
	diplomacy = 23
	intrigue = 10
	stewardship = 21
	religion = catholic
	culture = french
	trait = diligent
	trait = education_learning_4
	trait = just
	trait = twin
	trait = physique_good_3
	trait = intellect_good_3
	trait = beauty_good_3
	trait = shrewd
	disallow_random_traits = yes
	father = 999003
	mother = 999004
	846.7.29 = {
		birth = yes
	}
	920.5.25 = {
		death = yes
	}
}
```

- First of all, a character ID is assigned. The ID needs to be unique; going for 900000 and further should be safe. Also it allowed to use chars inside the ID-String like "modChar0". In case of a small mod with a limited number of characters it could be usefull to take the characters name as ID aslong the string itself keep unique for all characters. This ID is used to refer to the character within the game files and is replaced by dynmaic one, when a new game is created.
- The first name of the character can be set via the use of `name = "NAME"`. Note that in-game names may change based on culture (see [culture modding](https://ck3.paradoxwikis.com/Culture_modding "Culture modding")).
- In the dna-line the path for a specific dna can be inserted. An existing dna from the `00_dna.txt` in `common/dna_data` can be used or an new created by using the portrait editor.
- To set the character's gender to female, use `female = yes`.
- A character can be added to an existing or a new dynasty. Use `dynasty = DYNASTY_ID` for dynasties without houses, or `dynasty_house = HOUSE_ID` otherwise. The dynasty ID and house ID can be found in `common/dynasties` and `common\dynasty_houses`, respectively. See [dynasties modding](https://ck3.paradoxwikis.com/Dynasties_modding "Dynasties modding").
- Culture and faith must be assigned with `culture = CULTURE_ID` and `religion = FAITH_ID`, respectively. The right names can be found by searching in the corresponding folders `common/culture` and `common/religion`.
- Attributes can be set freely. Their value caps at 100. If they are not assigned, the game will generate random values. Note that this only adds to the character's _base_ attribute values, so the final value may be smaller or larger depending on traits and other factors. The attributes are as follows:

- `martial`
- `prowess`
- `diplomacy`
- `intrigue`
- `stewardship`
- `learning`

- Traits can be added through the use of `trait = TRAIT_ID`. Replace `TRAIT_ID` with the appropriate [trait ID](https://ck3.paradoxwikis.com/Trait_ID "Trait ID"). An unlimited amount of traits may be added; unless assigned or specified otherwise, the game will generate random traits. To ensure that traits are not changed at the start of the game, use `disallow_random_traits = yes`.
- Parents may be optionally assigned by using `father = CHARACTER_ID` and `mother = CHARACTER_ID`. Ensure that one uses the target character's ID, as opposed to their name. This can be useful in creating families.
- Sexuality can be set through `sexuality = SEXUALITY_ID`. The following can be used:

- `asexual`
- `heterosexual`
- `homosexual`
- `bisexual`

- Set the character's base health through `health = HEALTH_VALUE`, and fertility with `fertility = FERTILITY_VALUE`.

- Finally, birth and death of the character have to be defined. Crusader Kings 3 uses `yyyy.mm.dd` for date formats. Define a date block using `DATE = {...}`, replacing `...` with `birth = yes` or `death = yes`. Alternatively, replace `yes` with the date surrounded by speech marks (`"`). See [more uses of date blocks](https://ck3.paradoxwikis.com/Characters_modding#Advanced_use_of_date_blocks).

The same steps work for changing existing characters. Sometimes, like for Charlemagne, there are already most of the possible lines.

### Advanced use of date blocks\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Characters_modding&veaction=edit&section=6 "Edit section: Advanced use of date blocks") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Characters_modding&action=edit&section=6 "Edit section: Advanced use of date blocks")\]

- `add_spouse = CHARACTER_ID`, `remove_spouse = CHARACTER_ID` to add/remove spouses.
- `give_nickname = NICKNAME_ID` to add nicknames. Later uses of `give_nickname` replace old nicknames. See [nickname ID](https://ck3.paradoxwikis.com/Nickname_ID "Nickname ID").
- `employer = CHARACTER_ID`, similar to `set_employer = CHARACTER_ID` effect, moves the scoped character to the specified character's court.
- `give_council_position = COUNCILLOR_ID` to make the character a councillor. The following are accepted:

- `councillor_marshal`
- `councillor_spymaster`
- `councillor_chancellor`
- `councillor_court_chaplain`
- `councillor_steward`

- Assignments defined in the previous section, like `trait = TRAIT_ID`, may also be used in date blocks.
- Various other [effects](https://ck3.paradoxwikis.com/Effect "Effect") can be used that have a character scope, either directly in the date block or in an `effect` sub-block. See the following example from the game files, used to add a character flag and set character sexuality randomly:[\[1\]](https://ck3.paradoxwikis.com/Characters_modding#cite_note-1)

```
101515 = {
	...
	1019.1.1 = {
		...
		effect = {
			add_character_flag = has_scripted_appearance
			random_list = {
				50 = { set_sexuality = heterosexual }
				50 = { set_sexuality = bisexual }
			}
		}
	}
	...
}
```

### Hairstyles and beards for scripted characters\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Characters_modding&veaction=edit&section=7 "Edit section: Hairstyles and beards for scripted characters") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Characters_modding&action=edit&section=7 "Edit section: Hairstyles and beards for scripted characters")\]

To make a scripted character use the correct hairstyle and beard in-game, an entry must be added to `gfx\portraits\portrait_modifiers\99_beards_scripted_characters.txt` and `gfx\portraits\portrait_modifiers\99_hairstyles_scripted_characters.txt`. Under the entry for the hairstyle you want, add the following:

```
modifier = {
	add = 200
	exists = character:<history_id>
	this = character:<history_id>
}
```

## Calling characters from other scripts\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Characters_modding&veaction=edit&section=8 "Edit section: Calling characters from other scripts") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Characters_modding&action=edit&section=8 "Edit section: Calling characters from other scripts")\]

It is possible for mods to interact with existing pre-defined characters from their scripts, just like other scopes. Use code `character:<id>` to reference to characters. Below is an example from game files:

```
# this code can be found in /common/on_action/game_start.txt at line 15 (version 1.5.1.1)
character:74025 = {
	if = {
		limit = {
			is_alive = yes
			is_landed = yes
		}
	}
	trigger_event = bookmark.0200
}
```

## References\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Characters_modding&veaction=edit&section=9 "Edit section: References") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Characters_modding&action=edit&section=9 "Edit section: References")\]

1. [↑](https://ck3.paradoxwikis.com/Characters_modding#cite_ref-1 "Jump up")`game\history\characters\danish.txt`, character `101515`

**[Modding](https://ck3.paradoxwikis.com/Modding "Modding")**

|     |     |
| --- | --- |
| Documentation | [Scripting](https://ck3.paradoxwikis.com/Scripting "Scripting") • [Scopes](https://ck3.paradoxwikis.com/Scopes "Scopes") • [Effects](https://ck3.paradoxwikis.com/Effects "Effects") • [Triggers](https://ck3.paradoxwikis.com/Triggers "Triggers") • [Variables](https://ck3.paradoxwikis.com/Variables "Variables") • [Modifiers](https://ck3.paradoxwikis.com/Modifier_list "Modifier list") |

|     |     |
| --- | --- |
| Scripting | [AI](https://ck3.paradoxwikis.com/AI_modding "AI modding") • [Bookmarks](https://ck3.paradoxwikis.com/Bookmarks_modding "Bookmarks modding") • Characters • [Commands](https://ck3.paradoxwikis.com/Commands "Commands") • [Council](https://ck3.paradoxwikis.com/Council_modding "Council modding") • [Culture](https://ck3.paradoxwikis.com/Culture_modding "Culture modding") • [Decisions](https://ck3.paradoxwikis.com/Decisions_modding "Decisions modding") • [Dynasties](https://ck3.paradoxwikis.com/Dynasties_modding "Dynasties modding") • [Events](https://ck3.paradoxwikis.com/Event_modding "Event modding") • [Governments](https://ck3.paradoxwikis.com/Governments_modding "Governments modding") • [History](https://ck3.paradoxwikis.com/History_modding "History modding") • [Holdings](https://ck3.paradoxwikis.com/Holdings_modding "Holdings modding") • [Lifestyles](https://ck3.paradoxwikis.com/Lifestyles_modding "Lifestyles modding") • [Regiments](https://ck3.paradoxwikis.com/Regiments_modding "Regiments modding") • [Religions](https://ck3.paradoxwikis.com/Religions_modding "Religions modding") • [Script Values](https://ck3.paradoxwikis.com/Script_values "Script values") • [Story cycles](https://ck3.paradoxwikis.com/Story_cycles_modding "Story cycles modding") • [Struggles](https://ck3.paradoxwikis.com/Struggle_modding "Struggle modding") • [Titles](https://ck3.paradoxwikis.com/Title_modding "Title modding") • [Traits](https://ck3.paradoxwikis.com/Trait_modding "Trait modding") |

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

Retrieved from " [https://ck3.paradoxwikis.com/index.php?title=Characters\_modding&oldid=26267](https://ck3.paradoxwikis.com/index.php?title=Characters_modding&oldid=26267)"

[Categories](https://ck3.paradoxwikis.com/Special:Categories "Special:Categories"):

- [Potentially outdated](https://ck3.paradoxwikis.com/Category:Potentially_outdated "Category:Potentially outdated")
- [1.1](https://ck3.paradoxwikis.com/Category:1.1 "Category:1.1")
- [Modding](https://ck3.paradoxwikis.com/Category:Modding "Category:Modding")