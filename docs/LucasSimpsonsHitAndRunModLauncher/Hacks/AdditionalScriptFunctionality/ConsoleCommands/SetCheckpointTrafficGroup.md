---
title: "SetCheckpointTrafficGroup"
description: "Sets the current traffic group when resuming a stage from a checkpoint."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 78 # 1.25
---

This command sets the current traffic group when resuming a stage from a checkpoint.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStage.md }}

Additionally, this should be called alongside [[CHECKPOINT_HERE.md]].

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetCheckpointTrafficGroup( traffic_group );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetCheckpointTrafficGroup( traffic_group )
```
{{ endtab }}
{{ endtabs }}

* **traffic_group**: The index of the traffic group to use.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
	CHECKPOINT_HERE();
	SetCheckpointTrafficGroup(7);

	AddObjective("dummy");
	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage()
	Game.CHECKPOINT_HERE()
	Game.SetCheckpointTrafficGroup(7)

	Game.AddObjective("dummy")
	Game.CloseObjective()
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}

# Notes
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/DynamicTrafficRequired.md }}