---
title: "Redirect"
description: "Redirect the file being requested to a different path."
authors: [ 2 ]
# TODO: initialVersion
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/CustomFiles/MustBeCalledInPathHandler.md }}

Redirect the file being requested to a different path.

# Syntax
```lua
Redirect( <path> )
```

* **path**: The path to redirect this file to.

# Examples
```lua
-- Example redirection to a random file in the Mod's Resources folder.
local FilePath = GetModPath() .. "/Resources/example/"

local Files = {"example.p3d","example2.p3d","example3.p3d"}

Redirect(FilePath .. Files[math.random(1, #Files)])
```

# Version History
## Version 1.24
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.24/Hacks/CustomFiles/LuaFunctions/UseCallbacks.md }}