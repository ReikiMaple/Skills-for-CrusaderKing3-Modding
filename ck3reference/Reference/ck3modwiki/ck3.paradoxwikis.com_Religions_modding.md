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

# Religions modding

From CK3 Wiki

[Jump to navigation](https://ck3.paradoxwikis.com/Religions_modding#mw-head) [Jump to search](https://ck3.paradoxwikis.com/Religions_modding#searchInput)

Please help with verifying or updating older sections of this article.

At least some were last verified for [version](https://ck3.paradoxwikis.com/CK3_Wiki:Versioning "CK3 Wiki:Versioning") 1.0.

This article is for the PC version of Crusader Kings 3 only.

New religions can easily be added into the game using the highly modular design which the game offers.

## Contents

- [1Religion family](https://ck3.paradoxwikis.com/Religions_modding#Religion_family)
- [2Religion structure](https://ck3.paradoxwikis.com/Religions_modding#Religion_structure)
- [3Faiths](https://ck3.paradoxwikis.com/Religions_modding#Faiths)
- [4Localization](https://ck3.paradoxwikis.com/Religions_modding#Localization)
- [5Graphics](https://ck3.paradoxwikis.com/Religions_modding#Graphics)
- [6Holy sites](https://ck3.paradoxwikis.com/Religions_modding#Holy_sites)
- [7Tenet ID](https://ck3.paradoxwikis.com/Religions_modding#Tenet_ID)

## Religion family\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Religions_modding&veaction=edit&section=1 "Edit section: Religion family") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Religions_modding&action=edit&section=1 "Edit section: Religion family")\]

Each religion belongs to a family. The three vanilla families are Abrahamic, Eastern and Pagan. For instance:

- Christianity and Islam are part of the Abrahamic Family
- Slavism and Tengrism are part of the Pagan Family

Religion families are located in _/common/religion/religion\_families_. The religion family is defined as a tag with an alphanumerical ID. For example, the Abrahamic family is defined as follows:

```
rf_abrahamic = {
	graphical_faith = "orthodox_gfx"
	hostility_doctrine = abrahamic_hostility_doctrine
	doctrine_background_icon = core_tenet_banner_christian.dds
}
```

Below is a list of all parameters that can be set for religion families.

| Attribute | Type | Description | Example |
| --- | --- | --- | --- |
| name | localization key | If not set will use the object key as localization key | name = name\_of\_the\_family |
| is\_pagan | boolean | Specifies if the group is pagan or not (default value is yes) | is\_pagan = no |
| graphical\_faith | gfx | All religions in this family default to this 3D model (currently used for temple assets). Order of precedence is the lowest level scripted in: faith > religion > family. | graphical\_faith = catholic\_gfx |
| piety\_icon\_group | gfx | All religions in this family default to this set of piety icons. Order of precedence is the lowest level scripted in: faith > religion > family. | piety\_icon\_group = christian |
| doctrine\_background\_icon | gfx | All religions in this family default to this doctrine background icon. Order of precedence is the lowest level scripted in: faith > religion > family. | doctrine\_background\_icon = core\_tenet\_banner\_christian.dds |
| hostility\_doctrine | doctrine | INTERFACE ONLY: Use this doctrine when displaying hostility information for the whole religious family (if not scripted, then show no information) | hostility\_doctrine = christian\_hostility\_doctrine |

## Religion structure\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Religions_modding&veaction=edit&section=2 "Edit section: Religion structure") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Religions_modding&action=edit&section=2 "Edit section: Religion structure")\]

Religions are located in the _/common/religion/religions_ folder. Each religion is defined within a file, and the faiths that belong to it are defined within that definition. The religion is defined as a tag with an alphanumerical ID. Here is an example of a fictional religion (localization and faiths are addressed below):

```
sea_cults = {
	family = rf_pagan
	graphical_faith = pagan_gfx

	doctrine = pagan_hostility_doctrine

	pagan_roots = yes

	#Main Group
	doctrine = doctrine_spiritual_head
	doctrine = doctrine_gender_male_dominated
	doctrine = doctrine_pluralism_fundamentalist
	doctrine = doctrine_theocracy_lay_clergy
	doctrine = doctrine_pilgrimage_encouraged
	doctrine = doctrine_funeral_bewailment

	#Marriage
	doctrine = doctrine_concubines
	doctrine = doctrine_divorce_allowed
	doctrine = doctrine_bastardry_legitimization
	doctrine = doctrine_consanguinity_cousins

	#Crimes
	doctrine = doctrine_homosexuality_shunned
	doctrine = doctrine_adultery_men_shunned
	doctrine = doctrine_adultery_women_accepted
	doctrine = doctrine_kinslaying_accepted
	doctrine = doctrine_deviancy_accepted
	doctrine = doctrine_witchcraft_crime

	#Clerical Functions
	doctrine = doctrine_clerical_function_taxation
	doctrine = doctrine_clerical_gender_either
	doctrine = doctrine_clerical_marriage_allowed
	doctrine = doctrine_clerical_succession_spiritual_appointment

	traits = {
		virtues = { brave lunatic_1 wrathful }
		sins = { patient content shy }
	}

	reserved_male_names = {
		Lobbo Lobbeu Lobst Lob Lobr Loabstr Lobb Lub Leurbo
	}
	reserved_female_names = {
		Lobba Lobbelia Lobsta Loba Lober Loabstra Lobba Lubas Leurbos
	}
	holy_order_names = {
		{ name = "holy_order_claw_bearers" }
		{ name = "holy_order_clackers" }
		{ name = "holy_order_servants_of_the_lobbo" }
		{ name = "holy_order_the_pile" }
	}
	holy_order_maa = { huscarl }
	custom_faith_icons = { custom_faith_1 custom_faith_2 custom_faith_3 custom_faith_4 custom_faith_5 custom_faith_6 custom_faith_7 custom_faith_8 custom_faith_9 custom_faith_10 lobbist lobbist_reformed }

	localization = {
		...
	}

	faiths = {
		...
	}
}
```

Below is a list of all parameters that can be set for religions.

| Attribute | Type | Description | Example |
| --- | --- | --- | --- |
| family | religion family | What religion family the religion belongs to | family = family\_name |
| graphical\_faith | gfx | All faiths in this religion default to this 3D model (currently used for temple assets). Order of precedence is the lowest level scripted in: faith > religion > family. | graphical\_faith = catholic\_gfx |
| piety\_icon\_group | gfx | All faiths in this religion default to this set of piety icons. Order of precedence is the lowest level scripted in: faith > religion > family. | piety\_icon\_group = christian |
| doctrine\_background\_icon | image file | All faiths in this religion default to this doctrine background icon. Order of precedence is the lowest level scripted in: faith > religion > family. | doctrine\_background\_icon = core\_tenet\_banner\_christian.dds |
| pagan\_roots | boolean | If yes, then faiths without the unreformed doctrine are considered reformed by the interface. | pagan\_roots = yes |
| doctrine | doctrine | Doctrines defined in a religion will be applied to all faiths within it. This is only at game start; it is purely for script convenience, and would be equivalent to putting the doctrine in all the faiths. It can be overridden by putting a different doctrine in the group in the specific faith. Note that doctrines that allow more than one pick can **not** be defined on a religion level, as there's no obvious override system that would work then. Doctrines cannot be defined after the faiths section. | doctrine = doctrine\_spiritual\_head |
| traits | clause | Defines which traits are considered virtues and sins by the religion. Notes on virtues and sins: List traits that are virtues for all followers. Trait groups also work. If more than one trait in a group is defined (or the group itself), only the first will be shown in the UI<br>sins = { ... } # (sins)<br># Virtues and sins give an opinion bonus/penalty (see VIRTUOUS\_TRAIT and SINFUL\_TRAIT defines). For that it is the "viewer's" faith that matters.<br># E.g. if generous is a christian virtue, all christian characters will think more highly of all others with that trait, even if the others are not christian.<br># Holders of the traits will also get the virtue\_owner\_modifier/sin\_owner\_modifier for each matching trait.<br># Virtues and sins can optionally have a multiplier to scale the effects (default is 1):<br>virtues = { brave = 0.5 } # scales both the opinion effect and the modifier<br># And they can specify a custom modifier (default is virtue\_owner\_modifier/sin\_owner\_modifier):<br>sins = { stubborn = { monthly\_prestige = -0.1 } }<br># When using a custom modifier you can specify a scale as well (default is 1):<br>sins = { stubborn = { monthly\_prestige = -0.1 scale = 2 } } # scales both the opinion effect and the modifier | virtues = { brave generous } sins = { stubborn = { monthly\_prestige = -0.1 scale = 2 } } |
| reserved\_male\_names | list<string> | Names listed here will be applied to all faiths that don't define reserved\_male\_names themselves. These names can be applied to newborn males when selecting a religion-based name. | reserved\_male\_names = { Rodrigo Johan Paradoxus } |
| reserved\_female\_names | list<string> | Same as reserved\_male\_names, but applied to female characters instead. |  |
| custom\_faith\_icons | list<gfx> | When creating a custom faith, these will be the available icons. Path is "gfx/interface/icons/religion/%s.dds", where %s is the name. Also needs a text icon | custom\_faith\_icons = { custom\_faith\_1 custom\_faith\_2 custom\_faith\_3 } |
| localization | list<localization keys> | See localization inside faiths below. |  |
| holy\_order\_names | list<clause> | Names and CoAs that can be used by holy orders of this religion. These are used if there are none available for the faith. If there are none left here, it uses "holy\_order\_default" as name and a randomly generated CoA instead. | ```<br>holy_order_names = {<br>		{ name = "holy_order_name1" coat_of_arms = "holy_order_coa1" }<br>		{ name = "holy_order_name2" coat_of_arms = "holy_order_coa2" }<br>		...<br>	}<br>``` |
| holy\_order\_maa | list<regiment type> | Men-At-Arms types mostly used for holy orders. The culture of the headquarters of the holy order must have unlocked the required innovation. (It will use the last available type in the list.) | holy\_order\_maa = { huscarl } |
| faiths | list<Faiths> | See below |  |

## Faiths\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Religions_modding&veaction=edit&section=3 "Edit section: Faiths") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Religions_modding&action=edit&section=3 "Edit section: Faiths")\]

Faiths are defined within the faith clause of a religion. They can overwrite default doctrines and graphics set for the whole religion. Here is an example of a fictional faith within the religion defined above.

```
faiths = {
	lobbist = {
		color = { 0.2 0.2 0.9 }
		icon = lobbist
		reformed_icon = lobbist_reformed
		holy_site = uppsala
		holy_site = lejre
		holy_site = paderborn
		holy_site = zeeland
		holy_site = ranaheim

		doctrine = unreformed_faith_doctrine
		doctrine = tenet_warmonger
		doctrine = tenet_human_sacrifice
		doctrine = tenet_ancestor_worship

	}
}
```

Below is a list of all parameters that can be set for faiths.

| Attribute | Type | Description | Example |
| --- | --- | --- | --- |
| color | rgb |  | color = { 0.2 0.2 0.9 } |
| icon | gfx | If you want to use another faith's icon | icon = bosnian\_church |
| graphical\_faith | gfx | This faith (and custom faiths based on this faith) use this 3D model (currently used for temple assets). Order of precedence is the lowest level scripted in: faith > religion > family. | graphical\_faith = catholic\_gfx |
| piety\_icon\_group | gfx | This faith (and custom faiths based on this faith) use this set of piety icons. Order of precedence is the lowest level scripted in: faith > religion > family. | piety\_icon\_group = christian |
| doctrine\_background\_icon | gfx | This faith (and custom faiths based on this faith) use this doctrine background icon. Order of precedence is the lowest level scripted in: faith > religion > family. |  |
| religious\_head | title | What title should be this faith's religious head. If not set, will not have a religious head (unless created elsewhere in script) | religious\_head = d\_coptic\_papacy |
| holy\_site | holy site | Holy site, as defined in the holy\_site folder. You can add any number of these | holy\_site = jerusalem |
| doctrine | doctrine |  |  |
| reserved\_male\_names/reserved\_female\_names | list<string> |  |  |
| localization |  |  |  |

## Localization\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Religions_modding&veaction=edit&section=4 "Edit section: Localization") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Religions_modding&action=edit&section=4 "Edit section: Localization")\]

The localization clause in both faiths and religions provides key-value pairs for localization. However, this clause does not include object localization for the religion/faith itself and its basic properties. The following localization keys also need defining:

- <religion/faith\_name>
- <religion/faith\_name>\_adj
- <religion/faith\_name>\_adherent
- <religion/faith\_name>\_adherent\_plural
- <religion/faith\_name>\_desc

Below is a list of keys that need to be paired for localization. Although you can use this as a reference, it is also possible to simply copy and paste this list from a vanilla file and add your own keys where needed. Although many items in the list are not relevant to many religions/faiths, they can simply be assigned to a key used by another more relevant item. (e.g. FertilityGodName in Christianity is given as "$christianity\_high\_god\_name$" in the localization file):

- HighGodName
- HighGodNamePossessive
- HighGodNameSheHe
- HighGodHerselfHimself
- HighGodHerHis
- HighGodNameAlternate
- HighGodNameAlternatePossessive
- CreatorName
- CreatorNamePossessive
- CreatorSheHe
- CreatorHerHis
- CreatorHerHim
- HealthGodName
- HealthGodNamePossessive
- HealthGodSheHe
- HealthGodHerHis
- HealthGodHerHim
- FertilityGodName
- FertilityGodNamePossessive
- FertilityGodSheHe
- FertilityGodHerHis
- FertilityGodHerHim
- WealthGodName
- WealthGodNamePossessive
- WealthGodSheHe
- WealthGodHerHis
- WealthGodHerHim
- HouseholdGodName
- HouseholdGodNamePossessive
- HouseholdGodSheHe
- HouseholdGodHerHis
- HouseholdGodHerHim
- FateGodName
- FateGodNamePossessive
- FateGodSheHe
- FateGodHerHis
- FateGodHerHim
- KnowledgeGodName
- KnowledgeGodNamePossessive
- KnowledgeGodSheHe
- KnowledgeGodHerHis
- KnowledgeGodHerHim
- WarGodName
- WarGodNamePossessive
- WarGodSheHe
- WarGodHerHis
- WarGodHerHim
- TricksterGodName
- TricksterGodNamePossessive
- TricksterGodSheHe
- TricksterGodHerHis
- TricksterGodHerHim
- NightGodName
- NightGodNamePossessive
- NightGodSheHe
- NightGodHerHis
- NightGodHerHim
- WaterGodName
- WaterGodNamePossessive
- WaterGodSheHe
- WaterGodHerHis
- WaterGodHerHim
- PantheonTerm
- PantheonTermHasHave
- GoodGodNames (list)
- DevilName
- DevilNamePossessive
- DevilSheHe
- DevilHerHis
- DevilHerselfHimself
- EvilGodNames (list)
- HouseOfWorship
- HouseOfWorshipPlural
- ReligiousSymbol
- ReligiousText
- ReligiousHeadName
- ReligiousHeadTitleName
- DevoteeMale
- DevoteeMalePlural
- DevoteeFemalePlural
- DevoteeNeuter
- DevoteeNeuterPlural
- PriestMale
- PriestMalePlural
- PriestFemale
- PriestFemalePlural
- PriestNeuter
- PriestNeuterPlural
- AltPriestTermPlural
- BishopMale
- BishopMalePlural
- BishopFemale
- BishopFemalePlural
- BishopNeuter
- BishopNeuterPlural
- DivineRealm
- PositiveAfterLife
- NegativeAfterLife
- DeathDeityName
- DeathDeityNamePossessive
- DeathDeitySheHe
- DeathDeityHerHis
- WitchGodName
- WitchGodHerHis
- WitchGodSheHe
- WitchGodHerHim
- WitchGodMistressMaster
- WitchGodMotherFather
- GHWName
- GHWNamePlural

## Graphics\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Religions_modding&veaction=edit&section=5 "Edit section: Graphics") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Religions_modding&action=edit&section=5 "Edit section: Graphics")\]

No graphical modding is required to create a religion or faith, since there is an abundance of icons in the vanilla game, either in use by other religions or reserved for custom faiths. However, adding a new icon is very simple, if you feel that none of the vanilla icons are fitting for your religion. In the path _/gfx/interface/icons/faith_, create a new 100x100 dds file. The name of the file is how the icon is referred to in the religion file. (e.g. icon = lobbist will refer to /gfx/interface/icons/faith/lobbist.dds).

## Holy sites\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Religions_modding&veaction=edit&section=6 "Edit section: Holy sites") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Religions_modding&action=edit&section=6 "Edit section: Holy sites")\]

_See also: [Holy site ID](https://ck3.paradoxwikis.com/Holy_site_ID "Holy site ID")_

Custom holy sites can be added in a text document in the _/common/religion/holy\_sites_ folder. Each site is identified by a name, and contains information on the location of the site and the benefits (or potentially negatives) it brings.

```
jerusalem = {
	county = c_jerusalem

	character_modifier = {
		monthly_piety_gain_mult = 0.2
	}
	flag = jerusalem_conversion_bonus # +20% County Conversion
}
```

Below are the attributes which can be assigned to a holy site. Only the county is necessary.

| Attribute | Type | Description | Example |
| --- | --- | --- | --- |
| county | title | The county in which the holy site is located | county = c\_jerusalem |
| barony | title | The barony in which the holy site is located | barony = b\_vaticano |
| character modifier | modifier | Applied to all characters of any faith with this holy site when the holder of the barony is of their faith | character\_modifier = {<br>monthly\_piety\_gain\_mult = 0.2<br>} |
| flag | flag |  | flag = jerusalem\_conversion\_bonus |

Holy sites also require the following keys in localization:

- holy\_site\_<name>\_name
- holy\_site\_<name>\_effect\_name
- holy\_site\_<name>\_effects

```
 holy_site_jerusalem_name:0 "Jerusalem"
 holy_site_jerusalem_effect_name:0 "From [holy_site|E] #weak ($holy_site_jerusalem_name$)#!"
 holy_site_jerusalem_effects:0 "County Conversion Speed: #P +20%#!"
```

## Tenet ID\[ [edit](https://ck3.paradoxwikis.com/index.php?title=Religions_modding&veaction=edit&section=7 "Edit section: Tenet ID") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=Religions_modding&action=edit&section=7 "Edit section: Tenet ID")\]

Each tenet has an internal ID used to reference it within the game files. In general, to get the tenet ID from its name:

1. Take the non-variant name (i.e. non-faith specific)
2. Turn all upper case letters into lower case (`A...Z->a...z`)
3. Replace all spaces (``) with underscores (`_`)
4. Add `tenet_` to the beginning

Tenets that do not fit the pattern above have been listed below:

| Name | Tenet ID |
| --- | --- |
| [Auspicious Birthright](https://ck3.paradoxwikis.com/Auspicious_Birthright "Auspicious Birthright") | tenet\_mystical\_birthright |
| [Ritual Suicide](https://ck3.paradoxwikis.com/Ritual_Suicide "Ritual Suicide") | tenet\_consolamentum |
| [Ecclesiarchy](https://ck3.paradoxwikis.com/Ecclesiarchy "Ecclesiarchy") | tenet\_pentarchy |
| [Religious Law](https://ck3.paradoxwikis.com/Religious_Law "Religious Law") | tenet\_religious\_legal\_pronouncements |
| [Sacred Lies](https://ck3.paradoxwikis.com/Sacred_Lies "Sacred Lies") | tenet\_sacred\_shadows |
| [Sanctioned False Conversions](https://ck3.paradoxwikis.com/Sanctioned_False_Conversions "Sanctioned False Conversions") | tenet\_false\_conversion\_sanction |
| [Struggle and Submission](https://ck3.paradoxwikis.com/Struggle_and_Submission "Struggle and Submission") | tenet\_struggle\_submission |
| [Syncretic Folk Traditions](https://ck3.paradoxwikis.com/Syncretic_Folk_Traditions "Syncretic Folk Traditions") | tenet\_unreformed\_syncretism |

**[Modding](https://ck3.paradoxwikis.com/Modding "Modding")**

|     |     |
| --- | --- |
| Documentation | [Scripting](https://ck3.paradoxwikis.com/Scripting "Scripting") • [Scopes](https://ck3.paradoxwikis.com/Scopes "Scopes") • [Effects](https://ck3.paradoxwikis.com/Effects "Effects") • [Triggers](https://ck3.paradoxwikis.com/Triggers "Triggers") • [Variables](https://ck3.paradoxwikis.com/Variables "Variables") • [Modifiers](https://ck3.paradoxwikis.com/Modifier_list "Modifier list") |

|     |     |
| --- | --- |
| Scripting | [AI](https://ck3.paradoxwikis.com/AI_modding "AI modding") • [Bookmarks](https://ck3.paradoxwikis.com/Bookmarks_modding "Bookmarks modding") • [Characters](https://ck3.paradoxwikis.com/Characters_modding "Characters modding") • [Commands](https://ck3.paradoxwikis.com/Commands "Commands") • [Council](https://ck3.paradoxwikis.com/Council_modding "Council modding") • [Culture](https://ck3.paradoxwikis.com/Culture_modding "Culture modding") • [Decisions](https://ck3.paradoxwikis.com/Decisions_modding "Decisions modding") • [Dynasties](https://ck3.paradoxwikis.com/Dynasties_modding "Dynasties modding") • [Events](https://ck3.paradoxwikis.com/Event_modding "Event modding") • [Governments](https://ck3.paradoxwikis.com/Governments_modding "Governments modding") • [History](https://ck3.paradoxwikis.com/History_modding "History modding") • [Holdings](https://ck3.paradoxwikis.com/Holdings_modding "Holdings modding") • [Lifestyles](https://ck3.paradoxwikis.com/Lifestyles_modding "Lifestyles modding") • [Regiments](https://ck3.paradoxwikis.com/Regiments_modding "Regiments modding") • Religions • [Script Values](https://ck3.paradoxwikis.com/Script_values "Script values") • [Story cycles](https://ck3.paradoxwikis.com/Story_cycles_modding "Story cycles modding") • [Struggles](https://ck3.paradoxwikis.com/Struggle_modding "Struggle modding") • [Titles](https://ck3.paradoxwikis.com/Title_modding "Title modding") • [Traits](https://ck3.paradoxwikis.com/Trait_modding "Trait modding") |

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

Retrieved from " [https://ck3.paradoxwikis.com/index.php?title=Religions\_modding&oldid=26712](https://ck3.paradoxwikis.com/index.php?title=Religions_modding&oldid=26712)"

[Categories](https://ck3.paradoxwikis.com/Special:Categories "Special:Categories"):

- [Potentially outdated](https://ck3.paradoxwikis.com/Category:Potentially_outdated "Category:Potentially outdated")
- [1.0](https://ck3.paradoxwikis.com/Category:1.0 "Category:1.0")
- [Modding](https://ck3.paradoxwikis.com/Category:Modding "Category:Modding")