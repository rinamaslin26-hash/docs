---
title: "GetModTitle"
description: "Returns the title of the specified mod or the current mod if none is specified."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 388 # 1.22
---

Returns the title of the specified mod or the current mod if none is specified.

This returns `nil` if called with the name of a mod that is not enabled.

# Syntax
```lua
GetModTitle( [<mod_name>] )
```

* **mod_name**: The name of the mod whose title you'd like to get.

# Examples
```lua
local CurrentModTitle = GetModTitle()

print(CurrentModTitle .. " loaded!")
```