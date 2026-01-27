---
title: "SetStageHitAndRunDecay"
description: "Set the Hit & Run meter decay rate for a stage."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 379 # 1.18
---

Set the Hit & Run meter decay rate for a stage.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStage.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetStageHitAndRunDecay( decay_rate );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetStageHitAndRunDecay( decay_rate )
```
{{ endtab }}
{{ endtabs }}

* **decay_rate**: The decay rate. Defaults to the level's decay rate.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();    
	SetStageHitAndRunDecay(4.0);

	AddObjective("dummy");
	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage()
	Game.SetStageHitAndRunDecay(4.0)

	Game.AddObjective("dummy")
	Game.CloseObjective()
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}