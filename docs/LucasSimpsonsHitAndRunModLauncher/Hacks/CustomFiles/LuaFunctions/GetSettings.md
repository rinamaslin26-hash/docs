---
title: "GetSettings"
description: "Returns the values of all of the settings of the a mod as a table."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 383 # 1.19
---

Returns the values of all of the settings of the a mod as a table.

# Syntax
```lua
GetSettings( [<mod_name>] )
```

* **mod_name**: The mod you want to get setting values from. 
    * Optional, defaults to the mod that called the function.

# Examples
```lua
-- Get settings of the current mod
local Settings = GetSettings()

-- Get settings of another mod
local Settings = GetSettings("AnotherMod")
```

# Notes
When returning the value of MultipleChoice type settings this function returns them 1 based instead of 0 based like the older [[GetSetting.md]] function.

```lua
-- To demonstrate, here's an example.
-- For this example, let's assume that the Difficulty setting is on the first Option.

-- Difficulty would be 0
local Difficulty = GetSetting("Difficulty")
​
-- Settings.Difficulty would be 1
local Settings = GetSettings()
```

# Version History
## Version 1.23.10
{{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.10/Hacks/CustomFiles/LuaFunctions/GetSetting_GetSettings.md }}