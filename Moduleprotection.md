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


# Other Info <a name="other"></a>
As new hooks are added to forge, such as MobGrefing events and CreeperExplosions, new permissions will be added to stop them.