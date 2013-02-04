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
<tr><th>penalty name</th><th>effect</th><th>option</th></tr>
<tr><td>damage</th><td></td><td></td></tr>
<tr><td>executecommand</td><td></td><td></td></tr>
<tr><td>knockback</td><td></td><td></td></tr>
<tr><td>message</td><td> Message to send to the player. You can use color codes.</td><td></td></tr>
<tr><td>potion</td><td></td><td></td></tr>
<tr><td>serverkick</td><td></td><td>Message to send to the player on the kick screen.</td></tr>
<tr><td>smite</td><td></td><td>This effect has no option.</td></tr>
<table>




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