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
		<td>/zone &lt;define|create> &lt;name> </td>
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
		<td>Sets the zone's entry message to the specified</td>
	</tr>
	<tr>
		<td>/zone &lt;exit> &lt;name> [... message ...]</td>
		<td>Sets the zone's exit message to the specified</td>
	</tr>
</table>
## Permissions Commands
### Remember that the base command is `/feperm` and that `/p` is an alias