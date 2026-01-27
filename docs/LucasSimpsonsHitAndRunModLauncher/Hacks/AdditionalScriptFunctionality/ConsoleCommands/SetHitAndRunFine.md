---
title: "SetHitAndRunFine"
description: "Set the amount of coins the player will be fined if they are caught in a Hit & Run."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 379 # 1.18
---

Set the amount of coins the player will be fined if they are caught in a Hit & Run.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/LevelInit.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetHitAndRunFine( fine_amount );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetHitAndRunFine( fine_amount )
```
{{ endtab }}
{{ endtabs }}

* **fine_amount**: The amount to fine the player if they get caught. 
    * Defaults to 50.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
SetHitAndRunFine(69); // Nice
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetHitAndRunFine(69) -- Nice
```
{{ endtab }}
{{ endtabs }}