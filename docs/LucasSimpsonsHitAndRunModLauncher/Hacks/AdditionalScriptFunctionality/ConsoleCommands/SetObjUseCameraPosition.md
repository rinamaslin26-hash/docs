---
title: "SetObjUseCameraPosition"
description: "Set whether or not the game should use the camera's position for spawning traffic and pedestrians during a camera objective."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 379 # 1.18
---

Set whether or not the game should use the camera's position for spawning traffic and pedestrians during a [[../MissionObjectives/camera.md]] objective.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStageObjective.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetObjUseCameraPosition( use_camera_position );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetObjUseCameraPosition( use_camera_position )
```
{{ endtab }}
{{ endtabs }}

* **use_camera_position**: Set whether or not to use the camera position. 
    * Defaults to 0.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddObjective("camera");
	SetObjCameraName("mission0camShape");
	SetObjMulticontName("mission0cam");

	SetObjUseCameraPosition(0);
CloseObjective();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddObjective("camera")
	Game.SetObjCameraName("mission0camShape")
	Game.SetObjMulticontName("mission0cam")

	Game.SetObjUseCameraPosition(0)
Game.CloseObjective()
```
{{ endtab }}
{{ endtabs }}