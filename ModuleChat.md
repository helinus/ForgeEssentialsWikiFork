* [Installation](#install)
* [Configuration](#config)
* [Usage](#use)
* [Commands](#command)
* [OtherInfo](#other)

# Installation <a name="install"></a>
Put this module in the mods folder. If the Core is installed, it will be loaded.

# Configuration <a name="config"></a>
The configuration file for this can be found in ./ForgeEssentials/Chat/config.cfg  
For the chat formatting, codes are provided in the config file. The group prefixes and suffixes however are slightly different than standard chat formatting. they require special codes in the format {ladderName<:>zoneName}. Because a player can be in multiple zones, at multiple times, this kind of format is used so that an Admin may retain the prefixes of his Admin group in the GLOBAL zone while still having fun in the server Arena zone as one in the Contender group. Don't forget that if you don't have many groups, you can still use {...<:>...} to display groups from any ladder, and any zone.

# Usage <a name="use"></a>
Use the configs to format chat, and use the commands to do awesome chat related actions.

# Commands <a name="command"></a>
<table>
	<tr>
		<th>Command Usage</th>
		<th>Aliases</th>
		<th>Permission Node</th>
		<th>Description</th>
	</tr>
	<tr>
		<td>/msg [player|server] [message]</td>
		<td>/tell<br/>/whisper</td>
		<td>ForgeEssentials.Chat.commands.msg</td>
		<td>Sends a message directly to a player.<br/>Sends a private message.</td>
	</tr>
	<tr>
		<td>/r</td>
		<td></td>
		<td>ForgeEssentials.Chat.commands.r</td>
		<td>Replies to a PM (/msg)</td>
	</tr>
	<tr>
		<td>/nickname [nick|del]<br/>/nickname [username] [nick|del]</td>
		<td>/nick</td>
		<td>ForgeEssentials.Chat.commands.nick.self<br/>ForgeEssentials.Chat.commands.nick.others<br/></td>
		<td>changes the players nickname</td>
	</tr>
	<tr>
		<td>/mute [player]</td>
		<td></td>
		<td>ForgeEssentials.Chat.commands.mute</td>
		<td>mutes a player</td>
	</tr>
	<tr>
		<td>/unmute [player]</td>
		<td></td>
		<td>ForgeEssentials.Chat.commands.unmute</td>
		<td>unmutes a player</td>
	</tr>
</table>


# Other Info <a name="other"></a>
Us ForgeEssentials devs plan on allowing some awesome things in forge. We plan on having IRC integration as well as a channel system. Not to to mention ranged chat.