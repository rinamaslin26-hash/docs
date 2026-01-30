---
title: "Virtual File System"
description: "This hack has a virtual file system where various folders are mounted for easy access."
authors: [ 2 ]
---

This hack has a virtual file system where various folders are mounted for easy access.
 
# Mount Points
This hack various mount points within its virtual file system.

## /GameData
Allows access to files within the game's install directory (not including within RCF files) and within the "CustomFiles" folder of any enabled mod.

## /GameDir
Allows direct access to the game's install directory (bypassing any "CustomFiles" folders).

## /Mods/MODNAME
Allows access to the folder of any enabled mod via it's `InternalName`.

## /UserData/SavedGames
Allows access to the current saved games directory.

This could be the game directory if no main mod is enabled (depending on the user's **Always Keep Saved Games Separate** setting in the [[../../Settings.md|launcher's settings]]) or the main mod's saved games directory within the launcher's saved games directory if a main mod is enabled.

## /UserData/Screenshots
Allows access to the screenshots directory (or the folder inside the screenshots directory for the current main mod if a main mod is enabled).

## /UserData/Settings
Allows access to the folder containing "simpsons.ini".

This may be the same as `/GameData` depending on the user's **Keep Game Settings Separate** setting in the [[../../Settings.md|launcher's settings]]. 