---
title: "SetCarChangeHitAndRunChange"
description: "Set the amount the Hit & Run meter will change when swapping to a different vehicle."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 379 # 1.18
---

Set the amount the Hit & Run meter will change when swapping to a different vehicle.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/LevelInit.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetCarChangeHitAndRunChange( change_amount );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetCarChangeHitAndRunChange( change_amount )
```
{{ endtab }}
{{ endtabs }}

* **change_amount**: The amount that will be added to the Hit & Run meter when changing your car. 
    * Defaults to -100.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
SetCarChangeHitAndRunChange(-100);
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetCarChangeHitAndRunChange(-100)
```
{{ endtab }}
{{ endtabs }}