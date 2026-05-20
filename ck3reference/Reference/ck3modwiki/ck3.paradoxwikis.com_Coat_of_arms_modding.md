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

# Coat of arms modding

From CK3 Wiki

[Jump to navigation](https://ck3.paradoxwikis.com/Coat_of_arms_modding#mw-head) [Jump to search](https://ck3.paradoxwikis.com/Coat_of_arms_modding#searchInput)

This article is [timeless](https://ck3.paradoxwikis.com/Category:Timeless "Category:Timeless") and should be accurate for any version of the game.

**Coat of arms** are images used on shields and flags to identify titles, dynasties, and houses.

They are scripted in /Crusader Kings III/game/common/coat\_of\_arms/coat\_of\_arms.

They follow the basic scripting syntax of:

```
coat_of_arms_name = {
    keyword1 = value1
    keyword2 = value2
    ...
}
```

Is the "coat\_of\_arms\_name" identical to an title, house or dynasty keyname (like "d\_leon") the game will automatically using this CoA as default layout at game-start for this. This is also working with modded titles, houses or dynasties.

## Contents

- [1Valid keywords](https://ck3.paradoxwikis.com/Coat_of_arms_modding#Valid_keywords)
- [2Examples](https://ck3.paradoxwikis.com/Coat_of_arms_modding#Examples)
- [3Inheritance and subs](https://ck3.paradoxwikis.com/Coat_of_arms_modding#Inheritance_and_subs)
- [4Dynamic Coats of Arms](https://ck3.paradoxwikis.com/Coat_of_arms_modding#Dynamic_Coats_of_Arms)
- [5Easy going by using the IN-Game Designer](https://ck3.paradoxwikis.com/Coat_of_arms_modding#Easy_going_by_using_the_IN-Game_Designer)
  - [5.1Designer weaknesses](https://ck3.paradoxwikis.com/Coat_of_arms_modding#Designer_weaknesses)
- [6Coat of Arms Emblem Modding](https://ck3.paradoxwikis.com/Coat_of_arms_modding#Coat_of_Arms_Emblem_Modding)
  - [6.1.DDS file formatting](https://ck3.paradoxwikis.com/Coat_of_arms_modding#.DDS_file_formatting)
  - [6.2Emblem definitions file](https://ck3.paradoxwikis.com/Coat_of_arms_modding#Emblem_definitions_file)

## Valid keywords\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Coat_of_arms_modding&veaction=edit&section=1 "Edit section: Valid keywords") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Coat_of_arms_modding&action=edit&section=1 "Edit section: Valid keywords")\]

| Keyword | Comment | Example |
| --- | --- | --- |
| `parent` | Used for inheritance, read more below. | `parent = k_england` |
| `pattern` | The path to the file for the background pattern (usually located in /Crusader Kings III/game/gfx/coat\_of\_arms/patterns/.<br>A pattern should be included to avoid graphical issues with the masking textures when using textured emblems. | ```<br>pattern = "pattern_vertical_split_01"<br>``` |
| ```<br>color1<br>color2<br>color3<br>color4<br>color5<br>``` | Specifies a color, to be used in the pattern or as a color reference in colored\_emblems.<br>Usually refers to a color defined in /Crusader Kings III/game/common/named\_colors.<br>Can also explicitly define RGB, HSV and 8-Digit Hexadecimal values. | ```<br>color1 = "white"<br>color2 = hsv { 1.0 1.0 1.0 }<br>color3 = hsv360 { 360 100 100 }<br>color4 = rgb { 255 255 255 }<br>color5 = hex { aabbccdd }<br>``` |
| `textured_emblem` | \-\-\- | Multiple textured emblems can be specified. Each is itself a scripting object with the following valid keywords: | \-\-\- |
| `texture` | The path to the file for the emblem (usually located in /Crusader Kings III/game/gfx/coat\_of\_arms/textured\_emblems/). | ```<br>texture = "te_griffin_01.dds"<br>``` |
| `mask` | The coat of arms' background pattern can be used as a clipping mask for emblems. | ```<br>mask = { 1 3 }<br>``` |
| `instance` | `scale` | Given as a 2-dim float, has default value { 1.0 1.0 } | ```<br>instance = { <br>	scale = { 0.5 0.5 }  <br>	position = { 0.75 0.75 } <br>	rotation = 45<br>	depth = 5  <br>}<br>``` |
| `position` | Given as a 2-dim float, has default value { 0.0 0.0 } |
| `rotation` | Given as float value, has default value 0.0 |
| `depth` | Used to order rendering, given as float value with default of 0.0 |
| `colored_emblem` | \-\-\- | Multiple colored emblems can be specified. Each is itself a scripting object with the following keywords: | \-\-\- |
| `texture` | The path to the file for the emblem (usually located in /Crusader Kings III/game/gfx/coat\_of\_arms/colored\_emblems/). | ```<br>texture = "ce_crown.tga"<br>``` |
| " | All fields from textured\_emblem are valid | \-\-\- |
| `color1` | defines the base colour of the emblem | ```<br>color1 = color2<br>color2 = "white"<br>#color3 = hsv360 { 360 50 50 }<br>``` |
| `color2` | defines the secondary color of the emblem (the Green channel in the texture) |
| `color3` | currently unavailable, will default to white |
| `sub` | \-\-\- | Multiple subs can be specified, each is itself a complete coat of arms scripting object, allowing all fields except another sub, i.e. no sub nesting. | \-\-\- |
| `instance` | `scale` | Given as a 2-dim float, has default value { 1.0 1.0 } | \-\-\- |
| `offset` | Given as a 2-dim float, has default value { 0.0 0.0 } | \-\-\- |
| `depth` | Used to order rendering, given as float value with default of 0.0 | \-\-\- |

## Examples\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Coat_of_arms_modding&veaction=edit&section=2 "Edit section: Examples") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Coat_of_arms_modding&action=edit&section=2 "Edit section: Examples")\]

Here follows a few examples with their corresponding coat of arms.

```
flag_with_emblem = {
    pattern = "pattern_vertical_split_01"
    color1 = "lemon_yellow"
    color2 = "sky_blue"

    textured_emblem = {
        texture = "te_griffin_01"
    }
}
```

```
flag_with_culled_emblem = {
    pattern = "pattern_vertical_split_01"
    color1 = "lemon_yellow"
    color2 = "sky_blue"

    textured_emblem = {
        texture = "te_griffin_01"
        mask = { 1 }
    }
}
```

```
two_emblems_scaled_and_positioned = {
    pattern = "pattern_vertical_split_01"
    color1 = "lemon_yellow"
    color2 = "sky_blue"

    textured_emblem = {
        texture = "te_griffin_01"
        instance = { position = { 0.75 0.75 } scale = { 0.5 0.5 }  }
        instance = { position = { 0.75 0.25 } scale = { 0.5 0.5 }  }
    }
}
```

[![Emblem examples.png](https://ck3.paradoxwikis.com/images/2/20/Emblem_examples.png)](https://ck3.paradoxwikis.com/File:Emblem_examples.png)

## Inheritance and subs\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Coat_of_arms_modding&veaction=edit&section=3 "Edit section: Inheritance and subs") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Coat_of_arms_modding&action=edit&section=3 "Edit section: Inheritance and subs")\]

This section is largely dedicated towards inheritance, but to facilitate that discussion, first two points on subs:

The first "base coat of arms" is an implicit sub:

```
a = {
    pattern = "pattern_solid.tga"
    color1 = "blue"
    sub = { }
}
# the above is equal to:
b = {
    sub = {
        pattern = "pattern_solid.tga"
        color1 = "blue"
    }
    sub = { }
}
```

Each instance field (coat of arms instances, not emblem instances) is transformed into a separate sub:

```
a = {
    color1 = "blue"
    instance = { offset = { 0 0 } } # A
    instance = { offset = { 1 0 } } # B
    sub {
        color1 = "red"
        instance = { offset= { 0 1 } } # C
        instance = { offset = { 1 1 } } # D
    }
}
# the above is equal to:
b = {
    sub = {
        color1 = "blue"
        instance = { offset = { 0 0 } } # A
    }
    sub = {
        color1 = "blue"
        instance = { offset = { 1 0 } } # B
    }
    sub {
        color1 = "red"
        instance = { offset = { 0 1 } } # C
    }
    sub {
        color1 = "red"
        instance = { offset = { 1 1 } } # D
    }
}
```

With that out of the way, let's dive into inheritance.

Inheritance is achieved through the parent keyword. It basically says "Fetch the coat of arms given as value, and use it to populate any fields not explicitly set".

Example:

```
daddy = {
    pattern = "pattern_checkers_01.tga"
    color1 = "burned_red"
    color2 = "mid_grey"
    colored_emblem = {
        texture = "ce_angel.dds"
        color1 = "rust_brown"
        color2 = "rust_brown"
    }
}

child = {
    parent = "daddy"
    pattern = "pattern_checkers_diagonal_01.tga"
    color1 = "mint_green"
    # >color2 = "mid_grey"<        inherited
    # >colored_emblem = { ... }<   inherited
}
```

When it comes to emblems the inheritance is "all or nothing": if at least one emblem (of any type) is specified, no emblems are inherited, but if no emblem is specified, all the parent's emblems are inherited.

The inheritance rules become slightly more complicated once subs are involved. The two guiding rules are:

When a parent is specified, all values are fetched from its first sub (which many times will be an "implicit" sub).
If a sub doesn't specify a parent it will piggyback on the parent of its first sub. However, in this case all values will be fetched from the corresponding sub in the parent. Setting parent = "none" disables this automatic inheritance.
Example:

```
daddy = {
    pattern = "pattern_solid.tga"
    sub = { }
    sub = { }
}

child = {
    parent = "daddy"
    # this implicit sub inherits from the implicit sub in daddy
    sub = {
        # Since no parent is specified this sub will piggyback on >parent = "daddy"< and inherit from the second sub of "daddy".
    }
    sub = {
        parent = "other_coa"
        # since parent is specified explicitly this will inherit from first sub of "other_coa"
    }
}
```

Inheritance chains ("deep inheritance") is resolved in a bottom up manner. Users must take care not to create inheritance loops.

```
grand_dad = {
    pattern = "pattern_solid.tga"
    sub = { }
}

daddy = {
    parent = "grand_dad"
    # >pattern = "pattern_solid.tga"< inherited
    color1 = "blue"
    # >sub = { }< inherited
}

child = {
    parent = "daddy"
    # >pattern = "pattern_solid.tga"< inherited
    # >color1 = "blue"< inherited
    sub = {
        # this inherits from the second sub in daddy
    }
    sub = {
        # since daddy only has 2 subs, this has no parent
    }
}
```

And finally, a real example:

```
k_england_and_france = {
    sub = {
        parent = "k_france"  # defined elsewhere
        instance = { offset = { 0.0 0.0 } scale = { 0.5 0.5 }  } # top left
        instance = { offset = { 0.5 0.5 } scale = { 0.5 0.5 }  } # bottom right
    }
    sub = {
        parent = "k_england"  # defined elsewhere
        instance = { offset = { 0.5 0.0 } scale = { 0.5 0.5 }  } # top right
        instance = { offset = { 0.0 0.5 } scale = { 0.5 0.5 }  } # bottom left
    }
}
```

## Dynamic Coats of Arms\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Coat_of_arms_modding&veaction=edit&section=4 "Edit section: Dynamic Coats of Arms") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Coat_of_arms_modding&action=edit&section=4 "Edit section: Dynamic Coats of Arms")\]

In addition to the normal coats of arms assigned to any given title, you can also create dynamic coat of arms definitions, which are stored in /Crusader Kings III/game/\\common\\coat\_of\_arms\\dynamic\_definitions\:

```
# Name must match a landed title definition
title_name = {
	item = { # One or more items
		trigger = { # Trigger for when this item should be picked, first valid item is picked, root = the title
			<trigger> # This can be any scripted trigger, or a trigger defined inline as normal
		}
		coat_of_arms = name # Name of coat of arms to use as defined in Coat of Arms files
	}
}
```

In order to update the coat of arms, you need to call `update_dynamic_coa = yes` within the title scope. This is already called in `on_character_culture_change` and `on_character_faith_change` for all held titles, but if you want the dynamic coat of arms to be updated under any other circumstance, it's up to you to implement [on\_actions](https://ck3.paradoxwikis.com/Event_modding#On_Actions_.28on_action.29 "Event modding") as needed.

## Easy going by using the IN-Game Designer\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Coat_of_arms_modding&veaction=edit&section=5 "Edit section: Easy going by using the IN-Game Designer") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Coat_of_arms_modding&action=edit&section=5 "Edit section: Easy going by using the IN-Game Designer")\]

Together with the Royal Court DLC, Paradox has also created a handy ingame editor that can also be used to export the created CoA directly as valid script code. To do this, you simply create your desired coat of arms with the designer and then press the "Copy to clipboard" button. The game then creates the completely finished and valid code required for a coat of arms in the intermediate storage of the PC used. You can then insert this directly into the corresponding text file for your mod using the key combination CTRL+V. You just have to make sure that you set the right name (e.g. k\_england). The modder can also use a trick here and simply remove the localization files for a short time; CK then fails to load the name for the title and then displays the title's corresponding keyword in-game instead. The player could also change the title name via the CoA Designer or, in this case, simply copy the keyword and paste it into the appropriate file. In this way you can avoid typos, which would later lead to the corresponding CoA not being displayed ingame.

It should be noted again at this point that due to dynamic CoAs, there can be several CoAs, which can therefore also have a name that does not directly match a title key. Accordingly, the CK interpreter cannot recognize a typo and would therefore not issue an error message. If the self-made CoA is not displayed, the correct, character-accurate spelling should be explicitly checked again.

### Designer weaknesses\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Coat_of_arms_modding&veaction=edit&section=6 "Edit section: Designer weaknesses") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Coat_of_arms_modding&action=edit&section=6 "Edit section: Designer weaknesses")\]

The Designer may be intuitively easier to use than, for example, manually coding a CoA, but the Designer cannot be used to inherit or subdivide the CoA. The real example shown above, where you put the English and French coat of arms together into one, can practically not be created with the designer. Even the Spanish flag from EU4, which is a combination of the coats of arms of Castile, Leon, Aragon, Navarra and Sicily, could not be recreated with the designer. However, one of the designers can help create the base crest, so all you have to do afterwards is manually script the inheritance.

## Coat of Arms Emblem Modding\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Coat_of_arms_modding&veaction=edit&section=7 "Edit section: Coat of Arms Emblem Modding") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Coat_of_arms_modding&action=edit&section=7 "Edit section: Coat of Arms Emblem Modding")\]

By default, the CoA Designer only displays the emblems of the original game. However, it is very easy to expand the list.

### .DDS file formatting\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Coat_of_arms_modding&veaction=edit&section=8 "Edit section: .DDS file formatting") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Coat_of_arms_modding&action=edit&section=8 "Edit section: .DDS file formatting")\]

In order for your custom emblems to be recognized by the game, they must be saved as a .DDS file with a specific format. The file format should be "8.8.8.8 ARGB 32bpp / Unsigned"; this is also known as "B8G8R8A8 (Linear, A8R8G8B8)" in paint.net, a common free image editing program. You can also enable Mip Maps to improve image fidelity at smaller scales, although this is not required. In the image itself, only three specific colors should be used. The game automatically recognizes the color value 0x000084 (blue) as color 1, the color value 0x00FF94 (light green) as color 2, and the color value 0xFF0084 (magenta) as color 3. CK has a certain tolerance and tries to match other deviating colors according to one of these color values. However, this correction is not perfect and cannot be relied upon; the modder should always make sure to use the right colors.

### Emblem definitions file\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Coat_of_arms_modding&veaction=edit&section=9 "Edit section: Emblem definitions file") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Coat_of_arms_modding&action=edit&section=9 "Edit section: Emblem definitions file")\]

In addition, you must now create a text file at the same position (as always in UTF-8 BOM coding). In the text file you can now create a separate line with the following syntax for each emblem that you want to offer in the designer:

```
<pic_name>.dds = { colors = <1,2,3> category = <string> }
```

In order for the game to correctly recognize the emblems, the name in the text file must exactly match the name of the image file.

You can specify 1, 2, or 3 as the color option. This specifies how many colors the user can set for the chosen emblem. If you set a value in the corresponding file that is larger than the number of colors actually used, the user has one more color option but it will not have any function. However, if the modder specifies too small a number of colors in the text file, the automatic correction will either try to reduce the extra colors to one color if they are similar enough or simply set the unknown color to a reddish-brown hue, which cannot be changed by the user.

The game supports the following default categories: animals, circles\_spirals, crosses\_and\_knots, faiths, manmade, nature, patterns, tribal\_seal, writing & figures. If a different string is used, the game will add a new selectable category for the user. As the category name is displayed as text, you should also define a new line in the localization file for each new category as follows:

```
COA_DESIGNER_CATEGORY_<your_category_string_here>:0 "<What you want to Display as Category Name for the selected language>"
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
| Graphics | [3D models](https://ck3.paradoxwikis.com/3D_models "3D models") • [Exporters](https://ck3.paradoxwikis.com/Exporters "Exporters") • Coat of arms • [Graphical assets](https://ck3.paradoxwikis.com/Graphical_assets "Graphical assets") • [Fonts](https://ck3.paradoxwikis.com/Fonts "Fonts") • [Particles](https://ck3.paradoxwikis.com/index.php?title=Particles&action=edit&redlink=1 "Particles (page does not exist)") • [Shaders](https://ck3.paradoxwikis.com/index.php?title=Shaders&action=edit&redlink=1 "Shaders (page does not exist)") • [Unit models](https://ck3.paradoxwikis.com/index.php?title=Unit_models&action=edit&redlink=1 "Unit models (page does not exist)") |

|     |     |
| --- | --- |
| Audio | [Music](https://ck3.paradoxwikis.com/Music_modding "Music modding") • [Sound](https://ck3.paradoxwikis.com/Sound_modding "Sound modding") |

|     |     |
| --- | --- |
| Other | [Console commands](https://ck3.paradoxwikis.com/Console_commands "Console commands") • [Checksum](https://ck3.paradoxwikis.com/Checksum "Checksum") • [Mod structure](https://ck3.paradoxwikis.com/Mod_structure "Mod structure") • [Mod compatibility](https://ck3.paradoxwikis.com/Mod_compatibility "Mod compatibility") • [Modding tools](https://ck3.paradoxwikis.com/Modding_tools "Modding tools") • [Troubleshooting](https://ck3.paradoxwikis.com/Mod_troubleshooting "Mod troubleshooting") |

Retrieved from " [https://ck3.paradoxwikis.com/index.php?title=Coat\_of\_arms\_modding&oldid=26714](https://ck3.paradoxwikis.com/index.php?title=Coat_of_arms_modding&oldid=26714)"

[Categories](https://ck3.paradoxwikis.com/Special:Categories "Special:Categories"):

- [Timeless](https://ck3.paradoxwikis.com/Category:Timeless "Category:Timeless")
- [Modding](https://ck3.paradoxwikis.com/Category:Modding "Category:Modding")