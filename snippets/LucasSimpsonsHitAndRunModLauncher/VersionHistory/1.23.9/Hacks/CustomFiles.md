* Improved efficency of the `Output` Lua function for path handlers, particularly when calling it multiple times.
	* Also added a `-legacyoutput` command line argument to opt out of this change.
	* Also added the `IsLegacyOutput` Lua function to detect if that argument is in use.