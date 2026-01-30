### Lua Scripting
* Added several previously inaccessible Lua provided functions.
	* assert
	* collectgarbage
	* debug.debug
	* debug.gethook
	* debug.getlocal
	* debug.getmetatable
	* debug.getregistry
	* debug.getupvalue
	* debug.getuservalue
	* debug.sethook
	* debug.setlocal
	* debug.setmetatable
	* debug.setupvalue
	* debug.setuservalue
	* debug.upvaluejoin
	* getmetatable
	* math.maxinteger
	* math.mininteger
	* math.tointeger
	* math.type
	* math.ult
	* os.setlocale
	* rawequal
	* rawget
	* rawlen
	* rawset
	* setmetatable
	* string.dump
	* string.pack
	* string.packsize
	* string.unpack
	* table.concat
	* table.move
	* table.pack
* {{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.13/Hacks/CustomFiles/LuaFunctions/IsModEnabled.md }}
* {{ Snippet:LucasSimpsonsHitAndRunModLauncher/VersionHistory/1.13/Hacks/CustomFiles/LuaFunctions/GetSetting.md }}
* Updated `math.random` to support integers.