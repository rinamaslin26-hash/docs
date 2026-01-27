---
title: "SetStageVehicleCharacterJumpOut"
description: "Set the character to jump out of the vehicle when it's destroyed."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 383 # 1.19
---

Set the character to jump out of the vehicle when it's destroyed.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStage.md }}

Additionally, this should only be called on characters previously added to the car with [[AddStageVehicleCharacter.md]].

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetStageVehicleCharacterJumpOut( car, character, [direction] );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetStageVehicleCharacterJumpOut( car, character, [direction] )
```
{{ endtab }}
{{ endtabs }}

* **car**: The name of the car.
	* **current**: The player's current car.
* **character**: The name of the character.
* **direction**: The direction that the character will jump out of the vehicle. This is an angle from 0 to 360 degrees.
	* The default value of this depends on the character's position relative to the origin of the car.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();    
	AddStageVehicle("cVan", "m1_cVan", "NULL");

	AddStageVehicleCharacter("cVan", "lisa");
	SetStageVehicleCharacterJumpOut("cVan", "lisa", 270);

	AddObjective("dummy");
	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage() 
	Game.AddStageVehicle("cVan", "m1_cVan", "NULL")

	Game.AddStageVehicleCharacter("cVan", "lisa")
	Game.SetStageVehicleCharacterJumpOut("cVan", "lisa", 270)

	Game.AddObjective("dummy")
	Game.CloseObjective()
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}