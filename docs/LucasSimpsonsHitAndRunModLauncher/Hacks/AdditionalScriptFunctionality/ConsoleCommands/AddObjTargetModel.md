---
title: "AddObjTargetModel"
description: "Specify the name of a valid model for a destroycars objective or a hitpeds objective."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 379 # 1.18
---

Specify the name of a valid model for a [[../MissionObjectives/destroycars.md]] objective or a [[../MissionObjectives/hitpeds.md]] objective.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStageObjective.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
AddObjTargetModel( model_name );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddObjTargetModel( model_name )
```
{{ endtab }}
{{ endtabs }}

* **model_name**: The name of the car or character model (depending on the objective type).

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddObjective("hitpeds");
	AddObjTargetModel("marge");
CloseObjective();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddObjective("hitpeds")
	Game.AddObjTargetModel("marge")
Game.CloseObjective()
```
{{ endtab }}
{{ endtabs }}