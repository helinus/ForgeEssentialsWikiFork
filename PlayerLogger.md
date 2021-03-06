* [Installation](#install)
* [Configuration](#config)
* [Usage](#use)
* [Commands](#command)
* [Other Info](#other)

# Installation <a name="install"></a>
Put this module in the mods folder. If the Core is installed, it will be loaded.<br>
**Requires the WorldControl module to be able to use rollback**

# Configuration <a name="config"></a>
You have to have a MySQL database for PlayerLogger to put it's data in.

# Usage <a name="use"></a>
### Rollback usage
All actions must be confirmed with '/rb ok'.  
All actions can be canceld with '/rb abort'.  
`/rb clear <username>` => Removes a players data.  
`/rb undo <username>` => Undo a rollback. You can specify time and radius.  
`/rb <undo|rollback> <username>` => Rolls back a players changes. All the way!  
`/rb <undo|rollback> <username> <rad>` => Format like this: 10r");  
`/rb <undo|rollback> <username> <time>` => Format time like this: 10d = 10 days, 10h = 10 hours.  
A combo of the above is possible too.

# Commands <a name="command"></a>
<table>
	<tr>
		<th>Command Usage</th>
		<th>Aliases</th>
		<th>Permission Node</th>
		<th>Description</th>
	</tr>
	<tr>
		<td>/playerlogger &lt;enable|disable> [limit]</td>
		<td>/pl</td>
		<td>ForgeEssentials.playerLogger.playerlogger</td>
		<td>This enables you to click a block to get the last 5 changes, or more if you define a limit</td>
	</tr>
	<tr>
		<td>/rollback</td>
		<td>/rb</td>
		<td>ForgeEssentials.playerLogger.rollback</td>
		<td>Do something</td>
	</tr>
	<tr>
</table>


# Other Info <a name="other"></a>
