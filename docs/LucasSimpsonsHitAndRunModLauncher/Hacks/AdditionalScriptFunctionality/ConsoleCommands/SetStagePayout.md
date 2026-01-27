---
title: "SetStagePayout"
description: "Set an amount of coins to give the player when they complete the stage."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 379 # 1.18
---

Set an amount of coins to give the player when they complete the stage.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStage.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetStagePayout( coins );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetStagePayout( coins ) 
```
{{ endtab }}
{{ endtabs }}

* **coins**: The amount of coins to give the player upon completing the stage.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddStage();
	// Free 25 coins when you finish this stage.
	SetStagePayout(25);
		
	AddObjective("dummy");
	CloseObjective();
CloseStage();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddStage() 
	-- Free 25 coins when you finish this stage.
	Game.SetStagePayout(25)

	Game.AddObjective("dummy")
	Game.CloseObjective()
Game.CloseStage()
```
{{ endtab }}
{{ endtabs }}