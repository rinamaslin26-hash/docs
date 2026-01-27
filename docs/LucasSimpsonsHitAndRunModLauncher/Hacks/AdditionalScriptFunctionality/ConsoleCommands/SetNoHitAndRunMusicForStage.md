---
title: "SetNoHitAndRunMusicForStage"
description: "Disables the game switching to the Hit & Run music during a Hit & Run for the stage. Instead, the mission's music will continue."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 379 # 1.18
---

Disables the game switching to the Hit & Run music during a Hit & Run for the stage. Instead, the mission's music will continue.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStage.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetNoHitAndRunMusicForStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetNoHitAndRunMusicForStage()
```
{{ endtab }}
{{ endtabs }}

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
	SetNoHitAndRunMusicForStage();

	AddObjective("dummy");
	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage()
	Game.SetNoHitAndRunMusicForStage()

	Game.AddObjective("dummy")
	Game.CloseObjective()
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}