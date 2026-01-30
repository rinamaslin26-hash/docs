* Made it so the start of Lua file names are truncated instead of the end.
	* Also added `-notruncateluafilenamestart` to opt out of this change.
* Made various improvements to Lua execution errors.
	* They now include the title of the mod that executed the script.
	* They now include a stack trace.
		* Also added `-noluastacktrace` to opt out of this addition.
	* They now get logged to the log files (when "Logging" is enabled in the "Console and Logging" hack).
* Made various improvements to Lua load errors.
	* They now include the title of the mod that loaded the script.
	* They now get logged to the log files (when "Logging" is enabled in the "Console and Logging" hack).