---
title: "SetObjTotal"
description: "Set the total amount required for various ASF objectives."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 379 # 1.18
---

Sets the total amount required for the following ASF objective types:

* [[../MissionObjectives/collectcoins.md]]
* [[../MissionObjectives/collectwrench.md]]
* [[../MissionObjectives/completedwasps.md]]
* [[../MissionObjectives/destroycars.md]]
* [[../MissionObjectives/event.md]]
* [[../MissionObjectives/hitpeds.md]]
* [[../MissionObjectives/jump.md]]
* [[../MissionObjectives/collectcoins.md]]

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStageObjective.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetObjTotal( total );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetObjTotal( total )
```
{{ endtab }}
{{ endtabs }}

* **total**: The total amount required to pass the objective.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddObjective("jump");
	// Jump 3 times
	SetObjTotal(3);
CloseObjective();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddObjective("jump")
	-- Jump 3 times
	Game.SetObjTotal(3)
Game.CloseObjective()
```
{{ endtab }}
{{ endtabs }}