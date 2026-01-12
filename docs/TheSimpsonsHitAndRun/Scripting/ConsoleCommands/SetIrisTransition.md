---
title: "SetIrisTransition"
description: "Sets whether or not there should be an iris transition upon entering a vehicle."
authors: [ 104 ]
---

This command sets whether or not there should be an iris transition upon entering a vehicle.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/CarCon.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetIrisTransition( iris );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetIrisTransition( iris )
```
{{ endtab }}
{{ endtabs }}

* **iris**: Sets whether or not there should be an iris transition upon entering a vehicle.
    * Defaults to 0.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
SetIrisTransition(0);
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetIrisTransition(0)
```
{{ endtab }}
{{ endtabs }}

# Notes
This command overrides [[SetHasDoors.md]] in the event that both are present.