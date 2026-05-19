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

# 3D models

From CK3 Wiki

[Jump to navigation](https://ck3.paradoxwikis.com/3D_models#mw-head) [Jump to search](https://ck3.paradoxwikis.com/3D_models#searchInput)

This article is [timeless](https://ck3.paradoxwikis.com/Category:Timeless "Category:Timeless") and should be accurate for any version of the game.

Crusader Kings III uses 3d models to represent objects in the game such as portraits, units and holdings, as well as map objects such as trees. This guide is intended to help CK3 modders with some existing knowledge of 3d modelling and materials. This guide is similar to other 3d modelling guides for Clausewitz like Imperator: Rome.
To create a 3d model, you will need modelling software like Autodesk Maya or Blender. You will also need an addon to import and export Crusader Kings III models. To create a texture, you will need image-editing software like Adobe Photoshop or GIMP with an addon to import and export DDS textures.

## Contents

- [1Overview](https://ck3.paradoxwikis.com/3D_models#Overview)
- [2Tutorial: Setup](https://ck3.paradoxwikis.com/3D_models#Tutorial:_Setup)
  - [2.1Tools](https://ck3.paradoxwikis.com/3D_models#Tools)
  - [2.2Setup Clausewitz Maya exporter](https://ck3.paradoxwikis.com/3D_models#Setup_Clausewitz_Maya_exporter)
- [3Making the Model](https://ck3.paradoxwikis.com/3D_models#Making_the_Model)
  - [3.1Preparing Maya/Blender 3d model](https://ck3.paradoxwikis.com/3D_models#Preparing_Maya/Blender_3d_model)
    - [3.1.1UVs](https://ck3.paradoxwikis.com/3D_models#UVs)
    - [3.1.2Issues with UV maps](https://ck3.paradoxwikis.com/3D_models#Issues_with_UV_maps)
    - [3.1.3Broken normals](https://ck3.paradoxwikis.com/3D_models#Broken_normals)
  - [3.2Textures](https://ck3.paradoxwikis.com/3D_models#Textures)
    - [3.2.1Formats](https://ck3.paradoxwikis.com/3D_models#Formats)
      - [3.2.1.1Icons](https://ck3.paradoxwikis.com/3D_models#Icons)
      - [3.2.1.2Illustrations & Backgrounds](https://ck3.paradoxwikis.com/3D_models#Illustrations_&_Backgrounds)
      - [3.2.1.3Clothing Textures](https://ck3.paradoxwikis.com/3D_models#Clothing_Textures)
      - [3.2.1.4Building Textures](https://ck3.paradoxwikis.com/3D_models#Building_Textures)
    - [3.2.2Channel packing](https://ck3.paradoxwikis.com/3D_models#Channel_packing)
      - [3.2.2.1Gimp](https://ck3.paradoxwikis.com/3D_models#Gimp)
- [4Tutorial: Getting them on the map](https://ck3.paradoxwikis.com/3D_models#Tutorial:_Getting_them_on_the_map)
  - [4.1Holdings](https://ck3.paradoxwikis.com/3D_models#Holdings)

## Overview\[ [edit](https://ck3.paradoxwikis.com/index.php?title=3D_models&veaction=edit&section=1 "Edit section: Overview") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=3D_models&action=edit&section=1 "Edit section: Overview")\]

All models and their respective textures and animations can be found in /Crusader Kings III/game/gfx/models/

A typical model will have the following files:

- **<model>.mesh** \- The 3d model itself.
- **<model>.asset** \- The script adding the model to the game.
- **<model>\_diffuse.dds** \- The diffuse texture for the model.
- **<model>\_normal.dds** \- A normal map texture.
- **<model>\_properties.dds** \- A joint texture with specular, metalness and roughness.

More textures for other 3d models include:

- **<model>\_unique.dds** \- Used with the standard\_atlas shader. The B channel is the models’ ambient occlusion texture.

## Tutorial: Setup\[ [edit](https://ck3.paradoxwikis.com/index.php?title=3D_models&veaction=edit&section=2 "Edit section: Tutorial: Setup") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=3D_models&action=edit&section=2 "Edit section: Tutorial: Setup")\]

### Tools\[ [edit](https://ck3.paradoxwikis.com/index.php?title=3D_models&veaction=edit&section=3 "Edit section: Tools") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=3D_models&action=edit&section=3 "Edit section: Tools")\]

- Autodesk Maya. A program used to create 3d models and animation. Needs the Clausewitz Maya Exporter installed.
- [Clausewitz Maya Exporter](https://forum.paradoxplaza.com/forum/threads/information-and-faq.924764/). A Maya plugin from Paradox. Setup models based on installed games and exports model and asset. Installation instructions linked in the forum post and below.
- [Blender](https://www.blender.org/download/). A free program used to create 3d models and animation.
- [IO PDX Mesh addon](https://github.com/ross-g/io_pdx_mesh). Addon that can be installed to Blender or Autodesk Maya. Setup models from compatible games. Installation instructions on their page.

### Setup Clausewitz Maya exporter\[ [edit](https://ck3.paradoxwikis.com/index.php?title=3D_models&veaction=edit&section=4 "Edit section: Setup Clausewitz Maya exporter") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=3D_models&action=edit&section=4 "Edit section: Setup Clausewitz Maya exporter")\]

There is a full setup guide for the [exporters](https://ck3.paradoxwikis.com/Exporters "Exporters"). The below guide is shortened.

To setup CK3 for the exporter, open the clausewitz.settings file using a code editor, edit the folder paths and then save. The folder paths for CK3 are as follows:

- "name": "CrusaderKingsIII"
- "path": "C:/SteamLibrary/steamaps/common/Crusader Kings III/game/tools"
- "export\_path": "Your personal mod’s folder"
- "target\_exe": "C:/SteamLibrary/steamaps/common/Crusader Kings III/binaries/ck3.exe"

Notes:

- Your mod’s gfx/models folder can be anywhere on your C drive. You can choose to edit the settings for every mod you edit, or use one folder and copy your models from there to your mod.
- The / slash (forward slash) is important, Windows Explorer uses \ (backwards slash). If you copy from Windows Explorer, you will need to edit the folder paths to use /.
- The name must be one word, no spaces.

## Making the Model\[ [edit](https://ck3.paradoxwikis.com/index.php?title=3D_models&veaction=edit&section=5 "Edit section: Making the Model") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=3D_models&action=edit&section=5 "Edit section: Making the Model")\]

### Preparing Maya/Blender 3d model\[ [edit](https://ck3.paradoxwikis.com/index.php?title=3D_models&veaction=edit&section=6 "Edit section: Preparing Maya/Blender 3d model") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=3D_models&action=edit&section=6 "Edit section: Preparing Maya/Blender 3d model")\]

#### UVs\[ [edit](https://ck3.paradoxwikis.com/index.php?title=3D_models&veaction=edit&section=7 "Edit section: UVs") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=3D_models&action=edit&section=7 "Edit section: UVs")\]

Order of UV maps for the standard\_atlas shader:

1. **map1** \- uv mapped to AO "<model>\_unique"
2. **map2** \- uv mapped material atlas

#### Issues with UV maps\[ [edit](https://ck3.paradoxwikis.com/index.php?title=3D_models&veaction=edit&section=8 "Edit section: Issues with UV maps") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=3D_models&action=edit&section=8 "Edit section: Issues with UV maps")\]

This can catch you off guard when creating your model, map1 must be above map2, map1 must be the default uv set in Maya. If you’re importing the model from Blender as a .dae file, the uv maps must be in the correct order in Blender too.
If your uvs are not in the correct order, then use this method to rearrange them. I do not know a method to delete the default uv set in Maya.
The issue is that map1 is mapped to your material atlas.

1. UV - UV Set Editor. Copy map1.
2. Select map2 in the UV Set Editor.
3. UV - UV Editor. Then in the UV Editor, UV Sets – Copy UVs to UV Set. Choose map1.
4. In the UV Set Editor delete map2.
5. Rename UVSet1 (originally copied from map1 in step 1) to “map2”.
6. Select map1 and click Update.

#### Broken normals\[ [edit](https://ck3.paradoxwikis.com/index.php?title=3D_models&veaction=edit&section=9 "Edit section: Broken normals") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=3D_models&action=edit&section=9 "Edit section: Broken normals")\]

In Maya, use the Mesh Cleanup tool (with default settings) to solve `Error! Mesh contains broken normals, tangents and/or bitangents.`

### Textures\[ [edit](https://ck3.paradoxwikis.com/index.php?title=3D_models&veaction=edit&section=10 "Edit section: Textures") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=3D_models&action=edit&section=10 "Edit section: Textures")\]

#### Formats\[ [edit](https://ck3.paradoxwikis.com/index.php?title=3D_models&veaction=edit&section=11 "Edit section: Formats") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=3D_models&action=edit&section=11 "Edit section: Formats")\]

These are most of the Formats for Textures in Ck3 (Kudos to "@Sparc \| Princes of Darkness Mod" from the Ck3 Modding Coop) (Dimensions may have increased for some of these, but the smaller dimensions still work):

##### Icons\[ [edit](https://ck3.paradoxwikis.com/index.php?title=3D_models&veaction=edit&section=12 "Edit section: Icons") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=3D_models&action=edit&section=12 "Edit section: Icons")\]

| **Type** | **Dimensions** | **Format & Minimaps** |
| --- | --- | --- |
| Religion Icons | 100×100 | `32bit-A8R8G8B8` (No minimaps) |
| Coat of Arms (Colored Emblems) | 512×512 | `BC3/DXT5` (Minimaps) |
| Coat of Arms (Patterns) | 256×256 | `DXT1` (Minimaps) |
| Regiment Type Icons | 120×120 | `A8R8G8B8` (No minimaps) |
| Focus Icons | 140×140 | `A8R8G8B8` (No minimaps) |
| Faith Doctrine Tenet Icons | 260×400 | `DXT5` (No minimaps) |
| Faith Doctrine Icon Banners | 260×400 | `A8R8G8B8` (No minimaps) |
| Culture Innovations | 90×60 | `A8R8G8B8` (No minimaps) |
| Character Interactions | 120×120 | `A8R8G8B8` (No minimaps) |
| Building Type Icons | 150×130 | `A8R8G8B8` (No minimaps) |
| Trait Icons | 120×120 | `A8R8G8B8` (Minimaps) |
| Lifestyle Perks | 120×120 | `A8R8G8B8` (Minimaps) |
| Lifestyle Backgrounds | 608×1546 | `DXT5` (No minimaps) |
| Lifestyle Tree Backgrounds | 347×812 | `DXT5` (No minimaps) |
| Legacy Tracks | 4216×368 | `DXT5` (No minimaps) |
| Event Type Icons | 148×148 | _(Format not specified)_ |

##### Illustrations & Backgrounds\[ [edit](https://ck3.paradoxwikis.com/index.php?title=3D_models&veaction=edit&section=13 "Edit section: Illustrations & Backgrounds") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=3D_models&action=edit&section=13 "Edit section: Illustrations & Backgrounds")\]

| **Type** | **Dimensions** | **Format & Minimaps** |
| --- | --- | --- |
| Loading Screens | 3840×2160 | `DXT1` (No minimaps) |
| Event Scenes | 1592×848 | `DXT1` (No minimaps) |
| Event Scenes (Frontend) | 1592×828 | `DXT1` (No minimaps) |
| Decisions | 1100×440 | `DXT1` (No minimaps) |
| Council | 844×844 | `DXT1` (No minimaps) |
| Character View | 1539×849 | `DXT1` (No minimaps) |
| Holding Types | 2560×1168 | `DXT1` (No minimaps) |
| Terrain Types | 1200×600 | `DXT1` (No minimaps) |
| Men-at-Arms (Small) | 160×160 | `DXT1` (No minimaps) |
| Men-at-Arms (Big) | 680×400 | `DXT1` (No minimaps) |
| Bookmarks | 1920×1080 | `DXT5` (No minimaps) |

##### Clothing Textures\[ [edit](https://ck3.paradoxwikis.com/index.php?title=3D_models&veaction=edit&section=14 "Edit section: Clothing Textures") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=3D_models&action=edit&section=14 "Edit section: Clothing Textures")\]

| **Type** | **Dimensions** | **Format & Minimaps** |
| --- | --- | --- |
| Pattern Properties | 512×512 | `DXT5` (Minimaps) |
| Pattern Normal | 512×512 | `DXT5` (Minimaps) |

##### Building Textures\[ [edit](https://ck3.paradoxwikis.com/index.php?title=3D_models&veaction=edit&section=15 "Edit section: Building Textures") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=3D_models&action=edit&section=15 "Edit section: Building Textures")\]

All Building Textures are 1024×1024, with DXT5 and Minimaps.

#### Channel packing\[ [edit](https://ck3.paradoxwikis.com/index.php?title=3D_models&veaction=edit&section=16 "Edit section: Channel packing") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=3D_models&action=edit&section=16 "Edit section: Channel packing")\]

Channel packing is a way to combine different image data—like colors or textures—into one file by splitting them into its color channels (red, green, blue, or alpha), saving space and improving efficiency.

This is how most Vanilla Textures are packed (Kudos to the [Stellaris Modding Wiki](https://stellaris.paradoxwikis.com/Maya_exporter#Exporting_textures.2F "stella:Maya exporter")):

| File | Channel | Notes |
| --- | --- | --- |
| R | G | B | A |
| \[texturename\]\_diffuse.dds | DiffuseR | DiffuseG | DiffuseB | OpacityR | OpacityGB are ignored |
| \[texturename\]\_normal.dds | NormalR | NormalR | EmissiveR | NormalG | NormalB is ignored.<br>EmissiveGB are ignored |
| \[texturename\]\_specular.dds | Mask (various) | SpecularB | MetalB | GlossB | ColorRGB are ignored<br>SpecularRG are ignored.<br>Gloss RG are ignored. |

##### Gimp\[ [edit](https://ck3.paradoxwikis.com/index.php?title=3D_models&veaction=edit&section=17 "Edit section: Gimp") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=3D_models&action=edit&section=17 "Edit section: Gimp")\]

If you want to create for example a new normal map in gimp, you would do the following:

1. Import your Normal texture into Gimp.
2. Make sure you have no active selection, then go to the menu and click Colors > Components > Decompose
3. In the Decompose menu, leave everything as is and click ok. Gimp will now split your Image's Color channels, and you can then edit them as you would edit layers.
4. After this, you go back to Colors>Components>Compose. In the Compose menu, you select RGBA as Color model and can then decide which layer should represent which channel. In our example, you would set Red to the Red Layer, Green to the Red layer, Blue to a Mask Value of 0 and Alpha to the Green Layer.
5. After you click Ok, Gimp will compose the Image for you, and you should be left with a yellowish Normal map. Which you can export to \[texturename\]\_normal.dds with BC3/DXT5 Compression and generated mipmaps.

## Tutorial: Getting them on the map\[ [edit](https://ck3.paradoxwikis.com/index.php?title=3D_models&veaction=edit&section=18 "Edit section: Tutorial: Getting them on the map") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=3D_models&action=edit&section=18 "Edit section: Tutorial: Getting them on the map")\]

You'll want to make building models appear in the game; this requires editing a few other files.

First off, the asset file for a building must contain an entity-block and a pdxmesh-block, the former essentially containing just a reference to the latter. You'll want to reference either the mesh or the entity in different places.

### Holdings\[ [edit](https://ck3.paradoxwikis.com/index.php?title=3D_models&veaction=edit&section=19 "Edit section: Holdings") \| [edit source](https://ck3.paradoxwikis.com/index.php?title=3D_models&action=edit&section=19 "Edit section: Holdings")\]

To make holding buildings for your modded religion or culture, you must first make sure they are considered as entities to be placed on the map: you will need to reference them by editing the vanilla file `all_buildings.asset`, under `gfx/models/buildings`. It is unclear what all the settings do here, but you can just follow the pattern and add a locator and attach-block for each of your new holding models, e.g. like so:

```
locator = { name = "pos_11_a" position = { @[gap *  6.5] 000 @[gap * -1.5 ] } }
locator = { name = "pos_11_b" position = { @[gap *  6.5] 000 @[gap * -0.5 ] } }
locator = { name = "pos_11_c" position = { @[gap *  6.5] 000 @[gap *  0.5 ] } }
locator = { name = "pos_11_d" position = { @[gap *  6.5] 000 @[gap *  1.5 ] } }
attach = {         "pos_11_a" = "building_[mymod]_city_01_entity" }
attach = {         "pos_11_b" = "building_[mymod]_city_02_entity" }
attach = {         "pos_11_c" = "building_[mymod]_temple_01_entity" }
attach = {         "pos_11_d" = "building_[mymod]_temple_02_entity" }
```

Now, for the second part there's a distinction between temple holdings and castle/city holdings. The choice of temple holding is primarily determined by a religion, and for castles and cities it is culture. In order to have a culture make use of your new city and castle holdings, you define a new `graphical_culture` for your culture. This is just a tag and does not need to be declared anywhere; just put e.g. `[mymod]_building_gfx` in the `graphical_cultures` block at the top of your culture definition. Religions, on the other hand, define a `graphical_faith`. It is similarly defined at the top of a religion definition.

Then to string everything together, you edit the vanilla file for the _buildings_ (not holdings as one would expect). E.g. to add a new temple holding mesh, you edit `00_temple_buildings.txt`. Each of the four tiers of the holding (of the core building, really) has a series of asset blocks defining potential meshes to use for that building. You add one for your own new holding model like this:

```
asset = {
	type = pdxmesh
	name = "building_[mymod]_temple_01_mesh"
	illustration = "gfx/interface/illustrations/holding_types/temple_[mymod].dds"
	soundeffect = { soundeffect = "event:/SFX/Ambience/3DMapEmitters/Holdings/Temples/[mymod]_temple" soundparameter = { "Tier" = 0 } }
	graphical_faiths = { "[mymod]_gfx" }
	graphical_regions = { "graphical_[mymod]_region" }
}
```

In `name` you reference the _mesh_ tag from your asset file. `illustration` specifies the art forming the background of the holding UI (in vanilla a variable is used instead, with the underlying path at the top of the file). `soundeffect` references ambient sound you hear when you hover over the holding in the game. And here `graphical_faiths` references one or multiple graphical\_faiths that you can define for your new religion.

Finally, `graphical_region` is a fully optional way to restrict the geographic usage of the model. It can be used if you have several versions of the same model, using e.g. different materials so they blend in with different locales. They reference to a `graphical_region` in `map_data/geographical_regions.txt`, where you can add new ones too.

This syntax works the same for cities and castles; just use `graphical_cultures` in the place of `graphical_faiths`.

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
| Graphics | 3D models • [Exporters](https://ck3.paradoxwikis.com/Exporters "Exporters") • [Coat of arms](https://ck3.paradoxwikis.com/Coat_of_arms_modding "Coat of arms modding") • [Graphical assets](https://ck3.paradoxwikis.com/Graphical_assets "Graphical assets") • [Fonts](https://ck3.paradoxwikis.com/Fonts "Fonts") • [Particles](https://ck3.paradoxwikis.com/index.php?title=Particles&action=edit&redlink=1 "Particles (page does not exist)") • [Shaders](https://ck3.paradoxwikis.com/index.php?title=Shaders&action=edit&redlink=1 "Shaders (page does not exist)") • [Unit models](https://ck3.paradoxwikis.com/index.php?title=Unit_models&action=edit&redlink=1 "Unit models (page does not exist)") |

|     |     |
| --- | --- |
| Audio | [Music](https://ck3.paradoxwikis.com/Music_modding "Music modding") • [Sound](https://ck3.paradoxwikis.com/Sound_modding "Sound modding") |

|     |     |
| --- | --- |
| Other | [Console commands](https://ck3.paradoxwikis.com/Console_commands "Console commands") • [Checksum](https://ck3.paradoxwikis.com/Checksum "Checksum") • [Mod structure](https://ck3.paradoxwikis.com/Mod_structure "Mod structure") • [Mod compatibility](https://ck3.paradoxwikis.com/Mod_compatibility "Mod compatibility") • [Modding tools](https://ck3.paradoxwikis.com/Modding_tools "Modding tools") • [Troubleshooting](https://ck3.paradoxwikis.com/Mod_troubleshooting "Mod troubleshooting") |

Retrieved from " [https://ck3.paradoxwikis.com/index.php?title=3D\_models&oldid=28182](https://ck3.paradoxwikis.com/index.php?title=3D_models&oldid=28182)"

[Categories](https://ck3.paradoxwikis.com/Special:Categories "Special:Categories"):

- [Timeless](https://ck3.paradoxwikis.com/Category:Timeless "Category:Timeless")
- [Modding](https://ck3.paradoxwikis.com/Category:Modding "Category:Modding")