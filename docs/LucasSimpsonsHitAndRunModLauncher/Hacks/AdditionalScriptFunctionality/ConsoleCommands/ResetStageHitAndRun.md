---
title: "ResetStageHitAndRun"
description: "Resets the Hit & Run meter when reaching a stage, erasing all existing chase cars."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 379 # 1.18
---

Resets the Hit & Run meter when reaching a stage, erasing all existing chase cars.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStage.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
ResetStageHitAndRun();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.ResetStageHitAndRun()
```
{{ endtab }}
{{ endtabs }}

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
	ResetStageHitAndRun();

	AddObjective("dummy");
	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage();
	Game.ResetStageHitAndRun()

	Game.AddObjective("dummy")
	Game.CloseObjective()
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}