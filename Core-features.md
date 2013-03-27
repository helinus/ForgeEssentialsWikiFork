This is where all the features of ForgeEssentials exist that are NOT included in a separate module.

# Permissions
### [Getting Started With Permissions](https://github.com/ForgeEssentials/ForgeEssentialsMain/wiki/Permissions-Commands)

# ModList
A list of all the mods loaded and their versions is included in "./ForgeEssentials/modlist.txt"

# Commands
<table>
	<tr>
		<th>Command Usage</th>
		<th>Permission Node</th>
		<th>Description</th>
	</tr>
	<tr>
		<td>/fecredits</td>
		<td> none</td>
		<td>The Credits for ForgeEssentials</td>
	</tr>
	<tr>
		<td>/feversion</td>
		<td> none</td>
		<td>Shows the current ForgeEssentials version</td>
	</tr>
	<tr>
		<td>/fedebug</td>
		<td> ForgeEssentials.CoreCommands.fedebug</td>
		<td>Displays data about injected Block events</td>
	</tr>
	<tr>
		<td>//fewand</td>
		<td> ForgeEssentials.CoreCommands.select.wand</td>
		<td>Binds the wand</td>
	</tr>
	<tr>
		<td>//fewand</td>
		<td> ForgeEssentials.CoreCommands.select.wand</td>
		<td>Binds the wand</td>
	</tr>
	<tr>
		<td>//fepos1 <br /> //fepos2</td>
		<td> ForgeEssentials.CoreCommands.select.pos</td>
		<td>allows selecting points</td>
	</tr>
	<tr>
		<td>//fedesel</td>
		<td> ForgeEssentials.CoreCommands.select.deselect/td>
		<td> Clears the selection</td>
	</tr>
</table>


# Banning recipes
First off its very easy to use.
The file is located in `./ForgeEssentials/banneditems.cfg`
If you wish to ban the crafting of an item you place the item "id:meta" under "S:List" in the #nocraft section. pretty self explanatory.

Now say you didn't want anyone on your server to be able to craft some items. For this example were going to use a TNT (id=46) and a Chunk Loader(id=243). We will also show you how to ban all variants of an item/block. For that we will use a Mining Laser(id=30208:1 and 30208:27). You have 2 meta's for the mining laser for charged and uncharged so to be safe we ban them both by using "-1" to ban them all in one line.
lets see what this looks like in the cfg.


    ####################
    # nocraft
    #===================
    # Configuration options to make an item uncraftable.
    ####################
    nocraft {
        # Use this format: "id:meta". Use meta -1 to ban ALL variants of an item/block.
        S:List <
            243
            46
            30208:-1
         >