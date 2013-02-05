lets try to keep a changelog
just ignore the wiki style
try to keep changelog to stuff that is important towards the users.


**1.1.1.xxx**

1. Added
 * Added check for headroom in /bed [#](https://github.com/ForgeEssentials/ForgeEssentialsMain/commit/ea6b64c75892064af006aad1d28f437485da54b1)
 * added version check handler [#](https://github.com/ForgeEssentials/ForgeEssentialsMain/commit/3d4351ef7785798deb1eeb43cbb83492039b0cc3)
2. Changed
 * modified the chat layout for the capabilities command [#](https://github.com/ForgeEssentials/ForgeEssentialsMain/commit/8094ee0db46bb365d60e886eae4c47bdeac90bd5)
 * Better border system. (Uses moveEvent) [#](https://github.com/ForgeEssentials/ForgeEssentialsMain/commit/1603deb889fff62e27ac6d7017f67dcb5a9d4d6e)
3. Fixed
 * banneditems.cfg misbehaving [#](https://github.com/ForgeEssentials/ForgeEssentialsMain/commit/8230df5eb3971a83296aab66707133d76bc8949e)
4. Removed

**1.1.1.251**

1. Added
2. Changed
3. Fixed
4. Removed

**1.1.1**

1. Added
 * Added user and group perms listing to console parsing
2. Changed
 * Changed permission table names to fepermission_<tableName>
3. Fixed
 * Fixed issue where perms on a user wernt checked correctly
 * Fixed an issue with the SUPER permisisons
 * Fixed issue with perms not being removed from groups with clear
 * Fixed /spawn permission checking and notification
 * Fixed permissions exporting and importing (no more lost groups)
 * Fixed case-sensitive issue with H2 (everything in db is now totally case-insensitive, including perm node checks)

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
3. Fixed
 * Forever fixed H2 "host not found" error
 * Fixed zone area calculations
 * Fixed censor filter
 * Fixed teleportation glitches
 * Fixed bug where duplicate command removal as removing ForgeEssentials commands and not vanilla commands
 * Fixed /feperm export for MySQL
4. Removed
  * Removed <x y z> functionality of /home command

**1.0.0**
 * initial release