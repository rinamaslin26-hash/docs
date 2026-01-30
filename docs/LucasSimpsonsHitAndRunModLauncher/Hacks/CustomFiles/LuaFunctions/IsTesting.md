---
title: IsTesting
description: "Returns whether or not the user is currently using the -testing command line argument on the Mod Launcher."
authors: [ 2 ]
initialVersion:
  project_id: 6 # Lucas' Simpsons Hit & Run Mod Launcher
  projectBranch_id: 46 # Main
  projectBranchVersion_id: 383 # 1.19
---

Returns whether or not the user is currently using the `-testing` [[../../../CommandLineArguments.md|command line argument]].

# Syntax
```lua
IsTesting()
```

# Examples
```lua
local IsTestingLauncher = IsTesting()
```