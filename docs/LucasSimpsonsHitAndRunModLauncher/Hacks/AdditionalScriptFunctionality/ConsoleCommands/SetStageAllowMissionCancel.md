---
title: "SetStageAllowMissionCancel"
description: "Set whether or not the player is allowed to restart or cancel the mission during the stage."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 380 # 1.18.1
---

Set whether or not the player is allowed to restart or cancel the mission during the stage.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStage.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetStageAllowMissionCancel( allow );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetStageAllowMissionCancel( allow )
```
{{ endtab }}
{{ endtabs }}

* **allow**: Whether or not to allow the player to restart or cancel the mission. 
    * Defaults to 1 / true.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
	SetStageAllowMissionCancel(0);
	
	AddObjective("dummy");
	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage()
	Game.SetStageAllowMissionCancel(0)
	
	Game.AddObjective("dummy")
	Game.CloseObjective()
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}