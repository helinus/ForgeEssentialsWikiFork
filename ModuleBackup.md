* [Configuration](#config)
* [Usage](#use)
* [Commands](#command)
* [AutoBackup](#autobackup)
* [AutoRemove](#autoremove)

# Warning
Word of warning:
Do NOT change anything in the backup folder. Only copy out of the folder and change there. If you make changes to the folder structure, if WILL mess up the AutoRemove system.

# Configuration <a name="config"></a>
The configuration file for this module can be found in <serverDir>/ForgeEssentials/Backup/config.cfg  
The configuration file is well documented.
[Example of default config file after beta #219 or official build #252](http://pastebin.com/raw.php?i=Lv5wSTgr)

# Usage <a name="use"></a>
You can use the command to make manual backups of worlds or folders.
And you can use the AutoBackup & AutoRemove functions, explained in the config, to set up a fully automated backup system. More on that later.

# Commands <a name="command"></a>
<table>
	<tr>
		<th>Command Usage</th>
		<th>Aliases</th>
		<th>Permission Node</th>
		<th>Description</th>
	</tr>
	<tr>
		<td>/backup</td>
		<td></td>
		<td>ForgeEssentials.backup.command</td>
		<td>Makes a backup of all loaded worlds.</td>
	</tr>
        <tr>
		<td>/backup <dimensionID></td>
		<td></td>
		<td>ForgeEssentials.backup.command</td>
		<td>Makes a backup of a specific world.</td>
	</tr>
        <tr>
		<td>/backup <folder></td>
		<td></td>
		<td>ForgeEssentials.backup.command</td>
		<td>Makes a backup a folder relative to the server's jar file.</td>
	</tr>
	<tr>
</table>

# AutoBackup <a name="autobackup"></a>
Some properties explained:

"worldSaving":
If you change this to true you will allow all worlds to save. If this remains false, the worlds will only save at the set intervals.
This will reduce the HDD lag but if your server crashes, you will lose all changes made after the last save.

"whitelist":
If you add any dimensions to this list, it will assume they will need backups. Even though they might not be loaded. Still, if "backupOnWorldUnload" is false, it will not save unloaded worlds!

"blacklist":
If you add any dimensions to this list, it will never automatically make backups of that dimension. Manual backups don't check this list.

"extraFolders":
If you add folders to this list, it will make backups of those folders every time the world is backed up. You can use this to save the config folder or extra data saved by mods.

# AutoRemove <a name="autoremove"></a>
This is explained in the config. Use this to regulate the amount of backups made.
