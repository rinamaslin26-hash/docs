---
title: "SetHitAndRunDecayInterior"
description: "Set the amount the Hit & Run meter will decay each second while the player is in an interior."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 379 # 1.18
---

Set the amount the Hit & Run meter will decay each second while the player is in an interior.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/LevelInit.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetHitAndRunDecayInterior( decay_rate );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetHitAndRunDecayInterior( decay_rate )
```
{{ endtab }}
{{ endtabs }}

* **decay_rate**: The rate at which the meter will decay while in an interior.
    * Defaults to 6.0.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
SetHitAndRunDecayInterior(6.0);
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetHitAndRunDecayInterior(6.0)
```
{{ endtab }}
{{ endtabs }}

# Notes
This command replaces the game's incorrectly mapped [[/TheSimpsonsHitAndRun/Scripting/ConsoleCommands/SetHitAndRunDecayInterior.md]] command.