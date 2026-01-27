---
title: "SetObjTrigger"
description: "Specify the locator whose triggers will be used for the insidetrigger/outsidetrigger objectives."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 379 # 1.18
---

Specify the locator whose triggers will be used for the [[../MissionObjectives/insidetrigger-outsidetrigger.md]] objectives.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStageObjective.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetObjTrigger( locator_name );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetObjTrigger( locator_name )
```
{{ endtab }}
{{ endtabs }}

* **locator_name**: The name of the locator whose triggers will be used for the objective.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddObjective("insidetrigger");
	SetObjTrigger("z2phone1");
CloseObjective();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddObjective("insidetrigger")
	Game.SetObjTrigger("z2phone1")
Game.CloseObjective()
```
{{ endtab }}
{{ endtabs }}