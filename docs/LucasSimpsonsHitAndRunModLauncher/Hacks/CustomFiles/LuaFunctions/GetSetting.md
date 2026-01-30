---
title: "GetSetting"
description: "Returns the value of a setting in a mod."
authors: [ 2 ]
# TODO: initialVersion
---

Returns the value of a setting in a mod.

# Syntax
```lua
GetSetting( <setting_name>, [<mod_name>] )
```

* **setting_name**: The name of the setting to get the value of.
* **mod_name**: The mod you want to get the setting from from. Optional, defaults to the mod that called the function.

# Examples
```lua
-- Get the difficulty setting of the current mod.
local Difficulty = GetSetting("Difficulty")

-- Check some other setting in another mod.
local SomeOtherSetting = GetSetting("SomeOtherSetting","AnotherMod")
```

# Version History
## Version 1.23.10
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.10/Hacks/CustomFiles/LuaFunctions/GetSetting_GetSettings.md }}

## Version 1.13
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.13/Hacks/CustomFiles/LuaFunctions/GetSetting.md }}

## Version 1.12.1
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.12.1/Hacks/CustomFiles/LuaFunctions/GetSetting.md }}