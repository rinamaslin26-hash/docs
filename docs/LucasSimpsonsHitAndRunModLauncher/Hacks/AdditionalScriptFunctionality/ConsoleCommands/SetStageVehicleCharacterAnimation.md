---
title: "SetStageVehicleCharacterAnimation"
description: "Set the animation that a vehicle character will use."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 383 # 1.19
---

Set the animation that a vehicle character will use.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStage.md }}

Additionally, this should only be called on characters previously added to the car with [[AddStageVehicleCharacter.md]].

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetStageVehicleCharacterAnimation( car, character, animation, [bobbing] );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetStageVehicleCharacterAnimation( car, character, animation, [bobbing] )
```
{{ endtab }}
{{ endtabs }}

* **car**: The name of the car the character is on.
    * **current**: The player's current car.
* **character**: The name of character in the car.
* **animation**: The animation to make the character use. 
    * The default animation is "in_car_idle".
* **bobbing**: Whether or not to make the character bob up and down. 
    * Defaults to false (if this function is called).
    * This will also make the character lean side-to-side when appropriate if the **Steering Animations** fix in the [[../../BugFixes.md]] hack is enabled.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
	AddStageVehicle("cVan", "m1_cVan", "NULL", "cVan.con");
	
	// Bart uses the smoke location in this example.
	AddStageVehicleCharacter("cVan", "bart", "sl", 0);

	// Make Bart surf on the hood(ish)
	// Note that "surf_cycle" is not in the NPD animation set by default.
	SetStageVehicleCharacterAnimation("cVan", "bart", "surf_cycle");

	AddObjective("dummy");
	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage() 
	Game.AddStageVehicle("cVan", "m1_cVan", "NULL")
	
	-- Bart uses the smoke location in this example.
	Game.AddStageVehicleCharacter("cVan", "bart", "sl", 0)

	-- Make Bart surf on the hood(ish)
	-- Note that "surf_cycle" is not in the NPD animation set by default.
	Game.SetStageVehicleCharacterAnimation("cVan", "bart", "surf_cycle")

	Game.AddObjective("dummy")
	Game.CloseObjective()
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}