---
title: "SetStageVehicleCharacterVisible"
description: "Set if the character is visible in the vehicle. This allows you to make characters visible in vehicles where the driver is not."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 383 # 1.19
---

Set if the character is visible in the vehicle.

This allows you to make characters visible in vehicles where the driver is not.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStage.md }}

Additionally, this should only be called on characters previously added to the car with [[AddStageVehicleCharacter.md]].

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetStageVehicleCharacterVisible( car, character );
```
{{ endtab }}
{{ tab Lua }}
```lua
GameSetStageVehicleCharacterVisible( car, character )
```
{{ endtab }}
{{ endtabs }}

* **car**: The name of the car.
* **character**: The name of the character to make visible.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
	AddStageVehicle("cVan", "m1_cVan", "NULL", "cVan.con");
	
	// Bart uses the smoke location in this example.
	AddStageVehicleCharacter("cVan", "bart", "sl", 0);

	// Let's pretend cVan.con makes the driver invisible.
	// We'll use this to make Bart visible anyways since he's positioned on the outside of the car.
	SetStageVehicleCharacterVisible("cVan", "bart");

	AddObjective("dummy");
	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage() 
	Game.AddStageVehicle("cVan", "m1_cVan", "NULL", "cVan.con")
	
	-- Bart uses the smoke location in this example.
	Game.AddStageVehicleCharacter("cVan", "bart", "sl", 0)

	-- Let's pretend cVan.con makes the driver invisible.
	-- We'll use this to make Bart visible anyways since he's positioned on the outside of the car.
	Game.SetStageVehicleCharacterVisible("cVan", "bart")

	Game.AddObjective("dummy")
	Game.CloseObjective()
Game.CloseStage()       
```
{{ endtab }}
{{ endtabs }}