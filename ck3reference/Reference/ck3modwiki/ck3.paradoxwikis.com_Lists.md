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

# Lists

From CK3 Wiki

[Jump to navigation](https://ck3.paradoxwikis.com/Lists#mw-head) [Jump to search](https://ck3.paradoxwikis.com/Lists#searchInput)

Lists can be accessed using [list-builders](https://ck3.paradoxwikis.com/List-builders "List-builders"): `any_X`, `every_X`, `random_X`, `ordered_X`.

This article will use the `every_X` effect list-builder in its examples.

## Contents

- [1Code lists](https://ck3.paradoxwikis.com/Lists#Code_lists)
  - [1.1List Parameters](https://ck3.paradoxwikis.com/Lists#List_Parameters)
- [2scripted\_lists](https://ck3.paradoxwikis.com/Lists#scripted_lists)
- [3Custom lists](https://ck3.paradoxwikis.com/Lists#Custom_lists)
  - [3.1Normal lists](https://ck3.paradoxwikis.com/Lists#Normal_lists)
  - [3.2Variable lists](https://ck3.paradoxwikis.com/Lists#Variable_lists)

## Code lists\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Lists&veaction=edit&section=1 "Edit section: Code lists") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Lists&action=edit&section=1 "Edit section: Code lists")\]

When a scope has the same relation to multiple others, those can be provided in a list built in code. For example, in a character scope, code provides the `child` list, which contains all children that character ever had.

### List Parameters\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Lists&veaction=edit&section=2 "Edit section: List Parameters") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Lists&action=edit&section=2 "Edit section: List Parameters")\]

Some code lists have specific parameters that can be used in the list-builders. As those are parameters of the list, and not triggers, they don't go in the limit block.

- even\_if\_dead

Code lists of character scopes often only access living characters by default, even if the list technically includes dead character, in which case the \`even\_if\_dead\` parameter allows accessing dead characters.

```
every_child = {
   even_if_dead = yes
   limit = { < triggers > }
   < effects >
}
```

- scripted\_relations

From a character [scope](https://ck3.paradoxwikis.com/Scope "Scope"), the `relations` list provides all scripted\_relations of that character.
The `type` parameter specifies which scripted\_relations should be in the list.

```
every_relation = {
   type = friend
   type = lover
   limit = { < triggers > }
   < effects >
}
```

## scripted\_lists\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Lists&veaction=edit&section=3 "Edit section: scripted lists") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Lists&action=edit&section=3 "Edit section: scripted lists")\]

[\[top\]](https://ck3.paradoxwikis.com/Lists#top)

scripted\_lists are defined in `common/scripted_lists` and are used to customize code lists often used with the same limit conditions.

Ex: list builder for adult unlanded children

```
adult_unlanded_child = {
   base = child # any vanilla list builder can be used as base
   conditions = {
      is_adult = yes
      is_landed_ruler = no
   }
}
```

Once defined as such, this scripted\_list can be used with all list-builders, and further trimmed down using a [limit](https://ck3.paradoxwikis.com/Limit "Limit") block.

```
every_adult_unlanded_child = {
   limit = { < triggers > }
   < effects >
}
```

Note: as of 1.4.4, scripted\_lists cannot be used in script\_values, which is likely a bug.

## Custom lists\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Lists&veaction=edit&section=4 "Edit section: Custom lists") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Lists&action=edit&section=4 "Edit section: Custom lists")\]

[\[top\]](https://ck3.paradoxwikis.com/Lists#top)

The `in_list` list-builder can be used to access arbitrarily named lists of scopes created in script.

### Normal lists\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Lists&veaction=edit&section=5 "Edit section: Normal lists") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Lists&action=edit&section=5 "Edit section: Normal lists")\]

The `add_to_list` effect adds the scope it is executed from to the list with that name.

```
add_to_list = < list name >
```

Once the list is built, it can be accessed using list-builders through `in_list`, with the list name provided as a parameter:

```
every_in_list = {
   list = < list name >
   limit = { < triggers > }
   < effects >
}
```

Like a [saved scope](https://ck3.paradoxwikis.com/Saved_scope "Saved scope"), a normal list is available throughout the unbroken effect chain it is built in.

### Variable lists\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Lists&veaction=edit&section=6 "Edit section: Variable lists") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Lists&action=edit&section=6 "Edit section: Variable lists")\]

The `add_to_variable_list` effect adds the target [scope](https://ck3.paradoxwikis.com/Scope "Scope") to a list stored on the [scope](https://ck3.paradoxwikis.com/Scope "Scope") it is executed in.

```
add_to_variable_list = {
   name = < list name >
   target = < scope >
}
```

The target can be provided with a database reference, an event target, or a saved scope.

Once the list is built, it can be accessed using list-builders through the `in_list`, with the list name provided as a parameter:

```
every_in_list = {
   variable = < variable list name >
   limit = { < triggers >
   < effects >
}
```

.

Like a [variable](https://ck3.paradoxwikis.com/index.php?title=Variable&action=edit&redlink=1 "Variable (page does not exist)"), a variable list is stored on a specific scope, and can only be accessed from that specific scope.

Retrieved from " [https://ck3.paradoxwikis.com/index.php?title=Lists&oldid=20403](https://ck3.paradoxwikis.com/index.php?title=Lists&oldid=20403)"

[Category](https://ck3.paradoxwikis.com/Special:Categories "Special:Categories"):

- [Modding](https://ck3.paradoxwikis.com/Category:Modding "Category:Modding")