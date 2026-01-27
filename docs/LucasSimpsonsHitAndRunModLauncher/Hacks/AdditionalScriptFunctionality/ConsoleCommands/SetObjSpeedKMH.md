---
title: "SetObjSpeedKMH"
description: "Set the speed required to complete a reachspeed objective."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 379 # 1.18
---

Set the speed required to complete a a [[../MissionObjectives/reachspeed.md]] objective.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStageObjective.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetObjSpeedKMH( target_speed );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetObjSpeedKMH( target_speed )  
```
{{ endtab }}
{{ endtabs }}

* **target_speed**: The speed required for the objective.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddObjective("reachspeed");
	SetObjSpeedKMH(120);
CloseObjective();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddObjective("reachspeed")
	Game.SetObjSpeedKMH(120)
Game.CloseObjective()
```
{{ endtab }}
{{ endtabs }}