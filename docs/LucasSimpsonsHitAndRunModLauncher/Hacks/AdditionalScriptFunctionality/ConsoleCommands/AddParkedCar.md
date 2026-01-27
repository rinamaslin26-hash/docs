---
title: "AddParkedCar"
description: "Adds a car to the parked cars list for the level. This can be used to add a parked car without also adding it to a traffic group."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 388 # 1.22
---

Adds a car to the parked cars list for the level.

This can be used to add a parked car without also adding it to a traffic group using [[/TheSimpsonsHitAndRun/Scripting/ConsoleCommands/AddTrafficModel.md]].

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/LevelInit.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
AddParkedCar( car_name );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddParkedCar( car_name )
```
{{ endtab }}
{{ endtabs }}

* **car_name**: The name of the car to add to the parked cars list.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddParkedCar("famil_v");
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddParkedCar("famil_v")
```
{{ endtab }}
{{ endtabs }}