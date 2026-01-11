---
title: "SetCharactersVisible"
description: "Sets the visibility of the driver and the passenger in a vehicle."
authors: [ 2, 104 ]
---

This command sets the visibility of the driver and the passenger in a vehicle.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/ConsoleCommands/Scopes/CarCon.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetCharactersVisible( visibility );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetCharactersVisible( visibility )
```
{{ endtab }}
{{ endtabs }}

* **visibility**: Sets whether or not the characters are visible.
    * Defaults to 1.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
SetCharactersVisible(1);
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetCharactersVisible(1)
```
{{ endtab }}
{{ endtabs }}