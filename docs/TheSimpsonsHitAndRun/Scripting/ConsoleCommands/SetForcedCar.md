---
title: "SetForcedCar"
description: "Sets a mission to require a forced car."
authors: [ 2 ]
---

Sets a mission to require a forced car.

This will disable phonebooths for the duration of the mission.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitInner.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetForcedCar();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetForcedCar()
```
{{ endtab }}
{{ endtabs }}

# Examples
{{ tabs }}
{{ tab MFK }}
```js
SelectMission("m6");
	// ...
	InitLevelPlayerVehicle("marge_v", "m6_canyonero_start", "OTHER");

	SetForcedCar();

	AddStage();
		// ...
	CloseStage();
CloseMission();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SelectMission("m6")
	-- ...
	Game.InitLevelPlayerVehicle("marge_v", "m6_canyonero_start", "OTHER")

	Game.SetForcedCar()

	Game.AddStage()
		-- ...
	Game.CloseStage()
Game.CloseMission()
```
{{ endtab }}
{{ endtabs }}

# Notes
This command must be used in conjunction with [[InitLevelPlayerVehicle.md]] to add a player car to the `OTHER` slot for the mission. The game will crash if there is no `OTHER` vehicle.