---
title: "SetObjDecay"
description: "Set the decay delay and decay rate for the insidetrigger / outsidetrigger objectives."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 379 # 1.18
---

Set the decay delay and decay rate for the [[../MissionObjectives/insidetrigger-outsidetrigger.md]] objectives.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStageObjective.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetObjDecay( decay_rate, [decay_delay]  );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetObjDecay( decay_rate, [decay_delay]  )
```
{{ endtab }}
{{ endtabs }}

* **decay_rate**: The rate at which the objective decays. 
    * Defaults to 0.
* **decay_delay**: The amount of time that must pass before the objective begins decaying.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddObjective("insidetrigger");
	SetObjTrigger("z2Phone1");

	// Decay the meter by "3 seconds" when the player is not inside the trigger for more than 2 seconds.
	SetObjDecay(3, 2);
CloseObjective();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddObjective("insidetrigger")
	Game.SetObjTrigger("z2Phone1")

	-- Decay the meter by "3 seconds" when the player is not inside the trigger for more than 2 seconds.
	Game.SetObjDecay(3, 2)
Game.CloseObjective()
```
{{ endtab }}
{{ endtabs }}