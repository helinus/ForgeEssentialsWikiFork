So, what is the snooper? Its a module of ForgeEssentials that lets you get all kinds of data from your server.
It is based upon (but not compatible with) the vanilla system.

If you want to read about that, go [here](http://dinnerbone.com/blog/2011/10/14/minecraft-19-has-rcon-and-query/).
My PHP example page is based on [this](https://github.com/xPaw/PHP-Minecraft-Query)repo.

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