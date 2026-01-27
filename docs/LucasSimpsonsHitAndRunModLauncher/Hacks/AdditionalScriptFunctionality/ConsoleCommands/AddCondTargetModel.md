---
title: "AddCondTargetModel"
description: "Specify the name of a valid model for a destroycars condition or a hitpeds condition."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 379 # 1.18
---

Specify the name of a valid model for a [[../MissionConditions/destroycars.md]] condition or a [[../MissionConditions/hitpeds.md]] condition.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStageCondition.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
AddCondTargetModel( model_name );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddCondTargetModel( model_name )
```
{{ endtab }}
{{ endtabs }}

* **model_name**: The name of the car or character model (depending on the condition type).

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddCondition("hitpeds");
	AddCondTargetModel("marge");
CloseCondition();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddCondition("hitpeds")
	Game.AddCondTargetModel("marge")
Game.CloseCondition()
```
{{ endtab }}
{{ endtabs }}