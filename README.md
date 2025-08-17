# ShowHidden (ShowClips & ShowTriggers) - Enhanced

**Enhanced** addon for Garry's mod Bunnyhop gamemode that shows invisible obstacles with improved toggle-all functionality and streamlined commands.

## ✨ New Enhanced Features

* **`!tma` - Toggle All**: Smart command that enables/disables all visualisation options at once
* **`!tm` - Quick Menu**: Fast access to configuration menu  
* **Toggle All Button**: One-click enable/disable button in the settings menu
* **Smart State Detection**: Interface automatically adapts based on current settings
* **Enhanced Chat Commands**: Streamlined command set for better usability

## 🎯 Core Features

* Invisible brushes (walls)
  * Player-clip and Invisible
  * Invisible ladders
  * NoDraw and SkyBox
* Triggers (map created invisible zones)
  * Teleports and teleports with filters (reset zones)
  * Boosters: push, [gravity](https://gamebanana.com/prefabs/6677) and [base-velocity](https://gamebanana.com/prefabs/7118)
  * BunnyHop platforms (standing prevention)
  * PreSpeed prevention triggers ([gravity](https://gamebanana.com/prefabs/6760))
  * And other triggers...
* Static props collision models

You can select default, solid-color or wireframe texture for every brush/trigger type and change it's color.



## Installation

1. Download addon:
1. Unpack `show_hidden-master` folder into server's `addons` folder
2. Restart the server (if it was running)


## Internationalization support

You can change language strings in file `lua/showclips/cl_lang.lua`.


## Usage

You can toggle and configure everything from GUI (config menu).


### Chat commands

| Action              | Chat command      | Console command/variable   |
| ------------------- | ----------------- | -------------------------- |
| **🚀 Toggle All**   | **`!tma`**        | **`tma`**                  |
| **🎮 Quick Menu**   | **`!tm`**         | **`tm`**                   |
| Open config menu    | `!showhidden`     | `showhidden`               |
| Toggle ShowClips    | `!toggleclips`    | `showclips 1/0`            |
| Toggle ShowTriggers | `!toggletriggers` | `showtriggers_enabled 1/0` |
| Toggle ShowProps    | `!toggleprops`    | `showprops 1/0`            |

**New Enhanced Commands:**
- `!tma` - **Smart Toggle All**: Enables all options if any are disabled, disables all if everything is enabled
- `!tm` - **Quick Menu Access**: Instant access to configuration menu (alias for `!showhidden`)

There are also "on" and "off" commands for ShowClips and ShowTriggers.
Chat commands can be changed at the bottom of the `lua/show_hidden/sv_init.lua` file.


### Console commands and variables

| Command | Description |
| ------- | ----------- |
| `showhidden` | Open settings window |
| `showclips 0-31` | Set bit-mask with enabled brush types |
| `showclips_material 1-5 0-2 "R G B A"` | Set material and color for brush type |
| `showprops 0/1` | Toggle static props collision models |
| `showprops_material 0-2 "R G B A"` | Set material and color for props |
| `showtriggers_enabled 0/1` | Toggle ShowTriggers |
| `showtriggers_types 0-255` | Set bit-mask with enabled trigger types |
| `showtriggers_material 1-8 0-2 "R G B A"` | Set material and color for trigger type |
| `showtriggers_trace` | Show triggers information (you looking at), use `developer 1` to see text and lines on screen |

**MaterialTypes:** 0 - wireframe, 1 - default, 2 - solid color

**BrushTypes:** 1 - player-clip, 2 - invisible, 3 - ladder, 4 - nodraw, 5 - skybox

**TriggerTypes:** 1 - other, 2 - teleport, 3 - tele with filter, 4 - push, 5 - basevel, 6 - gravity, 7 - anti-pre, 8 - platform



## Credits
* Enchanced by [Poe](https://steamcommunity.com/id/dowjones123/) 
* Made by [CLazStudio](https://steamcommunity.com/id/CLazStudio/) 
* ShowClips part initially was sponsored by [rq](https://steamcommunity.com/id/relrq/)
* ShowTriggers part based on __Meeno__ version
* Trigger types inspired by [improved-showtriggers](https://github.com/blankbhop/improved-showtriggers) by __Eric__ and __Blank__
* This addon uses modified [luabsp-gmod](https://github.com/unktower/gmod-luabsp) library by __h3xcat__ licensed under GPL-3.0
