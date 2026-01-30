---
title: "GetModVersion"
description: "Returns the version of the specified mod or the current mod if none is specified."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 388 # 1.22
---

Returns the version of the specified mod or the current mod if none is specified.

# Syntax
```lua
GetModVersion( [<mod_name>] )
```

* **mod_name**: The name of the mod whose version you'd like to get.

# Examples
```lua
local CurrentModVersion = GetModVersion()

print("Version " .. CurrentModVersion .. " loaded!")
```