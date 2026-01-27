---
title: "SetCondDelay"
description: "Sets how long the delay is before the mission failed screen comes up when failing as a result of various ASF conditions."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 379 # 1.18
---

Sets how long the delay is before the mission failed screen comes up when failing as a result of the following ASF conditions:

* [[../MissionConditions/collectcoins.md]]
* [[../MissionConditions/collectwrench.md]]
* [[../MissionConditions/destroycars.md]]
* [[../MissionConditions/hitandrun.md]]
* [[../MissionConditions/hitandruncaught.md]]
* [[../MissionConditions/hitandrunrage.md]]
* [[../MissionConditions/hitpeds.md]]
* [[../MissionConditions/jump.md]]
* [[../MissionConditions/spring.md]]

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStageCondition.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetCondDelay( delay );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetCondDelay( delay )
```
{{ endtab }}
{{ endtabs }}

* **delay**: The amount of time in seconds to delay the mission ending after the condition is failed. 
    * Default delay varies by condition type.
	* [[../MissionConditions/collectcoins.md]]: 1 second.
	* [[../MissionConditions/collectwrench.md]]: 1 second.
	* [[../MissionConditions/destroycars.md]]: 1 second.
	* [[../MissionConditions/hitandrun.md]]: 2 seconds.
	* [[../MissionConditions/hitandruncaught.md]]: 2 seconds.
	* [[../MissionConditions/hitandrunrage.md]]: 1 second.
	* [[../MissionConditions/hitpeds.md]]: 1 second.
	* [[../MissionConditions/jump.md]]: 1 second.
	* [[../MissionConditions/spring.md]]: 1 second.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddCondition("jump");
	// Make it wait longer for some reason.
	SetCondDelay(3);
CloseCondition();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddCondition("jump")
	-- Make it wait longer for some reason.
	Game.SetCondDelay(3)
Game.CloseCondition()
```
{{ endtab }}
{{ endtabs }}