---
title: "SetStageHitAndRunFine"
description: "Set the Hit & Run fine for a stage."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 379 # 1.18
---

Set the Hit & Run fine for a stage.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStage.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetStageHitAndRunFine( fine );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetStageHitAndRunFine( fine )
```
{{ endtab }}
{{ endtabs }}

* **fine**: The amount to fine the player during the stage. Default's to the level's hit & run fine.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
	// No fine during this stage, go crazy.
	SetStageHitAndRunFine(0);

	AddObjective("dummy");
	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage() 
	-- No fine during this stage, go crazy.
	Game.SetStageHitAndRunFine(0)

	Game.AddObjective("dummy")
	Game.CloseObjective()
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}