* [Installation](#install)
* [Configuration](#config)
* [Usage](#use)
* [Commands](#command)
* [Other Info](#other)

# Installation <a name="install"></a>
Put this module in the mods folder. If the Core is installed, it will be loaded.

# Configuration <a name="config"></a>
The configuration file for this Module can be found in .ForgeEssentials/WorldControl.config.cfg

# Usage <a name="use"></a>
Use the wand command to make a selection, and then make edits to the selection with the other commands.

# Commands <a name="command"></a>
<table>
	<tr>
		<th>Command Usage</th>
		<th>Aliases</th>
		<th>Permission Node</th>
		<th>Description</th>
	</tr>
	<tr>
		<td>//fewand</td>
		<td></td>
		<td>ForgeEssentials.WorldControl.commands.fewand</td>
		<td>Allows a player to bind the wand</td>
	</tr>
	<tr>
		<td>//pos1<br/>//pos2</td>
		<td></td>
		<td>ForgeEssentials.WorldControl.commands.pos</td>
		<td>Allows a player to select points by looking or coords</td>
	</tr>
	<tr>
		<td>//deselect</td>
		<td>//sel</td>
		<td>ForgeEssentials.WorldControl.commands.deselect</td>
		<td>Allows a player to deselect the current selection</td>
	</tr>
	<tr>
		<td>//set [id|id:meta|name]</td>
		<td></td>
		<td>ForgeEssentials.WorldControl.commands.set</td>
		<td>Allows a player to set their selection to a given block</td>
	</tr>
	<tr>
		<td>//replace [1st] [with]</td>
		<td></td>
		<td>ForgeEssentials.WorldControl.commands.set</td>
		<td>Replaces all instances of the 1st block in the selection with the second</td>
	</tr>
	<tr>
		<td>//undo</td>
		<td></td>
		<td>ForgeEssentials.WorldControl.commands.undo</td>
		<td>Undoes the last WorldControl action</td>
	</tr>
	<tr>
		<td>//redo</td>
		<td></td>
		<td>ForgeEssentials.WorldControl.commands.redo</td>
		<td>Redoes the last undone action</td>
	</tr>
</table>

# Other Info <a name="other"></a>
This module will be expanded to work with all the WorldEdit commands.