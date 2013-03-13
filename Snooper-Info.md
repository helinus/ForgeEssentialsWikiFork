So, what is the snooper? Its a module of ForgeEssentials that lets you get all kinds of data from your server.
It is based upon (but not compatible with) the vanilla system.

If you want to read about that, go [here](http://dinnerbone.com/blog/2011/10/14/minecraft-19-has-rcon-and-query/).

You can see a static example page [here](https://github.com/ForgeEssentials/ForgeEssentialsMain/tree/master/snooperPHP).

Now, how does it work? I have no clue, It just does. You can look at the code if you'd like.

If you look at the PHP code, you can see that, when GetInfo(...) is called, a hex number is send along. This is the number that determines what response you will get.

### Config options
* enable: If false, no snooper!
* hostname: You should know this if you have done server stuff before.
* overrideIPValue: Set this to the server IP or domain name if its not send correctly. (set overrideIP to true).
* port: This defaults to the MC server port + 1.

## Info send:
Toggle-able settings are marked with this: *(The setting to toggle)
All of the info is send as a JSON string.

### Responces (id = 0)
* All available responces.
This also responds if you send invalid data.

### ServerInfo (id = 1)
* The server IP/hostname *
* The server Port *
* The modlist *
* The MOTD *
* The difficulty
* Server uptime
* MC version
* Default gamemode
* Player slots
* Worldname
* Worldborder information (Only center and radius)
* Players online (count)
* TPS for all dimentions specified in config

### CustomInfo (id = 2)
* Same data as send to MCstats

### PlayerInfo (id = 5, data = username)
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

### PlayerInv (type = 6, data = username)
* Array of 4 armor slots (default stack formatting, see below)
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