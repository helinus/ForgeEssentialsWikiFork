* [Installation](#install)
* [Configuration](#config)
* [Commands](#command)
* [Other Permissions](#perms)
* [IRC Integration](#irc)
* [OtherInfo](#other)

# Installation <a name="install"></a>
Put this module in the mods folder. If the Core is installed, it will be loaded.

# Configuration <a name="config"></a>
The configuration file for this can be found in ./ForgeEssentials/Chat/config.cfg  
For the chat formatting, codes are provided in the config file. 

### Group chat prefixes and suffixes
The group prefixes and suffixes however are slightly different than standard chat formatting. They require special codes in the format {ladderName<:>zoneName}. Because a player can be in multiple zones, at multiple times, this kind of format is used so that an Admin may retain the prefixes of his Admin group in the GLOBAL zone while still having fun in the server Arena zone as one in the Contender group. Don't forget that if you don't have many groups, you can still use {...<:>...} to display groups from any ladder (first "..."), and any zone (second "...").

### Censoring
The chat configuration file contains a list of banned words. You can add and remove these words from that list to control what will be censored and what will not be censored in the chat windows. Censoring can also be removed entirely by setting the ```censor``` property to false.

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
		<td>ForgeEssentials.Chat.commands.nickname<br/>ForgeEssentials.Chat.commands.nickname.others<br/></td>
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

# Other Permissions <a name="perms"></a>
```ForgeEssentials.chat.usecolor```  Controls if a & format tags will be replaced when the player chats.

# IRC Integration <a name="irc"></a>
The chat module now contains integrated support for IRC courtesy of luacs1998. If you know what IRC is... then this feature is largely self-explanatory. Settings for IRC may be found in the chat config. 

# Other Info <a name="other"></a>
Us ForgeEssentials devs plan on allowing some awesome things in forge. ~~We plan on having IRC integration as well as~~ We plan on an IRC channel system. Not to to mention ranged chat.