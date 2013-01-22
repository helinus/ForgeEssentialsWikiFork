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
		<td>afk</td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.afk</td>
		<td>/afk</td>
		<td>Appends the "[AFK]" tag to your username.</td>
	</tr>
	<tr>
		<td>back</td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.back</td>
		<td>/back</td>
		<td>Teleport to your last death point or teleport.</td>
	</tr>
	<tr>
		<td>bed</td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.bed</td>
		<td>/bed</td>
		<td>Teleport to your bed point.</td>
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
		<td>clearinventory</td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.clear</td>
		<td>/clear [player]</td>
		<td>Clears your or the specified player's inventory.</td>
	</tr>
	<tr>
		<td>colorize</td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.colorize</td>
		<td>/colorize</td>
		<td>Parses pre-existing color codes on signs.</td>
	</tr>
	<tr>
		<td>craft</td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.craft</td>
		<td>/clear [player]</td>
		<td>Brings up a crafting table GUI for use on the go.</td>
	</tr>
	<tr>
		<td>enderchest</td>
		<td>echest</td>
		<td>ForgeEssentials<br>.BasicCommands.enderchest</td>
		<td>/enderchest</td>
		<td>Opens your ender chest inventory.</td>
	</tr>
	<tr>
		<td>feperm</td>
		<td>fep, perm, p</td>
		<td>ForgeEssentials.perm</td>
		<td>/p &#60;group|user&#62 ...</td>
		<td>Edits the permissions system. For more information, see <a href=Permissions-Commands>Permissions Reference</a><br><b>**WARNING**</b> This is an all or nothing perm at the moment!</td>
	</tr>
	<tr>
		<td>gamemode</td>
		<td>gm</td>
		<td>ForgeEssentials<br>.BasicCommands.gamemode</td>
		<td>/gamemode [type]</td>
		<td>Changes your gamemode to the specified type (can be number or string).  If type is not specified, game mode is changed from survival/adventure to creative, or creative to survival.</td>
	</tr>
	<tr>
		<td>gamemode</td>
		<td>gm</td>
		<td>ForgeEssentials<br>.BasicCommands.gamemode.others</td>
		<td>/gamemode &#60;player> [type]</td>
		<td>Changes specified player's gamemode to the specified type (can be number or string).  If type is not specified, game mode is changed from survival/adventure to creative, or creative to survival.</td>
	</tr>
	<tr>
		<td>give</td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.give</td>
		<td>/give &#60;player> &#60;id[:meta] [amount]<br>OR<br>
		/give &#60;player> &#60;id> [amount] [meta]</td>
		<td>Gives the specified player the specified amount of the specified item.  Meta and amount are optional.  If not specified, meta defaults to 0, amount defaults to 64.</td>
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
		<td>/home</td>
		<td>Teleports your to your home.</td>
	</tr>
	<tr>
		<td>home</td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.home.set</td>
		<td>/home &#60f;set|x, y, z></td>
		<td>Sets your home to your current location. "/home x y z" sets your home to specific coordinates, where x, y, and z are numbers.</td>
	</tr>
	<tr>
		<td>i</td>
		<td>item</td>
		<td>ForgeEssentials<br>.BasicCommands.i</td>
		<td>/i &#60;id[:meta] [amount]</td>
		<td>Gives you the specified amount of the specified item.  Meta and amount are optional.  If not specified, meta defaults to 0, amount defaults to 64.</td>
	</tr>
        <tr>
		<td>invsee</td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.invsee</td>
		<td>/invsee &#60;player></td>
		<td>Allows you to see the player's inventory.  Top row is their hotbar.</td>
	</tr>
	<tr>
		<td>jump</td>
		<td>j</td>
		<td>ForgeEssentials<br>.BasicCommands.jump</td>
		<td>/jump</td>
		<td>Teleports you to the location you are currently looking.</td>
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
		<td>/kit set &#60;name&#62; [timeout in seconds] => Save your inventory as a kit.<br>
		/kit del &#60;name&#62 => Delete the kit.<br>
		/kit &#60;name&#62 => Get the kit</td>
	</tr>
	<tr>
		<td>modlist</td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.modlist</td>
		<td>/modlist [page]</td>
		<td>Prints a list of mods installed on the server.</td>
	</tr>
	<tr>
		<td>motd</td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.motd</td>
		<td>/motd [new motd]  </td>
		<td>Get the message of the day or set a new MOTD.</td>
	</tr>
	<tr>
		<td>msg</td>
		<td>tell, whisper</td>
		<td>ForgeEssentials<br>.Chat.commands.msg</td>
		<td>/msg &#60;player&#62 <message></td>
		<td>Allows you to send a private message to another player.</td>
	</tr>
	<tr>
		<td>mute</td>
		<td></td>
		<td>ForgeEssentials<br>.Chat.commands.mute</td>
		<td>/mute <player></td>
		<td>Prevents muted player from posting any messages in chat.</td>
	</tr>
	<tr>
		<td>nickname</td>
		<td>nick</td>
		<td>ForgeEssentials<br>.Chat.commands.nick</td>
		<td>/nick <name></td>
		<td>Change your display name.</td>
	</tr>
        <tr>
		<td>ping</td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.ping</td>
		<td>/ping</td>
		<td>"Pings" the server and returns the time taken to communicate with the server in milliseconds. Please note that ping is not guaranteed to be accurate and may produce inaccurate results for a variety of reasons beyond our control. We are not responsible for any inaccuracies of this command.</td>
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
		<td>ForgeEssentials<br>.Chat.commands.r</td>
		<td>/r &#60;message&#62</td>
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
		<td>repair</td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.repair</td>
		<td>/repair</td>
		<td>Restores your currently held item to its undamaged state.</td>
	</tr>
	<tr>
		<td>rules</td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.rules</td>
		<td>/rules [&#60;number&#62 remove|&#60;new rule&#62;]  </td>
		<td>Get the rules of the server. Specify a rule number and either a new rule or "remove" to add or remove a rule, respectively.</td>
	</tr>
        <tr>
		<td>setspawn</td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.setspawn</td>
		<td>/setspawn</td>
		<td>Sets the respawn point. (We're trying to figure out how to make it change the default spawn point while still holding onto the information we need)</td>
	</tr>
	<tr>
		<td>smite</td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.smite</td>
		<td>/smite &#60;me|player&#62;</td>
		<td>Strike the block your are looking at with lightning, or specify "me" or a player's name to strike yourself or another player, respectively.</td>
	</tr>
        <tr>
		<td>spawn</td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.spawn</td>
		<td>/spawn</td>
		<td>Teleports you to the point set by /setspawn.</td>
	</tr>
        <tr>
		<td>spawnmob</td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.setspawn</td>
		<td>/spawnmob &#60;mobname> [amount]</td>
		<td>Spawns the amount of mobname where you are looking.  Amount defaults to 1.</td>
	</tr>
	<tr>
		<td>tp</td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.tp</td>
		<td>/tp &#60;player> &#60;targetPlayer|x y z></td>
		<td>Teleport player to targetPlayer's position or coordinates set by x, y, and z.</td>
	</tr>
	<tr>
		<td>tphere</td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.tphere</td>
		<td>/tphere &#60;player></td>
		<td>Teleport another player to your position</td>
	</tr>
	<tr>
		<td>tppos</td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.tppos</td>
		<td>/tppos &#60;x y z></td>
		<td>Will allow a player to teleport to another</td>
	</tr>
	<tr>
		<td>tps</td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.tps</td>
		<td>/tps [all|#]</td>
		<td>Will display current memory use and average ticks per second of the current world you are in. The bigger the number, the better the server is performing.</td>
	</tr>
	<tr>
		<td>unmute</td>
		<td></td>
		<td>ForgeEssentials<br>.Chat.commands.unmute</td>
		<td>/unmute <player></td>
		<td>Unmutes the specified player.</td>
	</tr>
	<tr>
		<td>virtualchest</td>
		<td>vchest</td>
		<td>ForgeEssentials<br>.BasicCommands.virtualchest</td>
		<td>/vchest /virtualchest</td>
		<td>Opens a virtual chest equal to a double chest.</td>
	</tr>
	<tr>
		<td>warp</td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.warp</td>
		<td>/warp &#60;warpname></td>
		<td>Teleports you to the specified warp point.</td>
	</tr>
	<tr>
		<td>warp set|del</td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.warp.admin</td>
		<td>/warp set|del &#60;warpname></td>
		<td>Creates (set) or deletes (del) specified warp point.  Set will fail if warp name is in use.</td>
	</tr>
	<tr>
		<td></td>
		<td></td>
		<td>ForgeEssentials<br>.BasicCommands.</td>
		<td></td>
		<td></td>
	</tr>
</table>

### Vanilla Overrides
The following commands all have the permission node structure of<br>
**_ForgeEssentials.BasicCommands.&#60;name&#62;_**<br>
and have the same usage as the vanilla commands they override.
+ ban
+ ban-ip
+ banlist
+ debug
+ defaultgamemode
+ deop
+ difficulty
+ enchant
+ gamerule
+ kick
+ me
+ op
+ pardon
+ pardon-ip
+ publish
+ save-all
+ save-off
+ save-on
+ say
+ seed
+ stop
+ time
+ toggledownfall
+ weather
+ whitelist

## WorldControl Commands
<table>
	<tr>
		<th>Command</th>
		<th>Aliases</th>
		<th>Permission Node</th>
		<th>Usage</th>
		<th>Description</th>
	</tr>
	<tr>
		<td>pos1</td>
		<td></td>
		<td>ForgeEssentials.WorldControl<br>.commands.pos1</td>
		<td>//pos1 &lt;x> &lt;y> &lt;z></td>
		<td>Sets the first selection point to given X, Y, and Z coordinates.</td>
	</tr>
	<tr>
		<td>pos2</td>
		<td></td>
		<td>ForgeEssentials.WorldControl<br>.commands.pos2</td>
		<td>//pos2 &lt;x> &lt;y> &lt;z></td>
		<td>Sets the second selection point to given X, Y, and Z coordinates.</td>
	</tr>
	<tr>
		<td>deselect</td>
		<td></td>
		<td>ForgeEssentials.WorldControl<br>.commands.deselect</td>
		<td>//deselect</td>
		<td>Nulls the current selection, because having it hang around when it isn't needed is annoying. Does not affect blocks.</td>
	</tr>
	<tr>
		<td>wand</td>
		<td></td>
		<td>ForgeEssentials.WorldControl<br>.commands.wand</td>
		<td>//wand</td>
		<td>Binds the currently selected item in the player's hotbar to the WorldControl wand. If no item is selected, WC will use fists to select the area.</td>
	</tr>
	<tr>
		<td>undo</td>
		<td></td>
		<td>ForgeEssentials.WorldControl<br>.commands.undo</td>
		<td>//undo</td>
		<td>Undoes the last WorldControl action. The system only saves five steps of undo action.</td>
	</tr>
	<tr>
		<td>redo</td>
		<td></td>
		<td>ForgeEssentials.WorldControl<br>.commands.redo</td>
		<td>//redo</td>
		<td>Redoes an action previously undone using the //undo command. The system only saves five steps of redo action.</td>
	</tr>
	<tr>
		<td>set</td>
		<td></td>
		<td>ForgeEssentials.WorldControl<br>.commands.set</td>
		<td>//set &lt;block ID[:metadata]></td>
		<td>Sets all blocks within the current selection to the ID provided. Optionally, metadata can be provided for blocks that can use it.</td>
	</tr>
	<tr>
		<td>replace</td>
		<td></td>
		<td>ForgeEssentials.WorldControl<br>.commands.replace</td>
		<td>//replace &lt;target block ID[:metadata]> &lt;replacement block ID[:metadata]></td>
		<td>Searches the current selection for blocks of the target ID (optionally metadata; if none is provided, all blocks of the ID will be replaced) with the second block ID and optional Metadata.</td>
	</tr>
	<tr>
		<td>thaw</td>
		<td></td>
		<td>ForgeEssentials.WorldControl<br>.commands.thaw</td>
		<td>//thaw &lt;radius> [&lt;x> &lt;z>]</td>
		<td>Removes snow from exposed blocks, and replaces ice with water blocks within a specified radius. If the X and Z coordinates are not provided, the player's position will be used.</td>
	</tr>
	<tr>
		<td>freeze</td>
		<td></td>
		<td>ForgeEssentials.WorldControl<br>.commands.freeze</td>
		<td>//freeze &lt;radius> [&lt;x> &lt;z>]</td>
		<td>Replaces exposed water with ice blocks within a specified radius. If the X and Z coordinates are not provided, the player's position will be used.</td>
	</tr>
	<tr>
		<td>snow</td>
		<td></td>
		<td>ForgeEssentials.WorldControl<br>.commands.snow</td>
		<td>//snow &lt;radius> [&lt;x> &lt;z>]</td>
		<td>Adds a layer of snow to exposed blocks within a specified radius. If the X and Z coordinates are not provided, the player's position will be used.</td>
	</tr>
	<tr>
		<td>till</td>
		<td></td>
		<td>ForgeEssentials.WorldControl<br>.commands.till</td>
		<td>//till &lt;radius> [&lt;x> &lt;z>]</td>
		<td>Transforms exposed dirt and grass into farmland within a specified radius. If the X and Z coordinates are not provided, the player's position will be used.</td>
	</tr>
	<tr>
		<td>untill</td>
		<td></td>
		<td>ForgeEssentials.WorldControl<br>.commands.untill</td>
		<td>//untill &lt;radius> [&lt;x> &lt;z>]</td>
		<td>Transforms exposed farmland into dirt blocks within a specified radius. If the X and Z coordinates are not provided, the player's position will be used.</td>
	</tr>
</table>

## WorldBorder Commands

### Placeholder

## Admin Commands

### /serverdo &lt;command> [arg1] [arg2] ...
Allows network clients to perform server commands as though they had been typed into the server's console.
NOTE: Until permissions are working, only Ops are able to use this command.