---
title: "SetCondThreshold"
description: "Set a threshold for the insidetrigger / outsidetrigger conditions."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 379 # 1.18
---

Set a threshold for the the [[../MissionConditions/insidetrigger-outsidetrigger.md]] conditions.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStageCondition.md }}

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

* **threshold**: The amount of time the player must be inside or outside the trigger to fail the condition.
    * Defaults to 0.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddCondition("insidetrigger");
	SetCondTrigger("z2phone1");

	// Fail the player if they're inside the trigger for 10 seconds.
	SetCondThreshold(10);
CloseCondition();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddCondition("insidetrigger")
	Game.SetCondTrigger("z2phone1")

	-- Fail the player if they're inside the trigger for 10 seconds.
	Game.SetCondThreshold(10)
Game.CloseCondition()
```
{{ endtab }}
{{ endtabs }}