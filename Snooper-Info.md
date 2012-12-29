So, what is the snooper? Its a module of ForgeEssentials that lets you get all kinds of data from your server.
It is based upon (but not compatible with) the vanilla system.

If you want to read about that, go [here](http://dinnerbone.com/blog/2011/10/14/minecraft-19-has-rcon-and-query/).
My PHP example page is based on [this](https://github.com/xPaw/PHP-Minecraft-Query) repo.

You can see a static example page [here](http://driesgames.game-server.cc/snooper/static/).
The snooper_php.zip file contains the source code. [Extra link.](http://driesgames.game-server.cc/snooper)

Now, how does it work? I have no clue, It just does. You can look at the code if you'd like.

If you look at the PHP code, you can see that, when GetInfo(...) is called, a hex number is send along. This is the number that determines what response you will get.

### Config options
* enable: If false, no snooper!
* autoReload: If true, attempts to restore after error (the query only!).
* hostname: You should know this if you have done server stuff before.
* overrideIPValue: Set this to the server IP or domain name if its not send correctly. (set overrideIP to true).
* port: This defaults to the MC server port.

## Info send:
You can't toggle this response off completely.
Toggle-able settings are marked with this: *(The setting to toggle)
All of the info is send as a JSON string.

### Server Info (type = 0x00)
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

### Players online (type = 0x01)
* An array of players online.

### Player info (type = 0x05, extra data = username)
* Gamemode
* Capabilities (allowFly, edit, isFly & noDamage)
* Armor value
* XP (lvl & bar)
* Current group
* Health
* foodStats (saturation & fool)
* ping
* Money
* Current position (default point formatting, see below)

### Player armor info (type = 0x06, extra data = username)
* Array of 4 armor slots (default stack formatting, see below)

### Player inventory info (type = 0x06, extra data = username)
* Boolean Enchantments, If this is true, the enchantments where send along. This gets only false if the text to send was too long (> 2000 characters).
* Array of all used inventory slots (default stack formatting, see below)

## Formatting
### Stack format:
This is the format used to send info about itemstacks. To reduce bandwidth usage and to fit as much data in 1 go as possible, the amount of data send is minimal. You will always get:
* Item ID
* Item name (the nice one, like "Diamond Chestplate")

Optional data:
* Enchantments, Only if it was requested.
* Damage value, If not 0.
* Stacksize, if > 1.
* Actual item-name (if item was re-named using anvil) ("tile." and "item." are removed)

### Point format:
You get whats available.
Sometimes only X, Y and Z.
Most of the time you'll get the dimension too.
Sometimes (warps and homes) you can get the pitch and yaw too.