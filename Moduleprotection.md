* [Installation](#install)
* [Configuration](#config)
* [Usage](#use)
* [Permissions](#perm)
* [Other Info](#other)

# Installation <a name="install"></a>
Put this module in the mods folder. If the Core is installed, it will be loaded.

# Configuration <a name="config"></a>
`B:enable=true`
If this configuration is set to false, None of the permissions created by this module will be checked.

`B:enableMobCheck=false`
If this configuration is set to true, the permissions controlling mobspawning will take effect. Sometimes the mob-spawn permissionbs cause extensive ammounts of lag. You have been warned.

# Usage <a name="use"></a>
The protection module is similar to the ModifyWorld plugin for PEx. it simply adds permissions relating to protection of the world.

# Permissions <a name="perm"></a>
<table>
	<tr>
		<th>Node</th>
		<th>Description</th>
	</tr>
	<tr>
		<td>ForgeEssentials.Protection.overrideProtection</td>
		<td>If allowed, overrides every other Protection permission</td>
	</tr>
	<tr>
		<td>ForgeEssentials.Protection.allowEdits</td>
		<td>Allows the breaking and placing of blocks.</td>
	</tr>
	<tr>
		<td>ForgeEssentials.Protection.allowBlockInteractions</td>
		<td>Allows the usage of blocks such as levers, buttons, and doors</td>
	</tr>
	<tr>
		<td>ForgeEssentials.Protection.allowEntityInteractions</td>
		<td>Allows interacting with mobs in any way.<br /> hitting mobs, getting hit by mobs, milking cows, and shearing sheap <br /> are all controlled by this permission</td>
	</tr>	<tr>
		<td>ForgeEssentials.Protection.pvp</td>
		<td>Allows Player vs Player damage</td>
	</tr>
	<tr>
		<td>ForgeEssentials.Protection.itemUse</td>
		<td>Allows using specific items in the world. See below</td>
	</tr>
	<tr>
		<td>ForgeEssentials.Protection.mobSpawn.natural</td>
		<td>Allows the natural spawning of mobs in the world. See below</td>
	</tr>
	<tr>
		<td>ForgeEssentials.Protection.mobSpawn.forced</td>
		<td>Allows the forced spawning of mobs in the world. See below</td>
	</tr>
</table>

### ItemUse permission
ForgeEssentials uses an sophisticated algorithm to search for all existing items in Minecraft as of the start of the server. It compiles a list of all of these items, and converts them into permissions. The names are created in the following format: `[source].[block|item].[name|id]`

example for vanilla dirt: `vanilla.block.dirt`

example for BuildCraft DiamondGears : `BuildCraft|Core.item.diamondGearItem`

Sometimes, the algorithm somehow finds multiple items of the same name, thus numbers are appended to the names in order to keep them unique.

`vanilla.item.record`

`vanilla.item.record1`

`vanilla.item.record2`

`vanilla.item.record3`

Sometimes, multiples items are scrunched into a single ItemID like in the case of IronChests.
`IronChest.block.IronChest` Only one name is generated for all the possible types of IronChests there are. 

In order to get arround this, the permissions checked for items when they are used is the following.

if the item is registerred: `ForgeEssentials.protection.itemUse.[source].[block|item].[name].[#damage|#meta]`

if the item somehow evaded registration: `ForgeEssentials.protection.itemUse.unknownSource.unknownType.[#id].[#damage|#meta]`

if you wish to Allow/Deny all an entire ID. Use the name format. if you wish to deny an ID with a specific damage value, simple add the damage value to the end of the permission as the above format.

`IronChest.block.IronChest.0` affects the Iron chest

`IronChest.block.IronChest.1` affects the Gold chest

`IronChest.block.IronChest.6` affects the Obsidian chest

For your convenience, a list of all the generated names and their equivalent itemIDs can be found in `./ForgeEssentials/UnfreindlyItemList.txt`. This file will help you regarding what IDs are mapped to which names and vice versa. It does not however, help you at all when it comes to damage values and meta. For this, it is better to use something like NEI to ascertain the damage values of items.

# Other Info <a name="other"></a>
As new hooks are added to forge, such as endermen griefing events and creeper explosions, new permissions will be added to stop them.