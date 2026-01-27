---
title: "SetStageVehicleAbductable"
description: "Sets if a vehicle can be abducted by a UFO in a mission."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 78 # 1.25
---

Sets if a vehicle can be abducted by a UFO in a mission.

This persists until the command is called again, the status is reset with [[ResetStageVehicleAbductable.md]] or the mission ends.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStage.md }}


# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetStageVehicleAbductable( vehicle, abductable );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetStageVehicleAbductable( vehicle, abductable )
```
{{ endtab }}
{{ endtabs }}

* **vehicle**: The vehicle you would like to reset the abductable flag on.
	* When using `current` for the player's current vehicle, the flag will only affect the car the player has at the time they reach the stage.
* **abductable**: Set whether or not the vehicle will be abductable.
	* The default value of this depends on what is set in the [[../../CustomCarSupport.md]] hack.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
SetStageVehicleAbductable("skinn_v", true);
```
```js
SetStageVehicleAbductable("skinn_v", 1);
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetStageVehicleAbductable("skinn_v", true)
```
```lua
Game.SetStageVehicleAbductable("skinn_v", 1)
```
{{ endtab }}
{{ endtabs }}