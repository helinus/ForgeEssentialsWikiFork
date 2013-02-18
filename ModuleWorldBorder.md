* [Installation](#install)
* [Configuration](#config)
* [Penalties] (#Penalties)
* [Commands](#command)
* [Other Permissions](#perms)
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
<table>
	<tr>
		<th>Command</th>
		<th>Aliases</th>
		<th>Permission Node</th>
		<th>Usage</th>
		<th>Description</th>
	</tr>
	<tr>
		<td>fill</td>
		<td></td>
		<td>?</td>
		<td>/wb fill ok <dimension></td>
		<td>Pre-generates chunks up to world border. This will cause lag.</td>
	</tr>
	<tr>
		<td>turbo</td>
		<td></td>
		<td>?</td>
		<td>/wb turbo <dimension> [off]</td>
		<td>Enables 10 chunks per tick. This will cause severe lag.</td>
	</tr>
	<tr>
		<td>autopilot</td>
		<td></td>
		<td>?</td>
		<td>?</td>
		<td>?</td>
	</tr>
	<tr>
		<td>set</td>
		<td></td>
		<td>?</td>
		<td>/wb set <round|square> <Radius> <X> <Z></td>
		<td>Used to set a world border.</td>
	</tr>
</table>


# Other Permissions <a name="perms"></a>
# Other Info <a name="other"></a>