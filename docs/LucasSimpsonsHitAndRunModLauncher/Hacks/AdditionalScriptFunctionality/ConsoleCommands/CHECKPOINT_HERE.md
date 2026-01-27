---
title: "CHECKPOINT_HERE"
description: "Adds a checkpoint to a stage."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 379 # 1.18
---

This command adds a checkpoint to a stage.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStage.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
CHECKPOINT_HERE();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.CHECKPOINT_HERE()
```
{{ endtab }}
{{ endtabs }}

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
	CHECKPOINT_HERE();

	AddObjective("dummy");
	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage()
	Game.CHECKPOINT_HERE()

	Game.AddObjective("dummy")
	Game.CloseObjective()
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}

# Notes
Where the player spawns, the ped group, the traffic group and more can be configured when a stage is resumed from a checkpoint with the following commands:
* [[SetCheckpointDynaloadData.md]]
* [[SetCheckpointPedGroup.md]]
* [[SetCheckpointResetPlayerInCar.md]]
* [[SetCheckpointResetPlayerOutCar.md]]
* [[SetCheckpointTrafficGroup.md]]

Any parameters set with those commands also affect the defaults for subsequent checkpoints.

Furthermore, you can also use the [[IfCurrentCheckpoint.md]] conditional command to only execute certain commands when resuming from a checkpoint.

What checkpoint is resumed from when failing or restarting is remembered by its index. So if you reached the second checkpoint, you will resume from the second checkpoint regardless of if its on the same stage.