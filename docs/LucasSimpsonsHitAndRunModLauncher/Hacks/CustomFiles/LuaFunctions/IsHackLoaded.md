---
title: "IsHackLoaded"
description: "Returns whether or not a hack is loaded."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 370 # 1.15.2
---

Returns whether or not a hack is loaded.

# Syntax
```lua
IsHackLoaded( <hack_name> )
```

* **hack_name**: The InternalName of the hack.

# Examples
```lua
-- Will always return true because Hack Support is always enabled
print(IsHackLoaded("HackSupport"))

-- Check if CustomShopSupport is loaded
print(IsHackLoaded("CustomShopSupport"))

-- Mod Hacks can be checked with this or IsModEnabled
print(IsHackLoaded("DebugText"))
```