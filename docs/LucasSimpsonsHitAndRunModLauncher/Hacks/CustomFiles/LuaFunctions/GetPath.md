---
title: "GetPath"
description: "Returns the path of the file being requested."
authors: [ 2 ]
# TODO: initialVersion
---

{{ Snippet:LucasSimpsonsHitAndRunModLauncher/Hacks/CustomFiles/MustBeCalledInPathHandler.md }}

Returns the path of the file being requested.

# Syntax
```lua
GetPath()
```

# Examples
```lua
local CurrentPath = GetPath()

if ComparePaths(CurrentPath, "scripts\\missions\\rewards.mfk") then
    -- Do something based on it being the rewards file.
else
    -- Do something else, nothing probably with this example
end
```

# Version History
## Version 1.24
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.24/Hacks/CustomFiles/LuaFunctions/UseCallbacks.md }}