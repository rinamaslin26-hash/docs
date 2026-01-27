---
title: "SetCondMessageIndex"
description: "Set a message index for the insidetrigger / outsidetrigger conditions."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 379 # 1.18
---

Set a message index for the [[../MissionConditions/insidetrigger-outsidetrigger.md]] conditions.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStageCondition.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetCondMessageIndex( message_index );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetCondMessageIndex( message_index )
```
{{ endtab }}
{{ endtabs }}

* **message_index**: The condition message index (just like the [[/TheSimpsonsHitAndRun/Scripting/ConsoleCommands/SetStageMessageIndex.md]] command) to use for the condition.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddCondition("insidetrigger");
	SetCondTrigger("z2phone1");

	// Show MISSION_OBJECTIVE_03 if the player enters the trigger.
	SetCondMessageIndex(3);
CloseCondition();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddCondition("insidetrigger")
	Game.SetCondTrigger("z2phone1")

	-- Show MISSION_OBJECTIVE_03 if the player enters the trigger.
	Game.SetCondMessageIndex(3)
Game.CloseCondition()
```
{{ endtab }}
{{ endtabs }}