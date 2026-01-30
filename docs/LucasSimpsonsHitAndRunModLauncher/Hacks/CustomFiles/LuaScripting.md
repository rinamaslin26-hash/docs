---
title: "Lua Scripting"
description: "This hack utilises the Lua Support hack to allow mods to run Lua code to handle files when the game requests they be loaded."
authors: [ 2 ]
---

This hack utilises the [[../LuaSupport.md]] hack to allow mods to run Lua code to handle files when the game requests they be loaded. 

Mods can define Lua code in two places:

* `CustomFiles.lua`: This is a script located in the root of the mod that will be executed as soon as the mod is loaded.
* Path Handlers: Mods can specify Lua scripts that will be executed when a specific file or files (via wildcards) are requested by the game using the `CustomFiles.ini` configuration file.
	* These scripts are intended to go somewhere in a folder named "Resources" in the root of the mod.

This allows mods to do a number of powerful things such as redirect or manipulate the files being requested or generate new ones altogether.

# Allowed Functions/Variables
For a list of all of the stock Lua functions and variables that are allowed with this hack, see [[AllowedLuaFunctionsAndVariables.md]].

# Custom Functions
For a list of custom functions this hack provides, see [[LuaFunctions/AllFunctions.md]].