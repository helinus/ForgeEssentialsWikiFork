In this tutorial you will learn how to open H2DB Files. ForgeEssentials' Database files.
For this tutorial you will need the following things:
* SQL Workbench
* H2DB files location folder (ForgeEssentials folder)
First things first, you need SQL Workbench, so download it from [here](http://bit.ly/9PML5I). Then, you need to install it.
After installing, launch SQL Workbench and click File -> Connect Window(Alt + C). From there you can name your profile, select a driver and enter the location in the URL text field.
So after naming your profile you can select the driver, the driver required to open the database is "H2 Database Engine(org.h2.Driver)", upon selecting it, you will get a pop up window like [this](http://prntscr.com/ozyv8). Click "yes", a new window will pop up looking like [this](http://prntscr.com/p07w4)The only field you need to modify is "Library" you want to select the "H2DB.jar" file in the "lib" folder of your Minecraft Server. Click "open" followed by "ok", then for the URL you want to locate the db file you want to modify, e.g. "Server/ForgeEssentials/H2-Data", then in the URL you will want to type "jdbc:h2:file:Server/ForgeEssentials/H2-Data". In order to view the table you need to open the Database Explorer, you can do so by click Tools -> Show Database Explorer(Ctrl + D). And now you're done!
Thanks to Malk on the IRC channel for helping me figure it out.