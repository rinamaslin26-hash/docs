---
title: "SetCondDisplay"
description: "Set how an ASF condition displays to the user."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 379 # 1.18
---

Set how an [[../MissionConditions/AllConditions.md|ASF condition]] displays to the user.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStageCondition.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetCondDisplay( display_type );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetCondDisplay( display_type )
```
{{ endtab }}
{{ endtabs }}

* **display_type**: The type of display to use to convey (or hide) the condition to the player. 
    * **none**: The display will be hidden.
    * **fill**: The bar will be full when the player is near the midpoint of the specified speed range.
		* Only for [[../MissionConditions/maintainspeed.md]] conditions.
    * **midpoint**: The bar will be empty when the player is near the lower limit and full when the player is near the higher limit.
		* Only for [[../MissionConditions/maintainspeed.md]] conditions.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddCondition("hitpeds");
	SetCondDisplay("none");
CloseCondition();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddCondition("hitpeds")
	Game.SetCondDisplay("none")
Game.CloseCondition()
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.

# Version History
## 1.18.1
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.18.1/Hacks/AdditionalScriptFunctionality/ConsoleCommands/SetCondDisplay.md }}