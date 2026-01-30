### General
Added various Console output messages.

### Lua Scripting
* Now uses the Lua Support hack.
    * This means this version effectively upgrades from Lua 5.2.3 to 5.3.1.
		* This change also removes the following functions:
			* math.atan2
			* math.cosh
			* math.frexp
			* math.ldexp
			* math.log10
			* math.pow
			* math.sinh
			* math.tanh
			* table.maxn
		* This also makes the `utf8` library available.
* Made the `coroutine` library available.
* Removed support for compiled Lua files.