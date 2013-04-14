**1.2.0**

1. Added
 * Permissions for PvP, itemuse, mob spawns
 * Entry/exit messages for zones
 * [Tickets](https://github.com/ForgeEssentials/ForgeEssentialsMain/wiki/Ticket-Module)
 * [Afterlife (deathchests, the like)](https://github.com/ForgeEssentials/ForgeEssentialsMain/wiki/Afterlife-Module)
 * [Auth](https://github.com/ForgeEssentials/ForgeEssentialsMain/wiki/Authentication-Module)
 * Selection highlighting for PlayerLogger
 * [MCStats integration](http://mcstats.org/plugin/ForgeEssentials)
 * Changes to economy module
 * PermissionsList.txt - list of all possible permission nodes
 * Commands module now has alias configuration

2. Changed
 * Permissions are exported on first load
 * Selection commands - //wand to //fewand, //pos to //fepos, //deselect to //fedeselect.
 * /setspawn is now precise to a point

3. API additions (for modders)
 * Added marker for entities for /butcher

**1.1.1**

1. Added
 * Added user and group perms listing to console parsing
 * /locate command
 * Check for headroom in /bed
 * Version check handler

2. Changed
 * Changed permission table names to fepermission_<tableName>
* Modified chat layout for /capabilities
* Better border system
* Reworked /tps

**1.1.0**

1. Added
 * Added update.sql for help in updating database structures.
 * Added Module Overriding to the API
 * Added permissions hooks and checks to the API
 * Added DataAPI to the API
 * Added permission lists for players and groups
 * Added /feperm default command for setting/adding default groups
 * Added admin-type nodes for some commands (warp.set)
 * Added @token parsing for player and console commands
 * Added CommandBlock functionality for every Commands module command that could work it
 * Added ability to modify permissions settings for offline and non-existent players, with a warning
2. Changed
 * Reverted /spawn and spawn system to vanilla. Pending overhaul in 1.2
 * Changed chat error color to dark red
 * Moved WorldControl config file
 * Redid /rules command
 * Changed prefix and suffix parsing to allow for group prefixes to color usernames
4. Removed
  * Removed <x y z> functionality of /home command

**1.0.0**
 * initial release