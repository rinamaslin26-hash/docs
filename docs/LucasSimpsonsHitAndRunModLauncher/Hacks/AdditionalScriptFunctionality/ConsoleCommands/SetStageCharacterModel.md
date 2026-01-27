---
title: "SetStageCharacterModel"
description: "Set the player character's model for the stage."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 379 # 1.18
---

Set the player character's model for the stage.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStage.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetStageCharacterModel( model, [animation_set] );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetStageCharacterModel( model, [animation_set] )
```
{{ endtab }}
{{ endtabs }}

* **model**: The character model to use.
* **animation_set**: The animation set to use.
    * Optional, defaults to the current player character's animation set as of 1.19.
    * Using anything else can cause issues.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
    // Switch to Homer's Muumuu costume for the stage.
	SetStageCharacterModel("h_fat");

	AddObjective("dummy");
    CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage()
    -- Switch to Homer's Muumuu costume for the stage.
	Game.SetStageCharacterModel("h_fat")

	Game.AddObjective("dummy")
    Game.CloseObjective()
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}

# Notes
No additional notes.

# Version History
## Version 1.19
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.19/Hacks/AdditionalScriptFunctionality/ConsoleCommands/SetStageCharacterModel.md }}

## Version 1.18.1
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.18.1/Hacks/AdditionalScriptFunctionality/ConsoleCommands/SetStageCharacterModel.md }}