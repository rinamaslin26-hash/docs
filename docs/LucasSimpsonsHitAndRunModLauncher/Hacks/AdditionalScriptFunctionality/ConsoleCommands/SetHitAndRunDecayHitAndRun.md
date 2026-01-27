---
title: "SetHitAndRunDecayHitAndRun"
description: "Set the amount the Hit & Run meter will decay each second while the player is in a Hit & Run."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 379 # 1.18
---

Set the amount the Hit & Run meter will decay each second while the player is in a Hit & Run.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/LevelInit.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetHitAndRunDecayHitAndRun( decay_rate );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetHitAndRunDecayHitAndRun( decay_rate )
```
{{ endtab }}
{{ endtabs }}

* **decay_rate**: The rate at which the meter will decay while in a Hit & Run. 
    * Defaults to 10.0.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
SetHitAndRunDecayHitAndRun(6.0);
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetHitAndRunDecayHitAndRun(6.0)
```
{{ endtab }}
{{ endtabs }}