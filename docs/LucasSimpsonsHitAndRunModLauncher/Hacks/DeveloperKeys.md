---
title: "Developer Keys"
description: "This hack adds key binds that are useful for mod developers."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 294 # 1.27
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/Headers/CanBeEnabledOnSettingsPage.md }}

This hack adds key binds that are useful for mod developers.

# Keybinds
| Key      | Function                                                                                    |
|----------|---------------------------------------------------------------------------------------------|
| 0        | Reset your Hit & Run meter.                                                                 |
| 2        | Double Speed.                                                                               |
| 3        | Stop your car.                                                                              |
| 5        | Invert your car's speed.                                                                    |
| 6        | Repair your car.                                                                            |
| 7        | Makes your car jump.                                                                        |
| F4       | Teleport your car to you or shows a phone booth interface if you do not already have a car. |
| F7       | Teleport your car or character forwards.                                                    |
| Shift+F4 | Shows a phone booth interface.                                                              |

# Settings
## Keybinds
### Toggle Map Debug View
The key used to toggle debug rendering of various types of map data.

**Defaults to F2.**

### Reload Map Regions
The key used to reload all currently loaded map regions.

**Defaults to F3.**

# Map Debug Views
What exactly he **Toggle Map Debug View** key does depends on if the [[DebugTest.md]] hack is also enabled.

Without Debug Test, the key simply toggles the game's **Show Tree** [[/TheSimpsonsHitAndRun/Cheats.md|cheat]].

With Debug Test, it cycles through various modes:
* Drawing the current [[/Pure3DFiles/ChunkTypes/Intersect.md]] chunk
* Drawing the current [[/Pure3DFiles/ChunkTypes/Intersect.md]] chunk and current the [[/Pure3DFiles/ChunkTypes/Tree.md]] chunk
* Drawing all currently loaded [[/Pure3DFiles/ChunkTypes/TriggerVolume.md]] chunks
* Drawing all currently loaded [[/Pure3DFiles/ChunkTypes/Intersectiond.md]] chunks and [[/Pure3DFiles/ChunkTypes/Road.md]] chunks (without directional arrows)
* Drawing all currently loaded [[/Pure3DFiles/ChunkTypes/Intersectiond.md]] chunks and [[/Pure3DFiles/ChunkTypes/Road.md]] chunks (with directional arrows)
* Drawing all currently loaded [[/Pure3DFiles/ChunkTypes/Path.md]] chunks
* Drawing all currently loaded [[/Pure3DFiles/ChunkTypes/Fence.md]] chunks

This limitation exists because of how the code of these two hacks is currently structured, but we hope to remove this limitation in a future update.