---
title: "SetPedsEnabled"
description: "Sets whether or not pedestrians are enabled for a mission."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 384 # 1.20
---

Sets whether or not pedestrians are enabled for a mission.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitInner.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetPedsEnabled( peds_enabled );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetPedsEnabled( peds_enabled )
```
{{ endtab }}
{{ endtabs }}

* **peds_enabled**: Whether or not peds are enabled. 
    * Defaults to 1 (true) unless [[/TheSimpsonsHitAndRun/Scripting/ConsoleCommands/StreetRacePropsLoad.md]] is called in the mission.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
SelectMission("m1");
	// ...

    StreetRacePropsLoad("l4_m1p.p3d;");
	StreetRacePropsUnload("l4_m1p.p3d:");
    
    // Enable Peds even though Street Race Props are in use.
	SetPedsEnabled(1);

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

    Game.StreetRacePropsLoad("l4_m1p.p3d;")
	Game.StreetRacePropsUnload("l4_m1p.p3d:")
    
    -- Enable Peds even though Street Race Props are in use.
	Game.SetPedsEnabled(1)

	Game.AddStage()
    	-- ...
	Game.CloseStage()
Game.CloseMission()
```
{{ endtab }}
{{ endtabs }}

# Notes
This command can be helpful for enabling peds in a mission where the "Street Race Props" would not interfere with the ped paths, such as the original game's L1M7 which lacks peds by default.

# Version History
## Version 1.23.8
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.8/Hacks/AdditionalScriptFunctionality/ConsoleCommands/SetPedsEnabled.md }}

## Version 1.21
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.21/Hacks/AdditionalScriptFunctionality/ConsoleCommands/SetPedsEnabled.md }}