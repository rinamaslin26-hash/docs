### General
* Made `CustomFiles.lua` execute after all hacks that are supposed to be loaded are loaded.
* Made this hack only mount **CustomFiles** folders that exist.
    * This change can dramatically improve performance if you have lots of mods enabled but only a few have CustomFiles folders (like Mod Hacks for instance).

### Lua Scripting
* Added the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/CustomFiles/LuaFunctions/GetLauncherVersion.md]] function.
	* This returns the current version of the Mod Launcher.
* Added the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/CustomFiles/LuaFunctions/GetMainMod.md]] function.
	* This returns the InternalName of the current main mod (if there is one).
* Added the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/CustomFiles/LuaFunctions/GetSettings.md]] function.
	* This returns the settings of the current mod (or the specified mod) in a Lua table.
* Added the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/CustomFiles/LuaFunctions/IsTesting.md]] function.
	* This checks if the user is has the Mod Launcher's testing mode enabled.
* Added the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/CustomFiles/LuaFunctions/UseCallbacks.md]] function.
	* This is an advanced function for handling files with Lua that may or may not have a use case.
* {{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.19/Hacks/CustomFiles/LuaFunctions/ComparePaths.md }}