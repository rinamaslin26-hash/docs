---
title: "UseCallbacks"
description: "Builds a file as the game requests it using callback functions."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 383 # 1.19
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/CustomFiles/MustBeCalledInPathHandler.md }}

Builds a file as the game requests it using callback functions.

# Syntax
```lua
UseCallbacks( <length>, <read_callback>, <close_callback> )
```

* **length**: The filesize of the file in bytes.
* **read_callback**: This callback function will get called each time the game tries to read from the file.
* **close_callback**: This callback gets called when the game is done with the file.

# Examples
TODO

# Version History
## Version 1.24
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.24/Hacks/CustomFiles/LuaFunctions/UseCallbacks.md }}