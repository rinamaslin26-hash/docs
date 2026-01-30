### General
Fixed a bug where [Data Execution Prevention](https://docs.microsoft.com/en-us/windows/win32/memory/data-execution-prevention) was enabled on executables that don't support it.

### Lua Scripting
* Removed the "interval too large" check from the `math.random` function.
	* Previously, the range could not be more than 9,223,372,036,854,775,807 (the value of `math.maxinteger`).
	* This limitation no longer applies to this implementation of `math.random` so this check has been removed.
* Made `math.randomseed` not get the argument as a double precision floating point and cast it to a 64-bit integer.