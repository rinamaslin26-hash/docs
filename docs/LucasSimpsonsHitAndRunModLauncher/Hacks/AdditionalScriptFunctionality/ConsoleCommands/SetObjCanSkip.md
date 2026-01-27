---
title: "SetObjCanSkip"
description: "Set whether or not a camera objective can be skipped."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 379 # 1.18
---

Set whether or not a [[../MissionObjectives/camera.md]] can be skipped.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStageObjective.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetObjCanSkip( can_skip );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetObjCanSkip( can_skip )
```
{{ endtab }}
{{ endtabs }}

* **can_skip** : Whether or not the player can skip the objective. 
    * Defaults to 0 / false.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddObjective("camera");
	SetObjCameraName("mission0camShape");
	SetObjMulticontName("mission0cam");

	// Let the player skip the camera animation.
	SetObjCanSkip(1);
CloseObjective();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddObjective("camera")
	Game.SetObjCameraName("mission0camShape")
	Game.SetObjMulticontName("mission0cam")

	-- Let the player skip the camera animation.
	Game.SetObjCanSkip(1)
Game.CloseObjective()
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.

# Version History
## 1.18.1
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.18.1/Hacks/AdditionalScriptFunctionality/Booleans.md }}