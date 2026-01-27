---
title: "SetStageVehicleReset"
description: "Sets whether or not an AI car will automatically reset onto the road if it's off for too long in certain objective types."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 379 # 1.18
---

Sets whether or not an AI car will automatically reset onto the road if it's off for too long in certain objective types (such as `evade`).

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStage.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetStageVehicleReset( stage_vehicle_name, reset );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetStageVehicleReset( stage_vehicle_name, reset )
```
{{ endtab }}
{{ endtabs }}

* **stage_vehicle_name**: The name of the stage vehicle.
* **reset**: Set whether or not it should have this behaviour.
	* The default depends on the type of behaviour the AI vehicle is using.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
	AddStageVehicle("cNerd", "m3_nerd_start", "evade");
	SetStageVehicleReset("cNerd", 0);

	AddObjective("dummy");
	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage() 	
	Game.AddStageVehicle("cNerd", "m3_nerd_start", "evade")
	Game.SetStageVehicleReset("cNerd", 0)

	Game.AddObjective("dummy")
	Game.CloseObjective()
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}