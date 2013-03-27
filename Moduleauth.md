* [Introduction](#intro)
* [Configuration](#config)
* [Commands](#command)
* [Other Info](#other)

# Introduction <a name="inro"></a>
The AuthModule is a module to provide security measures to a ForgeEssentials server. This module can force players to register on the server, login, and be unable to do ANYTHING until they do so. This module was designed with the fact that the Minecraft Authorization Services go offline quite often, and thus we have included a feature where the module can detect such a disturbance, and automatically switch the server to offline mode until the servers come back on.

# Configuration <a name="config"></a>
The configuration file can be found in ./ForgeEssentials/AuthLogin/config.cfg

When this Module is **enabled**...
* Anyone logging into the server that has not registered will be forced to register.
* Anyone logging into the server that has registered will be forced to login.
* Anyone who has not registered or not logged in will be unable to do the following...
* --- break/place blocks
* --- send chat messages
* --- use commands other than /register and /login
* --- hit mobs or other players
* --- be hurt by anything
* --- move
* --- interact with mobs or blocks
* --- use items

`B:allowOfflineReg=false`
This configuration is geared towards server owners that usually keep their servers "Online". That means that the servers check to ensure that the players logging in have paid, and are using their Minecraft accounts. Setting this property to `true` will allow players to register their usernames even if the server is offline. The default `false` of the property makes it so that players can only register their usernames while the server is using the Minecraft Authorization Services.

`B:autoEnable=true`
If this is set to `true`, then the AuthModule will check the Minecraft Authorization Service. When the authorization service goes down, the module will turn itself on and set the server to the "Offline" state. When the Authorization Services come back on, the Module will turn itself off and return the server to the "Online" state. If this property is set to `false`, the AuthModule will never check the status of the Minecraft Authorization Services, and never **enable** or **disable** itself automatically.

`B:forceEnable=false`
If this property is set to `true`, then this module will be **enabled** at all times regardless of the server's "Online" or "Offline" status. If this property is set to `false`, the Module will only be enabled if/when the server is in "Offline" mode.

`S:salt=#############`
This property property will automatically be set with an auto-generated salt to be used when encryption passwords. Setting this property and reloading the server will change the salt. Once the salt has been generated, it will never be auto-generated again unless this entire property line is deleted.

`java >> password = sha1(rawpassword + salt);`

` PHP >> $password = sha1($rawPassword.$salt);`

The sha1 encryption algorithm is designed to work flawlessly to imitate PHP.

# Commands <a name="command"></a>
<table>
	<tr>
		<th>Command Usage</th>
		<th>Permission Node</th>
		<th>Description</th>
	</tr>
	<tr>
		<td>/auth help</td>
		<td> none</td>
		<td>Shows the player help for the <br /> /auth command</td>
	</tr>
	<tr>
		<td>/auth register [password]</td>
		<td>none</td>
		<td>Registers the player with the <br /> supplied password</td>
	</tr>
	<tr>
		<td>/auth login [password]</td>
		<td>none</td>
		<td>Allows the player to login if they supply <br /> the correct password for their username</td>
	</tr>
	<tr>
		<td>/auth changepass [oldpass] [newpass]</td>
		<td> none</td>
		<td>Allows the player to change their password</td>
	</tr>
	<tr>
		<td>/auth setpass [player] [password]</td>
		<td>ForgeEssentials.ModuleAuth.admin</td>
		<td>Sets the named players password to the <br /> one supplied</td>
	</tr>
	<tr>
		<td>/auth kick [player]</td>
		<td> ForgeEssentials.ModuleAuth.admin</td>
		<td>Forces the named palyer to login again</td>
	</tr>
	<tr>
		<td>/auth unregister [player]</td>
		<td> ForgeEssentials.ModuleAuth.admin</td>
		<td>Forces the named palyer to register again</td>
	</tr>
</table>


# Other Info <a name="other"></a>
The following improvements are planned for the Auth module.. Mind you these are my dream improvements
* password complexity nforcement
* variable encryption, not just SHA1
* per-player generated salts
* failed login punishments
* AuthModule bans
* Web request authentication
* configurable login and register commands. (force an email anyone?)