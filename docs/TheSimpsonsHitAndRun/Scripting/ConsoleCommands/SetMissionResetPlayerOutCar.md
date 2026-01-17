---
title: "SetMissionResetPlayerOutCar"
description: "Sets the positions where the player and their vehicle are placed upon restarting a mission."
authors: [ 2116 ]
---

Sets the positions where the player and their vehicle are placed upon restarting a mission.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitInner.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetMissionResetPlayerOutCar( player_locator, vehicle_locator );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetMissionResetPlayerOutCar( player_locator, vehicle_locator )
```
{{ endtab }}
{{ endtabs }}

* **player_locator**: The name of the [[/Pure3DFiles/ChunkTypes/Locator.md|CarStart Locator]] where the player is placed.
* **vehicle_locator**: The name of the [[/Pure3DFiles/ChunkTypes/Locator.md|CarStart Locator]] where the player's vehicle is placed.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
SelectMission("m1");
	// ...

	SetMissionResetPlayerOutCar("m4_homer_start", "m4_carstart");

	AddStage();
		// ...
	CloseStage();
CloseMission();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SelectMission("m1")
	-- ...

	Game.SetMissionResetPlayerOutCar("m4_homer_start", "m4_carstart")

	Game.AddStage()
		-- ...
	Game.CloseStage()
Game.CloseMission()
```
{{ endtab }}
{{ endtabs }}

# Notes
When both this command and [[SetMissionResetPlayerInCar.md]] are used, the player will be placed at the **player_locator** from this command, and the vehicle will be placed at whichever **vehicle_locator** is specified last in the script.