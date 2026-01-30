### General
* Fixed an assert when attempting to enable [Data Execution Prevention](https://docs.microsoft.com/en-us/windows/win32/memory/data-execution-prevention) in a couple cases:
	* When the [SetProcessDEPPolicy](https://docs.microsoft.com/en-us/windows/win32/api/winbase/nf-winbase-setprocessdeppolicy) API is not implemented (such as when running in Wine).
	* When the system DEP policy is set to "AlwaysOff" or "AlwaysOn".

### Lua Scripting
Added the [[/LucasSimpsonsHitAndRunModLauncher/Hacks/CustomFiles/LuaFunctions/GetGameLanguage.md]] function.

This allows you to check what language version of the game the user is playing.