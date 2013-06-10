# Description

A Basic server economy module. Players have access to a virtual wallet and with that money they can buy, sell, and transfer it to other players.

# Configuration
``` S:currencySingular=Credit``` the singular form of your currency

``` S:currencyPlural=Credits``` The plural form of your currency

``` I:startbuget=100 ``` _not a typo_ The ammount of money players start with when they join the server

# Commands and Permissions

/addtowallet _player_ _amount_ -- Adds _amount_ to wallet of _player_<br /> &nbsp;&nbsp; **ForgeEssentials.Economy.addtowallet** <br /><br />

/setwallet _player_ _amount_ -- Sets the wallet of _player_ to _amount_<br /> &nbsp;&nbsp; **ForgeEssentials.Economy.setwallet** <br /><br />

/pay _player_ -- Pays a player from your own wallet<br /> &nbsp;&nbsp; **ForgeEssentials.Economy.pay** <br /><br />
/getwallet _player_ -- Display's a _players_ money(wallet)<br /> &nbsp;&nbsp; **ForgeEssentials.Economy.getwallet** <br /><br />

/money -- Displays how much you have in your wallet <br /> &nbsp;&nbsp; **ForgeEssentials.Economy.money** <br /><br />
### Shop setup
Inteded for use with commandblocks.
<br />
<br />
The syntax is:<br />
``/paidcommand <player> <amount> <command [args]>``<br />
``/sellcommand <player> <['amount'x]item[:'meta']> <command [args]>``<br />
Examples:<br />
``/paidcommand @p 100 i diamond 1`` would add 1 diamond for a 100 currency <br />
``/sellcommand @p 64x3:0 i diamond 1`` would add 1 diamond for a stack of dirt(id 3)
### Footnote
<br />
I'm sure that someone will clear this up, or add to it if I don't get to it in the next couple of days. --Zhivotnoya