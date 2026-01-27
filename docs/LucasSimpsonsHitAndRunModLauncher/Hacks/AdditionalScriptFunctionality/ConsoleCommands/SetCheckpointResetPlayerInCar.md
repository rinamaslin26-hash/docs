---
title: "SetCheckpointResetPlayerInCar"
description: "Makes the player reset in their car when resuming a stage from a checkpoint."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 78 # 1.25
---

This command makes the player reset in their car when resuming a stage from a checkpoint.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStage.md }}

Additionally, this should be called alongside [[CHECKPOINT_HERE.md]].

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetCheckpointResetPlayerInCar( locator );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetCheckpointResetPlayerInCar( locator )
```
{{ endtab }}
{{ endtabs }}

* **locator**: The name of a [[/Pure3DFiles/ChunkTypes/Locator.md|CarStart Locator]] that the car will spawn on.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
	CHECKPOINT_HERE();
	SetCheckpointResetPlayerInCar("m1_carstart");

	AddObjective("dummy");
	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage()
	Game.CHECKPOINT_HERE()
	Game.SetCheckpointResetPlayerInCar("m1_carstart")

	Game.AddObjective("dummy")
	Game.CloseObjective()
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}