# Description

Allows you to have a basic server economy.  Good if you have bukkitForge installed as well, and you have Jobs installed.  Give players another means to buy/sell stuff in a market.  Also good as a reward for voting.

# Configuration

Configuration file is pretty straight forward.  Here's mine as a reference.  It can be found in the ForgeEssentials/Economy directory of your server.
<br /><br />
> economy { <br />
>     S:currencyPlural=Kredits <br />
>     S:currencySingular=Kredit <br />
>     I:startbuget=100  _that's a not my typo...that's how it's spelled in the config_ :) <br />
> } 
<br /> <br />

# Commands and Permissions

/addtowallet _player_ _amount_ -- Adds _amount_ to wallet of _player_<br /> &nbsp;&nbsp; **ForgeEssentials.Economy.addtowallet** <br /><br />

/setwallet _player_ _amount_ -- Sets the wallet of _player_ to _amount_<br /> &nbsp;&nbsp; **ForgeEssentials.Economy.setwallet** <br /><br />

/pay _player_ -- Pays a player from your own wallet<br /> &nbsp;&nbsp; **ForgeEssentials.Economy.pay** <br /><br />
/getwallet _player_ -- Display's a _players_ money(wallet)<br /> &nbsp;&nbsp; **ForgeEssentials.Economy.getwallet** <br /><br />

/money -- Displays how much you have in your wallet <br /> &nbsp;&nbsp; **ForgeEssentials.Economy.money** <br /><br />