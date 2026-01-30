---
title: "GetEnabledMods"
description: "Calls the given callback function for each mod that is enabled."
authors: [ 2 ]
# TODO: InitialVersion
---

Calls the given callback function for each mod that is enabled.

# Syntax
```lua
GetEnabledMods( <callback> )
```

* **callback**: The callback that will be called for each enabled mod.
    * This callback is given one argument:
        * **ModInternalName**: The InternalName of the mod.
    * This callback must return true for the loop to continue.

# Examples
```lua
-- Print the InternalName of each enabled mod/hack
GetEnabledMods(function(ModInternalName) 
	print(ModInternalName)
	return true
end)
```