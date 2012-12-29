So, what is the snooper? Its a module of ForgeEssentials that lets you get all kinds of data from your server.
It is based upon (but not compatible with) the vanilla system.

If you want to read about that, go [here](http://dinnerbone.com/blog/2011/10/14/minecraft-19-has-rcon-and-query/).
My PHP example page is based on [this](https://github.com/xPaw/PHP-Minecraft-Query) repo.

You can see a static example page [here](http://driesgames.game-server.cc/snooper/static/).
The snooper_php.zip file contains the source code. [Extra link.](http://driesgames.game-server.cc/snooper)

Now, how does it work? I have no clue, It just does. You can look at the code if you'd like.

If you look at the PHP code, you can see that, when GetInfo(...) is called, a hex number is send along. This is the number that determines what response you will get.

* 0) Server info
* 1) All the online players
* 2, 3, 4) Nothing, reserved for general info.
* 5) Player info *
* 6) Player armor *
* 7) player inventory *

*= For these you need to send the username too. In the example page it gets done through GET_["player"].

## Config options

* enable: If false, no snooper!
* autoReload: If true, attempts to restore after error (the query only!).
* hostname: You should know this if you have done server stuff before.
* overrideIPValue: Set this to the server IP or domain name if its not send correctly. (set overrideIP to true).
* port: This defaults to the MC server port.

## Info send:
You can't toggle this response off completely.
Toggle-able settings are marked with this: *(The setting to toggle)
All of the info is send as a JSON string.
### Server Info

* The server IP/hostname *(send_IP)
* The server Port *(send_IP)
* The modlist *(send_Mods)
* The MOTD *(send_MOTD)
* The difficulty
* Server uptime
* MC version
* Default gamemode
* Player slots
* Worldname
* Worldborder information (Only center and radius) *(send_WorldBorder)
* Players online (count)
* TPS for all dimentions specified in config
