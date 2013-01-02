## Syntax Explanation
Take this command as an example: "/rules [\<number> \<"remove">|\<new rule>]"  
**/rules:** The command itself. Always preceded by / or in some cases, //  
  
**[\<number> remove|\<new rule>]:** This is an optional argument. Anything surrounded by [] is optional. Inside of the optional brackets are the required brackets, \<>. These mean that the argument within the \<> is required if the argument within the [] is used. "remove" has quotation marks, meaning that it is a literal word that can be used as an argument.  
  
Here are some examples of valid commands:  
**/rules:** All the arguments after the command are surrounded by [], meaning they are optional as a whole.  
  
**/rules 2 remove:** The optional argument requires 2 sub-arguments. If that optional argument is used at all, all sub-arguments must be provided.  
  
**/rules 2 No TNT:** This is also valid because one option for the second argument is the enter any new rule that you want. In this case, the new rule can be multiple words. This is not the case with all commands.  
  
Here are some invalid commands:  
**/rules 2:** The argument is provided, so both sub-arguments are necessary, not just one.  
  
**/rules remove 2:** The arguments are backwards. The game will think that you want rule number remove to be 2, not rule 2 to be removed. It will likely tell you about this mistake in a hurtful way.  
## User Commands
<table>
	<tr>
		<th>Command</th>
		<th>Aliases</th>
		<th>Permission Node</th>
		<th>Usage</th>
		<th>Description</th>
	</tr>
	<tr>
		<td>back</td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.back</td>
		<td>/back</td>
		<td>Teleport to your last death point or teleport (/tp command is being worked on).</td>
	</tr>
	<tr>
		<td>backup</td>
		<td></td>
		<td>ForgeEssentials.backup</td>
		<td>/backup</td>
		<td>Runs a backup of your world data folder.</td>
	</tr>
	<tr>
		<td>burn</td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.burn</td>
		<td>/burn [me|player]</td>
		<td>Sets you or someone else on fire.</td>
	</tr>
	<tr>
		<td>butcher</td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.butcher</td>
		<td>/butcher [radius|world] [type] [x, y, z]</td>
		<td>Kill all hostile mobs within a certain radius, or 10 blocks by default.  Putting "world" instead of a numerical radius specifies the entire dimension.  The 6 types you can choose from are: passive (all non-hostile mobs except tamed animals), hostile (doesn't cover bosses), golem, villager, tamed, and all (everything but bosses and players).  <b>BE CAREFUL!  This cannot be undone!</td>
	</tr>
	<tr>
		<td>capabilities</td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.capabilities</td>
		<td>/capabilities [player] [capability] [value|default]</td>
		<td>Allows you to modify a bunch of interesting stuff related to the player.</td>
	</tr>
	<tr>
		<td>enderchest</td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.enderchest</td>
		<td>/enderchest</td>
		<td>Opens your ender chest inventory.</td>
	</tr>
	<tr>
		<td>heal</td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.heal</td>
		<td>/heal [player]</td>
		<td>Restores the target's health, hunger and extinguishes them.</td>
	</tr>
	<tr>
		<td>home</td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.home</td>
		<td>/home [here|x, y, z] </td>
		<td>Teleports your to your home. "/home here" sets your home to your current location. "/home x y z" sets your home to specific coordinates, where x, y, and z are numbers.</td>
	</tr>
	<tr>
		<td>kill</td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.kill</td>
		<td>/kill [player]</td>
		<td>Kill yourself or the specified player.</td>
	</tr>
	<tr>
		<td>kit</td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.kit</td>
		<td>/kit [set|del][kitname]</td>
		<td>/kit set <name> [timeout in seconds] => Save your inventory as a kit.<br>
		/kit del <name> => Delete the kit.<br>
		/kit <name> => Get the kit</td>
	</tr>
	<tr>
		<td>motd</td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.motd</td>
		<td>/motd [new motd]  </td>
		<td>Get the message of the day or set a new MOTD.</td>
	</tr>
	<tr>
		<td>modlist</td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.modlist</td>
		<td>/modlist [page]</td>
		<td>Prints a list of mods installed on the server.</td>
	</tr>
	<tr>
		<td>msg</td>
		<td>tell, whisper</td>
		<td>ForgeEssentials<br>.BasicCommands.msg</td>
		<td>/msg <player> <message></td>
		<td>Allows you to send a private message to another player.</td>
	</tr>
	<tr>
		<td>potion</td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.potion</td>
		<td>/potion [player] [effect] [duration in seconds]</td>
		<td>Applies the specified effect to the specified player, for the specified duration.  "me" makes the potion work on you.</td>
	</tr>
	<tr>
		<td>r</td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.r</td>
		<td>/r <message></td>
		<td>Replies directly to the last person you interacted with in the private message system.</td>
	</tr>
	<tr>
		<td>remove</td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.remove</td>
		<td>/remove [radius] [x, y, z]</td>
		<td>Remove all item entities within specified radius or specified point, or 15 blocks by default.</td>
	</tr>
	<tr>
		<td>rules</td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.rules</td>
		<td>/rules [\<number> remove|\<new rule>]  </td>
		<td>Get the rules of the server. Specify a rule number and either a new rule or "remove" to add or remove a rule, respectively.</td>
	</tr>
	<tr>
		<td>smite</td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.smite</td>
		<td>/smite [me|\<player>]</td>
		<td>Strike the block your are looking at with lightning, or specify "me" or a player's name to strike yourself or another player, respectively.</td>
	</tr>
	<tr>
		<td></td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.</td>
		<td></td>
		<td></td>
	</tr>
	<tr>
		<td></td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.</td>
		<td></td>
		<td></td>
	</tr>
	<tr>
		<td></td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.</td>
		<td></td>
		<td></td>
	</tr>
	<tr>
		<td></td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.</td>
		<td></td>
		<td></td>
	</tr>
	<tr>
		<td></td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.</td>
		<td></td>
		<td></td>
	</tr>
	<tr>
		<td></td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.</td>
		<td></td>
		<td></td>
	</tr>
	<tr>
		<td></td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.</td>
		<td></td>
		<td></td>
	</tr>
	<tr>
		<td></td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.</td>
		<td></td>
		<td></td>
	</tr>
	<tr>
		<td></td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.</td>
		<td></td>
		<td></td>
	</tr>
	<tr>
		<td></td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.</td>
		<td></td>
		<td></td>
	</tr>
	<tr>
		<td></td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.</td>
		<td></td>
		<td></td>
	</tr>
	<tr>
		<td></td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.</td>
		<td></td>
		<td></td>
	</tr>
	<tr>
		<td></td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.</td>
		<td></td>
		<td></td>
	</tr>
	<tr>
		<td></td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.</td>
		<td></td>
		<td></td>
	</tr>
	<tr>
		<td></td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.</td>
		<td></td>
		<td></td>
	</tr>
	<tr>
		<td></td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.</td>
		<td></td>
		<td></td>
	</tr>
	<tr>
		<td></td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.</td>
		<td></td>
		<td></td>
	</tr>
	<tr>
		<td></td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.</td>
		<td></td>
		<td></td>
	</tr>
</table>

## WorldControl Commands

### //pos1 &lt;x> &lt;y> &lt;z>
Sets the first selection point to given X, Y, and Z coordinates.

### //pos2 &lt;x> &lt;y> &lt;z>
Sets the second selection point to given X, Y, and Z coordinates.

### //deselect
Removes the current selection, because having it hang around when it isn't needed is annoying. Does not affect blocks.

### //wand
Binds the currently selected item in the player's hotbar to the WorldControl wand. If no item is selected, WC will use fists to select the area.

### //undo
Undoes the last WorldControl action. The system only saves five steps of undo action.

### //redo
Redoes an action previously undone using the //undo command. The system only saves five steps of redo action.

### //set &lt;block ID[:metadata]>
Sets all blocks within the current selection to the ID provided. Optionally, metadata can be provided for blocks that can use it.

### //replace &lt;target block ID[:metadata]> &lt;replace with block ID[:metadata]>
Searches the current selection for blocks of the target ID (optionally metadata; if none is provided, all blocks of the ID will be replaced) with the second block ID and optional Metadata.

### //thaw &lt;radius> [&lt;x> &lt;z>]
Removes snow from exposed blocks, and replaces ice with water blocks within a specified radius. If the X and Z coordinates are not provided, the player's position will be used.

### //freeze &lt;radius> [&lt;x> &lt;z>]
Replaces exposed water with ice blocks within a specified radius. If the X and Z coordinates are not provided, the player's position will be used.

### //snow &lt;radius> [&lt;x> &lt;z>]
Adds a layer of snow to exposed blocks within a specified radius. If the X and Z coordinates are not provided, the player's position will be used.

### //till &lt;radius> [&lt;x> &lt;z>]
Transforms exposed dirt and grass into farmland within a specified radius. If the X and Z coordinates are not provided, the player's position will be used.

### //untill &lt;radius> [&lt;x> &lt;z>]
Transforms exposed farmland into dirt blocks within a specified radius. If the X and Z coordinates are not provided, the player's position will be used.

## Admin Commands

### /serverdo &lt;command> [arg1] [arg2] ...
Allows network clients to perform server commands as though they had been typed into the server's console.
NOTE: Until permissions are working, only Ops are able to use this command.