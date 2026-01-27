---
title: "SetCondSpeedRangeKMH"
description: "Set a speed range for the maintainspeed condition."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 379 # 1.18
---

Set a speed range for the [[../MissionConditions/maintainspeed.md]] condition.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStageCondition.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetCondSpeedRangeKMH( lower_limit, upper_limit );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetCondSpeedRangeKMH( lower_limit, upper_limit )
```
{{ endtab }}
{{ endtabs }}

* **lower_limit**: The lowest speed the player is allowed to go.
	* You can use `0` to have no lower limit.
* **upper_limit**: The highest speed the player is allowed to go.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddCondition("maintainspeed");
	SetCondSpeedRangeKMH(90, 150);
CloseCondition();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddCondition("maintainspeed")
	Game.SetCondSpeedRangeKMH(90, 150)
Game.CloseCondition()
```
{{ endtab }}
{{ endtabs }}