---
title: "SetStageVehicleCharacterScale"
description: "Set the scale of the character in the stage vehicle."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 383 # 1.19
---

Set the scale of the character in the stage vehicle.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStage.md }}

Additionally, this should only be called on characters previously added to the car with [[AddStageVehicleCharacter.md]].

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetStageVehicleCharacterScale( car, character, scale );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetStageVehicleCharacterScale( car, character, scale )
```
{{ endtab }}
{{ endtabs }}

* **car**: The name of the car the character is in.
* **character**: The name of the character.
* **scale**: Set the scale of the character. 
    * Defaults to the car's character scale set with [[/TheSimpsonsHitAndRun/Scripting/ConsoleCOmmands/SetCharacterScale.md]].

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();    
	AddStageVehicle("cVan", "m1_cVan", "NULL", "cVan.con");
	AddStageVehicleCharacter("cVan", "bart", "sl", 0);	

	// Big Bort
	SetStageVehicleCharacterScale("cVan", "bart", 3);

	AddObjective("dummy");
	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage() 
	Game.AddStageVehicle("cVan", "m1_cVan", "NULL", "cVan.con")
	Game.AddStageVehicleCharacter("cVan", "bart", "sl", 0)

	-- Big Bort
	Game.SetStageVehicleCharacterScale("cVan", "bart", 3)

	Game.AddObjective("dummy")
	Game.CloseObjective()
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}