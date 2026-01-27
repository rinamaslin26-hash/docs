---
title: "SetCondTrigger"
description: "Specify the locator whose triggers will be used for the insidetrigger/outsidetrigger conditions."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 379 # 1.18
---

Specify the locator whose triggers will be used for the [[../MissionConditions/insidetrigger-outsidetrigger.md]] conditions.

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStageCondition.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetCondTrigger( locator_name );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetCondTrigger( locator_name )
```
{{ endtab }}
{{ endtabs }}

* **locator_name**: The name of the locator whose triggers will be used for the condition.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddCondition("insidetrigger");
	SetCondTrigger("z2phone1");
CloseCondition();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddCondition("insidetrigger")
	Game.SetCondTrigger("z2phone1")
Game.CloseCondition()
```
{{ endtab }}
{{ endtabs }}