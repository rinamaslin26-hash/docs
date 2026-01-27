---
title: "SetObjExplosion"
description: "Set an explosion effect to use for a hitpeds objective."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 379 # 1.18
---

Set an explosion effect to use for a [[../MissionObjectives/hitpeds.md]].

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStageObjective.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetObjExplosion( explosion_index, scale, [vertical_scale]);
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetObjExplosion( explosion_index, scale, [vertical_scale])
```
{{ endtab }}
{{ endtabs }}

* **explosion_index**: The index of the explosion effect.
    * **24**: Car Explosion.
    * Other explosion effects should also work providing they are loaded.
* **scale**: The scale of the explosion.
* **vertical_scale**: The vertical scale of the explosion. Defaults to "scale" if not specified.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddObjective("hitpeds");
	// Show a scaled car explosion where the pedestrian was.
	SetObjExplosion(24, 0.25, 3);
CloseObjective();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddObjective("hitpeds")
	-- Show a scaled car explosion where the pedestrian was.
	Game.SetObjExplosion(24, 0.25, 3)
Game.CloseObjective()
```
{{ endtab }}
{{ endtabs }}

# Notes
This causes the pedestrian that exploded to get removed from the world so they can only be kicked one time.