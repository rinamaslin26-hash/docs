---
title: "IsModEnabled"
description: "Returns whether or not a mod, mod hack or framework is enabled."
authors: [ 2 ]
# TODO: initialVersion
---

Returns whether or not a mod, mod hack or framework is enabled.

# Syntax
```lua
IsModEnabled( <mod_name> )
```

* **mod_name**: The name of the mod to check for. This should be the mod's InternalName (if it has one, which it should).

# Examples
```lua
if IsModEnabled("ReplayableBonusMissions") then
    -- Do stuff differently if the Replayable Bonus Missions Mod Hack is enabled.
end
```

# Version History
## Version 1.13
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.13/Hacks/CustomFiles/LuaFunctions/IsModEnabled.md }}