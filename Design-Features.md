# Major Features of ForgeEssentials
This page is meant to be a listing of all the features of ForgeEssentials to help keep devs on track, and note who is currently working on the task. 
**This is a working document, and should not be taken as a complete feature list.** Some items may be added or removed in the future.

## Pluggable Base Permissions System
These functions are meant to provide server administrators tools to allow/deny actions to players dependant on player status on the server, as well as within custom areas. (Similar to WorldGuard for Bukkit.)

* Configurable permission ranks (Provide a generic set to begin with)
* Basic server permissions (place/remove blocks, allow/deny crafting of certain blocks or items, etc.)
* Plugin framework for mods to specify their own permission classes (eg allow/deny mod's research tree or similar)

## WorldEdit-like functionality
Provides basic world editing commands.

* Select and name volume
* Copy contents of one volume to another location

## WorldGuard-like functionality
Requires functionality provided by the base permissions system and enforces them in a world.

* Enforcement of permissions
* Enforcement of volume permissions