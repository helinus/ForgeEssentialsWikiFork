lets try to keep a changelog
just ignore the wiki style
try to keep changelog to stuff that is important towards the users.


**1.1.1.xxx**

-added

-removed

-changed/fixed

modified the chat layout for the capabilities command

**1.1.1.251**

+added

-removed

-fixed

**1.1.1**


Changed permission table names to fepermission_<tableName>

Fixed issue where perms on a user wernt checked correctly

Fixed an issue with the SUPER permisisons

Added user and group perms listing to console parsing

Fixed issue with perms not being removed from groups with clear

Fixed /spawn permission checking and notification

Fixed permissions exporting and importing (no more lost groups)

Fixed case-sensitive issue with H2 (everything in db is now totally case-insensitive, including perm node checks)

**1.1.0**

Added update.sql for help in updating database structures.

Reverted /spawn and spawn system to vanilla. Pending overhaul in 1.2

Forever fixed H2 "host not found" error

Fixed zone area calculations

Fixed censor filter

Fixed teleportation glitches

Moved WorldControl config file

Redid /rules command

Fixed bug where duplicate command removal as removing ForgeEssentials commands and not vanilla commands

Changed chat error color to dark red

Added Module Overriding to the API

Added permissions hooks and checks to the API

Added DataAPI to the API

Added permission lists for players and groups
Added /feperm default command for setting/adding default groups
Added admin-type nodes for some commands (warp.set,
Removed <x y z> functionality of /home command
Added @token parsing for player and console commands
Added CommandBlock functionality for every Commands module command that could work it
Added ability to modify permissions settings for offline and non-existent players, with a warning
Fixed /feperm export for MySQL
Changed prefix and suffix parsing to allow for group prefixes to color usernames
1.0.0
initial release

