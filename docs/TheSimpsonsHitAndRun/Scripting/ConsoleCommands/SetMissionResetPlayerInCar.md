---
title: "SetMissionResetPlayerInCar"
description: "Forces the player into their vehicle and sets the position the vehicle is placed upon restarting a mission."
authors: [ 2116 ]
---

Forces the player into their vehicle and sets the position the vehicle is placed upon restarting a mission.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitInner.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetMissionResetPlayerInCar( vehicle_locator );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetMissionResetPlayerInCar( vehicle_locator )
```
{{ endtab }}
{{ endtabs }}

* **vehicle_locator**: The name of the [[/Pure3DFiles/ChunkTypes/Locator.md|CarStart Locator]] where the player's vehicle is placed.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
SelectMission("m1");
	// ...
	
	SetMissionResetPlayerInCar("m1_carstart");

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
	
	Game.SetMissionResetPlayerInCar("m1_carstart")

	Game.AddStage()	
		-- ...
	Game.CloseStage()
Game.CloseMission()
```
{{ endtab }}
{{ endtabs }}

# Notes
When both this command and [[SetMissionResetPlayerOutCar.md]] are used, the player will be placed at the **player_locator** from [[SetMissionResetPlayerOutCar.md]], and the vehicle will be placed at whichever **vehicle_locator** is specified last in the script.