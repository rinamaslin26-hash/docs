---
title: "SetObjMessageIndex"
description: "Set a message index for the insidetrigger / outsidetrigger objectives."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 379 # 1.18
---

Set a message index for the [[../MissionObjectives/insidetrigger-outsidetrigger.md]] objectives.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStageObjective.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetObjMessageIndex( message_index );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetObjMessageIndex( message_index )
```
{{ endtab }}
{{ endtabs }}

* **message_index**: The objective message index (just like the [[/TheSimpsonsHitAndRun/Scripting/ConsoleCommands/SetStageMessageIndex.md]] command) to use for the objective.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddObjective("insidetrigger");
	SetObjTrigger("z2phone1");

	// Show MISSION_OBJECTIVE_03 if the player enters the trigger.
	SetObjMessageIndex(3);
CloseObjective();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddObjective("insidetrigger")
	Game.SetObjTrigger("z2phone1")

	-- Show MISSION_OBJECTIVE_03 if the player enters the trigger.
	Game.SetObjMessageIndex(3)
Game.CloseObjective()
```
{{ endtab }}
{{ endtabs }}