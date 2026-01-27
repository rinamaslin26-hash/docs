---
title: "UseTrafficGroup"
description: "Set what traffic group will be used when the mission is selected or restarted."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 388 # 1.22
---

Set what traffic group will be used when the mission is selected or restarted.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitInner.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
UseTrafficGroup( group_index );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.UseTrafficGroup( group_index )
```
{{ endtab }}
{{ endtabs }}

* **group_index**: The index of the traffic group.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
SelectMission("m1");
	// ...

    // Use the 2nd traffic group when restarting the mission.
    // This does NOT apply when going from the SD mission into the main mission.
	UseTrafficGroup(2);

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

    -- Use the 2nd traffic group when restarting the mission.
    -- This does NOT apply when going from the SD mission into the main mission.
	Game.UseTrafficGroup(2)

	Game.AddStage()
    	-- ...
	Game.CloseStage()
Game.CloseMission()
```
{{ endtab }}
{{ endtabs }}

# Notes
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/DynamicTrafficRequired.md }}