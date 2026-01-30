### General
* Added an `[AdditionalFiles]` section to the hack's configuration file.
	* This allows you to define any number of additional files to be loaded when a particular file is requested.
	* This is useful for the new husk features of Custom Car Support, allowing you to keep a car specific husk model separate and have it get loaded alongside the regular car model.

### Lua Scripting
* {{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.24/Hacks/CustomFiles/LuaFunctions/ReadFile.md }}
* {{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.24/Hacks/CustomFiles/LuaFunctions/UseCallbacks.md }}
* Added the `ReadFileOffset` function.
	* This allows you to read part of a file.