* [Installation](#install)
* [Configuration](#config)
* [Penalties] (#Penalties)
* [Commands](#command)
* [Other Info](#other)

# Installation <a name="install"></a>
Put this module in the mods folder. If the Core is installed, it will be loaded.

# Configuration <a name="config"></a>
The configuration file for this can be found in ./ForgeEssentials/WorldBorder/config.cfg  

# Penalties <a name="penalties"></a>
Possible penalties
<table>
<tr><th>penalty name</th><th>effect</th><th>effect options</th></tr>
<tr><td>damage</th><td>hurts the player by the given value</td><td>Amount of damage in 1/2 hearts.</td></tr>
<tr><td>executecommand</td><td>executes a given server command</td><td>%p gets replaced with the players username</td></tr>
<tr><td>knockback</td><td>Teleports the player back to the start of the border</td><td>This effect has no options.</td></tr>
<tr><td>message</td><td> Message to send to the player. You can use color codes.</td><td>Message to send to the player. You can use color codes.</td></tr>
<tr><td>potion</td><td>Applies a given potion (multiple possible) on a player</td><td>Format like this: 'ID:duration:amplifier</td></tr>
<tr><td>serverkick</td><td>Kicks the player</td><td>Message to send to the player on the kick screen.</td></tr>
<tr><td>smite</td><td>Player is struck by lightning</td><td>This effect has no option.</td></tr>
</table>




# Commands <a name="command"></a>
## Setting the border.
The command name is "worldborder", or use "wb" as alias.
Permission node is "ForgeEssentials.WorldBorder.admin". Defaults to owners.
<table>
	<tr>
		<th>Command</th>
		<th>Description</th>
	</tr>
	<tr>
		<td>/wb <global|world|dimID> [info]</td>
		<td>Gets info about the (global / world) border.</td>
	</tr>
	<tr>
		<td>/wb &lt;global|world|dimID> &lt;enable|disable></td>
		<td>Enable or disable the border.</td>
	</tr>
	<tr>
		<td>/wb &lt;global|world|dimID> &lt;center|radius|shape></td>
		<td>Set the center (&lt;x y z>), radius (&lt;size>) or shape (&lt;square|round>) of the border.</td>
	</tr>
</table>
## Filling the border.
<table>
	<tr>
		<th>Command</th>
		<th>Description</th>
	</tr>
	<tr>
		<td>/filler</td>
		<td>Gets info on all running fillers.</td>
	</tr>
	<tr>
		<td>/filler &lt;world|dimID></td>
		<td>Gets info on the filler for that world.</td>
	</tr>
</table>

# Other Info <a name="other"></a>
Written by Dries007, so you will most likely find some bugs. ;-)