---
title: "SetCondTotal"
description: "Set the total amount required to fail various ASF conditions."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 379 # 1.18
---

Sets the total amount required to fail the following ASF conditions:

* [[../MissionConditions/collectcoins.md]]
* [[../MissionConditions/collectwrench.md]]
* [[../MissionConditions/destroycars.md]]
* [[../MissionConditions/event.md]]
* [[../MissionConditions/hitpeds.md]]
* [[../MissionConditions/jump.md]]

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStageCondition.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetCondTotal( total );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetCondTotal( total )
```
{{ endtab }}
{{ endtabs }}

* **total**: The total amount required to fail the condition.

# Examples
{{ tabs }}
{{ tab MFK }}
```js
AddCondition("jump");
	// Jump 3 times
	SetCondTotal(3);
CloseCondition();
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.AddCondition("jump")
	-- Jump 3 times
	Game.SetCondTotal(3)
Game.CloseCondition()
```
{{ endtab }}
{{ endtabs }}