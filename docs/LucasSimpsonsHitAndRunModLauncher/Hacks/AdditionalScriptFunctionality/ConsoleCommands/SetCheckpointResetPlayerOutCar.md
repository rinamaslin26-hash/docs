---
title: "SetCheckpointResetPlayerOutCar"
description: "Makes the player reset on foot when resuming a stage from a checkpoint."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 78 # 1.25
---

This command makes the player reset on foot when resuming a stage from a checkpoint.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStage.md }}

Additionally, this should be called alongside [[CHECKPOINT_HERE.md]].

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetCheckpointResetPlayerOutCar( player_locator, car_locator );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetCheckpointResetPlayerOutCar( player_locator, car_locator )
```
{{ endtab }}
{{ endtabs }}

* **player_locator**: The name of a [[/Pure3DFiles/ChunkTypes/Locator.md|CarStart Locator]] that the player character will spawn on.
* **car_locator**: The name of a [[/Pure3DFiles/ChunkTypes/Locator.md|CarStart Locator]] that the player's car will spawn on.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
	CHECKPOINT_HERE();
	SetCheckpointResetPlayerInCar("level1_homer_start", "level1_carstart");

	AddObjective("dummy");
	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage()
	Game.CHECKPOINT_HERE()
	Game.SetCheckpointResetPlayerInCar("level1_homer_start", "level1_carstart")

	Game.AddObjective("dummy")
	Game.CloseObjective()
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}