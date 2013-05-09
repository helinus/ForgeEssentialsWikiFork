###This page is a quick reference for all the permissions commands

## Zone Commands
### `/zn` is an alias for `/zone`
<table>
	<tr>
		<th>Command Usage</th>
		<th>Description</th>
	</tr>
	<tr>
		<td>/zone list [#page]</td>
		<td>Lists all the zones</td>
	</tr>
	<tr>
		<td>/zone info &lt;zone|here></td>
		<td>Displays information about the zone such as parent, priority, and location</td>
	</tr>
	<tr>
		<td>/zone &lt;define> &lt;name> </td>
		<td>Creates a a zone with the given name</td>
	</tr>
	<tr>
		<td>/zone &lt;redefine> &lt;name> </td>
		<td>Changes an existing zone to the new selection</td>
	</tr>
	<tr>
		<td>/zone &lt;remove|delete> &lt;name> </td>
		<td>Removes the specified zone</td>
	</tr>
	<tr>
		<td>/zone &lt;setparent> &lt;name> &lt;name></td>
		<td>Sets the parent of the first zone to the second zone.</td>
	</tr>
	<tr>
		<td>/zone &lt;entry> &lt;name> [... message ...]</td>
		<td>Sets the zone's entry message to the specified.<br>
keyword "remove" as the message will erase any existing message</td>
	</tr>
	<tr>
		<td>/zone &lt;exit> &lt;name> [... message ...]</td>
		<td>Sets the zone's exit message to the specified.<br>
keyword "remove" as the message will erase any existing message</td>
	</tr>
</table>
## Permissions Commands
### Remember that the base command is `/feperm` and that `/p` is an alias
<table>
	<tr>
		<th>Command Usage</th>
		<th>Description</th>
	</tr>
	<tr>
		<td>/feperm export [folder]</td>
		<td>Exports the permissions to the specified folder. Default is folder 'export'</td>
	</tr>
	<tr>
		<th>feperm user commands</th>
		<th>Description</th>
	</tr>
	<tr>
		<td>/feperm user &lt;player|_ME_> supers get &lt;permission></td>
		<td>Displays the status of the permission, if its allowed or denied</td>
	</tr>
	<tr>
		<td>/feperm user &lt;player|_ME_> supers &lt;allow|true> &lt;permission></td>
		<td>Allows a permission for the player in the SUPERS context</td>
	</tr>
	<tr>
		<td>/feperm user &lt;player|_ME_> supers &lt;deny|false> &lt;permission></td>
		<td>Denies a permission for the player in the SUPERS context</td>
	</tr>
	<tr>
		<td>/feperm user &lt;player|_ME_> supers &lt;clear|remove> &lt;permission></td>
		<td>clears a permission for the player in the SUPERS context</td>
	</tr>
	<tr>
		<td>/feperm user &lt;player|_ME_> group set &lt;group></td>
		<td>Removes the player from all other groups, and then adds them to the specified group </td>
	</tr>
	<tr>
		<td>/feperm user &lt;player|_ME_> group add &lt;group></td>
		<td>Adds the player to the specified group </td>
	</tr>
	<tr>
		<td>/feperm user &lt;player|_ME_> group remove &lt;group></td>
		<td>Removes the player from the specified group </td>
	</tr>
	<tr>
		<td>/feperm user &lt;player|_ME_> prefix set &lt;prefix></td>
		<td>Sets the players prefix</td>
	</tr>
	<tr>
		<td>/feperm user &lt;player|_ME_> suffix set &lt;suffix></td>
		<td>Sets the players suffix</td>
	</tr>
	<tr>
		<td>/feperm user &lt;player|_ME_> get &lt;permission> [zone]</td>
		<td>Displays the status of the permission, if its allowed or denied</td>
	</tr>
	<tr>
		<td>/feperm user &lt;player|_ME_> &lt;allow|true> &lt;permission> [zone]</td>
		<td>Allows a permission for the player in the specified zone or the _GLOBAL_ zone</td>
	</tr>
	<tr>
		<td>/feperm user &lt;player|_ME_> &lt;deny|false> &lt;permission> [zone]</td>
		<td>Denies a permission for the player in the specified zone or the _GLOBAL_ zone</td>
	</tr>
	<tr>
		<td>/feperm user &lt;player|_ME_> &lt;clear|remove> &lt;permission> [zone]</td>
		<td>clears a permission for the player in the specified zone or the _GLOBAL_ zone</td>
	</tr>
	<tr>
		<th>feperm group commands</th>
		<th>Description</th>
	</tr>
	<tr>
		<td>/feperm group &lt;group> prefix set &lt;prefix></td>
		<td>Sets the players prefix</td>
	</tr>
	<tr>
		<td>/feperm group &lt;group> suffix set &lt;suffix></td>
		<td>Sets the players suffix</td>
	</tr>
	<tr>
		<td>/feperm group &lt;group> get &lt;permission></td>
		<td>Displays the status of the permission, if its allowed or denied</td>
	</tr>
	<tr>
		<td>/feperm group &lt;group> &lt;allow|true> &lt;permission> [zone]</td>
		<td>Allows a permission for the group in the specified zone or the _GLOBAL_ zone</td>
	</tr>
	<tr>
		<td>/feperm group &lt;group> &lt;deny|false> &lt;permission> [zone]</td>
		<td>Denies a permission for the group in the specified zone or the _GLOBAL_ zone</td>
	</tr>
	<tr>
		<td>/feperm group &lt;group> &lt;clear|remove> &lt;permission> [zone]</td>
		<td>clears a permission for the group in the specified zone or the _GLOBAL_ zone</td>
	</tr>
</table>