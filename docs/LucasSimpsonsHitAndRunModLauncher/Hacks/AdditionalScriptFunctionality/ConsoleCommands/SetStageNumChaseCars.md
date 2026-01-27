---
title: "SetStageNumChaseCars"
description: "Set the amount of chase cars that will spawn during a Hit & Run this stage."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 379 # 1.18
---

Set the amount of chase cars that will spawn during a Hit & Run this stage.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStage.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetStageNumChaseCars( amount );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetStageNumChaseCars( amount )
```
{{ endtab }}
{{ endtabs }}

* **amount**: The amount of chase cars to spawn. This can be from 1 to 5. Defaults to the level's number of chase cars.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
	// You probably want to avoid stuff during this stage...
	SetStageNumChaseCars(5);

	AddObjective("dummy");
	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage() 
	-- You probably want to avoid stuff during this stage...
	Game.SetStageNumChaseCars(5)

	Game.AddObjective("dummy")
	Game.CloseObjective()
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}