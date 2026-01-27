---
title: "SetCondDecay"
description: "Set the decay delay and decay rate for the insidetrigger / outsidetrigger conditions."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 379 # 1.18
---

Set the decay delay and decay rate for the [[../MissionConditions/insidetrigger-outsidetrigger.md]] conditions.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStageCondition.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetCondDecay( decay_rate, [decay_delay]  );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetCondDecay( decay_rate, [decay_delay]  )
```
{{ endtab }}
{{ endtabs }}

* **decay_rate**: The rate at which the condition decays. 
    * Defaults to 0.
* **decay_delay**: The amount of time that must pass before the condition begins decaying.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddCondition("insidetrigger");
	SetCondTrigger("z2Phone1");

	// Decay the meter by "3 seconds" when the player is not inside the trigger for more than 2 seconds.
	SetCondDecay(3, 2);
CloseCondition();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddCondition("insidetrigger")
	Game.SetCondTrigger("z2Phone1")

	-- Decay the meter by "3 seconds" when the player is not inside the trigger for more than 2 seconds.
	Game.SetCondDecay(3, 2)
Game.CloseCondition()
```
{{ endtab }}
{{ endtabs }}