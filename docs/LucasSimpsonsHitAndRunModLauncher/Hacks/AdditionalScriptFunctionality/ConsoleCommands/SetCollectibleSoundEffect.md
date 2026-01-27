---
title: "SetCollectibleSoundEffect"
description: "Sets the sound effect to use when collecting an item in a delivery, dump or race objective."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main Branch
  projectBranchVersion_id: 398 # 1.23.5
---

Sets the sound effect that plays when collecting an item in the following objectives:

* [[/TheSimpsonsHitAndRun/Scripting/MissionObjectives/delivery.md]]
* [[/TheSimpsonsHitAndRun/Scripting/MissionObjectives/dump.md]]
* [[/TheSimpsonsHitAndRun/Scripting/MissionObjectives/race.md]]

# Scope
{{ Snippet:TheSimpsonsHitAndRun/Scripting/ConsoleCommands/Scopes/MissionInitStageObjective.md }}

# Syntax
{{ tabs }}
{{ tab MFK }}
```js
SetCollectibleSoundEffect( sound_resource_name );
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetCollectibleSoundEffect( sound_resource_name )
```
{{ endtab }}
{{ endtabs }}

* **sound_resource_name**: The name of the sound resource to play.
    * **none**: No sound will play when picking up collectibles for the stage.
    * Default varies by level and in one case by mission:
        * Level 1: `level_1_pickup_sfx`
        * Level 2: `level_2_pickup_sfx`
        * Level 2 Mission 6: `monkey_collect`
        * Level 3: `level_3_pickup_sfx`
        * Level 4: `level_4_pickup_sfx`
        * Level 5: `level_5_pickup_sfx`
        * Level 6: `level_6_pickup_sfx`
        * Level 7: `nuclear_waste_collect`

# Examples
{{ tabs }}
{{ tab MFK }}
```js
SetCollectibleSoundEffect("W_Idlereply_Moe_genitalsA");
```
{{ endtab }}
{{ tab Lua }}
```lua
Game.SetCollectibleSoundEffect("W_Idlereply_Moe_genitalsA")
```
{{ endtab }}
{{ endtabs }}