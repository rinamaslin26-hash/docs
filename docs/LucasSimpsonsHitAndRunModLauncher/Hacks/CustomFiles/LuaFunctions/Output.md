---
title: "Output"
description: "Outputs text or binary data to a virtual file in memory which is then handed off to the game in place of the file it requested."
authors: [ 2 ]
# TODO: initialVersion
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/CustomFiles/MustBeCalledInPathHandler.md }}

Outputs text or binary data to a virtual file in memory which is then handed off to the game in place of the file it requested.

# Syntax
```lua
Output( <string> )
```

* **string**: The string to output to the virtual file.

# Examples
```lua
-- Example that would be used in a PathHandler on an MFK script
Output([[
    LoadP3DFile("art\\cars\\famil_v.p3d");
]])
```

# Version History
## Version 1.24
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.24/Hacks/CustomFiles/LuaFunctions/UseCallbacks.md }}

## Version 1.23.9
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.9/Hacks/CustomFiles/LuaFunctions/Output.md }}