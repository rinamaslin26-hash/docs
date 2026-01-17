---
title: "SetMusicState"
description: "Triggers a music state change upon reaching a stage."
authors: [ 2 ]
---

Triggers a music state change upon reaching a stage.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStage.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetMusicState( state_name, state_value );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetMusicState( state_name, state_value );
```
{{ endtab }}
{{ endtabs }}

* **state_name**: The name of a State in the currently loaded music RadMusic script.
* **state_value**: The name of a value in the State.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
	AddObjective("dummy");
	CloseObjective();

	SetMusicState("Mission2", "Stage1");
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage()
	Game.AddObjective("dummy")
	Game.CloseObjective()

	Game.SetMusicState("Mission2", "Stage1")
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}