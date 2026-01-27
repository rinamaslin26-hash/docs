---
title: "SetStageHitAndRun"
description: "Set the value of the Hit & Run meter when starting the stage."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 379 # 1.18
---

Set the value of the Hit & Run meter when starting the stage.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStage.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetStageHitAndRun( meter );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetStageHitAndRun( meter )
```
{{ endtab }}
{{ endtabs }}

meter: The value to set the meter to. From 0 to 100.
100 will trigger a Hit & Run when reaching the stage.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
	SetStageHitAndRun(100);

	AddObjective("dummy");
	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage()
	Game.SetStageHitAndRun(100)

	Game.AddObjective("dummy")
	Game.CloseObjective()
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}