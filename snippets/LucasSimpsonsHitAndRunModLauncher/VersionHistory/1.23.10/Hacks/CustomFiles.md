### General
* Made this hack enable [Data Execution Prevention](https://docs.microsoft.com/en-us/windows/win32/memory/data-execution-prevention) if any mods provide custom files, path redirections, path handlers or an AdditionalFiles folder.
	* Also added the `-noenabledep` command line argument to opt out of this.

### Lua Scripting
* Made the `math.random` function use a 64-bit Mersenne Twister 19937 random number generator initially seeded (at load time) with a cryptographically secure random number instead of just using a cryptographically secure random number.
* Added the `math.randomseed` function. This allows you to set the seed on a sandboxed, per-mod, basis.
	* See [this page](http://lua-users.org/wiki/MathLibraryTutorial) for more details on this function.
* {{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.10/Hacks/CustomFiles/LuaFunctions/GetSetting_GetSettings.md }}
	* If you'd like, you can use something like `if SettingValue > 2147483647 then SettingValue = SettingValue - 4294967296 end` to support old versions of the Mod Launcher.
* Fixed a bug where `coroutine.isyieldable` wasn't allowed.
* Removed functions from the global table that don't get copied into mod environments as is.
* {{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.23.10/Hacks/CustomFiles/LuaFunctions/DirectoryGetEntries.md }}
* Added the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/CustomFiles/LuaFunctions/GetShared.md]] function.
	* This returns a table that is shared by all mods.
* Added the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/CustomFiles/LuaFunctions/Pause.md]] function.
	* This will pause the console and prompt the user to "Press any key to continue...".
	* If the Console feature of the Console and Logging hack is not enabled, a console window will still be shown temporarily to prompt the user.
* Added the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/CustomFiles/LuaFunctions/IsDemo.md]] function.
	* This returns true when the user is playing the Demo version of the game.