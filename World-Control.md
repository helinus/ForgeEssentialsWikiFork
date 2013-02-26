* [Installation](#install)
* [Configuration](#config)
* [Usage](#use)
* [Commands](#command)
* [ID Syntax](#idsyntax)
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
		<td>//wand [rebind|unbind|ITEM]</td>
		<td></td>
		<td>ForgeEssentials.WorldControl.selection</td>
		<td>Allows a player to bind the wand</td>
	</tr>
	<tr>
		<td>//pos1 [x y z]<br/>//pos2 [x y z]</td>
		<td>//p1<br/>//p2</td>
		<td>ForgeEssentials.WorldControl.selection</td>
		<td>Allows a player to select points by looking or coords</td>
	</tr>
	<tr>
		<td>//deselect</td>
		<td>//desel<br/>//sel</td>
		<td>ForgeEssentials.WorldControl.selection</td>
		<td>Allows a player to deselect the current selection</td>
	</tr>
	<tr>
		<td>//set [id]</td>
		<td></td>
		<td>ForgeEssentials.WorldControl.blockmanipulation</td>
		<td>Allows a player to set their selection to a given block</td>
	</tr>
	<tr>
		<td>//replace [1st] [with]</td>
		<td></td>
		<td>ForgeEssentials.WorldControl.blockmanipulation</td>
		<td>Replaces all instances of the 1st block in the selection with the second</td>
	</tr>
	<tr>
		<td>//undo</td>
		<td></td>
		<td>ForgeEssentials.WorldControl.backup</td>
		<td>Undoes the last WorldControl action</td>
	</tr>
	<tr>
		<td>//redo</td>
		<td></td>
		<td>ForgeEssentials.WorldControl.backup</td>
		<td>Redoes the last undone action</td>
	</tr>
	<tr>
		<td>//thaw</td>
		<td></td>
		<td>ForgeEssentials.WorldControl.commands.thaw</td>
		<td>thaws the selection area. Melts all ice and snow.</td>
	</tr>
	<tr>
		<td>//freeze</td>
		<td></td>
		<td>ForgeEssentials.WorldControl.commands.freeze</td>
		<td>Turns all the water in the selection into ice</td>
	</tr>
	<tr>
		<td>//snow</td>
		<td></td>
		<td>ForgeEssentials.WorldControl.commands.snow</td>
		<td>Puts a layer of snow over the selection</td>
	</tr>
	<tr>
		<td>//till</td>
		<td></td>
		<td>ForgeEssentials.WorldControl.commands.till</td>
		<td>Turns all dirt in the selection into farmland</td>
	</tr>
	<tr>
		<td>//untill</td>
		<td></td>
		<td>ForgeEssentials.WorldControl.commands.untill</td>
		<td>Turns all farmland in the selection to dirt</td>
	</tr>
	<tr>
		<td>//chunk</td>
		<td></td>
		<td>ForgeEssentials.WorldControl.selection</td>
		<td>Selects the chunk the players is in</td>
	</tr>
	<tr>
		<td>//contract [amount] [reverse] [direction(NSEWUD)]</td>
		<td></td>
		<td>ForgeEssentials.WorldControl.selection</td>
		<td>Contracts the selection with the choosen amount in the choosen direction</td>
	</tr>
	<tr>
		<td>//copy [name(default)] [filler]</td>
		<td></td>
		<td>ForgeEssentials.WorldControl.clipboard</td>
		<td>Copies selection to clipboard</td>
	</tr>
</table>

# ID Syntax <a name="idsyntax"></a>
<table>
<tr>
<th>Name</th>
<th>Syntax</th>
<th>Description</th>
</tr>
<tr>
<td>ID</td>
<td>ID</td>
<td>Block ID, if invalid or 0, results in air</td>
</tr>
<tr>
<td>ID & Meta</td>
<td>ID:Meta</td>
<td>same as ID, just metadata is added</td>
</tr>
<tr>
<td>Name</td>
<td>oakwoodplanks</td>
<td>The name of any block, no spaces, case is irrelevant, no periods.</td>
</tr>
<tr>
<td>Name & Meta</td>
<td>oakwoodplanks:2</td>
<td>Same as name, if a block name has a metadata it work work, for instance, sprucewood:1 does not work, but oakwood:1 does.</td>
</tr>
<tr>
<td>ID & Meta Range</td>
<td>35:0-15</td>
<td>Same as ID:Meta, except it ranges the meta, Ex: wool:0-15 returns all types of wool</td>
</tr>
<tr>
<td>Name & Meta Range</td>
<td>wool:0-15</td>
<td>Same as above, but uses a name instead, must be an ID based name.</td>
</tr>
<tr>
<td>ID Range</td>
<td>35_40</td>
<td>ID range, does not work with names, may eventually be deprecated.</td>
</tr>
</table>

Special Features: <br>
Long Range placing & breaking(just like normal)

# Other Info <a name="other"></a>
This module will be expanded to work with all the WorldEdit commands.