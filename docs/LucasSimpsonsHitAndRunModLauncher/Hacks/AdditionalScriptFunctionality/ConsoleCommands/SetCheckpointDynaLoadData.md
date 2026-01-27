---
title: "SetCheckpointDynaLoadData"
description: "Sets the dyna load data string to use when resuming a stage from a checkpoint."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 78 # 1.25
---

This command sets the dyna load data string to use when resuming a stage from a checkpoint.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStage.md }}

Additionally, this should be called alongside [[CHECKPOINT_HERE.md]].

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetCheckpointDynaLoadData( dyna_load_data );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetCheckpointDynaLoadData( dyna_load_data )
```
{{ endtab }}
{{ endtabs }}

* **dyna_load_data**: The [[/TheSimpsonsHitAndRun/DynaLoadData.md]] string to execute.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
	CHECKPOINT_HERE();
	SetCheckpointDynaLoadData("l1z1.p3d;l1r1.p3d;l1r7.p3d;");

	AddObjective("dummy");
	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage()
	Game.CHECKPOINT_HERE()
	Game.SetCheckpointDynaLoadData("l1z1.p3d;l1r1.p3d;l1r7.p3d;")

	Game.AddObjective("dummy")
	Game.CloseObjective()
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}