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

# Interactions modding

From CK3 Wiki

[Jump to navigation](https://ck3.paradoxwikis.com/Interactions_modding#mw-head) [Jump to search](https://ck3.paradoxwikis.com/Interactions_modding#searchInput)

Character interactions are set up in common/character\_interactions.

See \_character\_interactions.info file in that folder for more details.

## Example\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Interactions_modding&veaction=edit&section=1 "Edit section: Example") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Interactions_modding&action=edit&section=1 "Edit section: Example")\]

The simplest interaction looks like this:

```
basic_interaction = {
  on_accept = {
    scope:actor = {
      add_gold = 100
    }
    scope:recipient = {
      remove_short_term_gold = 100
    }
  }
  auto_accept = {
    always = yes
  }
}
```

[![an interaction that gives the player 100 gold and removes 100 gold from the selected character](https://ck3.paradoxwikis.com/images/thumb/8/87/Basic_interaction.png/356px-Basic_interaction.png)](https://ck3.paradoxwikis.com/File:Basic_interaction.png)

Interactions expect the recipient to accept it and then an effect happens. auto\_accept makes it instant, which is nice for testing.

We can also use on\_send instead, but that won't create a preview of the effects.

On\_accept and other effect blocks don't have a root scope, so we need to tell the interaction who the effects should apply to.

There are scopes provided by game code for us:

- **scope:actor** \- the character who initiated the interaction
- **scope:recipient** \- the recipient of the interaction

Always remember to scope to a character first and then apply the effects.

Note that the interaction above will appear in "Uncategorized" category in the interactions menu.

A properly formatted interaction should have a category and an icon. And potentially a description.

Retrieved from " [https://ck3.paradoxwikis.com/index.php?title=Interactions\_modding&oldid=20307](https://ck3.paradoxwikis.com/index.php?title=Interactions_modding&oldid=20307)"

[Category](https://ck3.paradoxwikis.com/Special:Categories "Special:Categories"):

- [Modding](https://ck3.paradoxwikis.com/Category:Modding "Category:Modding")