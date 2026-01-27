---
title: "SetObjThreshold"
description: "Set a threshold for the insidetrigger / outsidetrigger objectives."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 379 # 1.18
---

Set a threshold for the [[../MissionObjectives/insidetrigger-outsidetrigger.md]] objectives.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStageObjective.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetCondThreshold( threshold );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetCondThreshold( threshold )
```
{{ endtab }}
{{ endtabs }}

* **threshold**: The amount of time the player must be inside or outside the trigger to pass the objective.
    * Defaults to 0.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddObjective("insidetrigger");
	SetObjTrigger("z2phone1");

	// Require the player to be inside that trigger for 10 seconds to pass.
	SetObjThreshold(10);
CloseObjective();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddObjective("insidetrigger")
	Game.SetObjTrigger("z2phone1")

	-- Require the player to be inside that trigger for 10 seconds to pass.
	Game.SetObjThreshold(10)
Game.CloseObjective()
```
{{ endtab }}
{{ endtabs }}