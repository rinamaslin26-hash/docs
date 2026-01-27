---
title: "SetStageCarChangeHitAndRunChange"
description: "Set the amount the Hit & Run meter will change when swapping to a different vehicle for the stage."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 379 # 1.18
---

Set the amount the Hit & Run meter will change when swapping to a different vehicle for the stage.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStage.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetStageCarChangeHitAndRunChange( change_amount );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetStageCarChangeHitAndRunChange( change_amount )
```
{{ endtab }}
{{ endtabs }}

* **change_amount**: The amount that will be added to the Hit & Run meter when changing your car. 
	* Defaults to -100.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();    
	SetStageCarChangeHitAndRunChange(-100);

	AddObjective("dummy");
	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage()    
	Game.SetStageCarChangeHitAndRunChange(-100)

	Game.AddObjective("dummy")
	Game.CloseObjective()
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}