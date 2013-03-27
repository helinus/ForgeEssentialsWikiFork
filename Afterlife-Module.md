* [Installation](#install)
* [Configuration](#config)
* [Other Info](#other)

This module adds a DeathChest (in form of a player Skull), Potion effects on respawn and adjustable HP and hunger levels on respawn.

# Installation <a name="install"></a>
Simply putting the module zip into the mods folder should be sufficient.

# Configuration <a name="config"></a>
The configuration file is split into multiple categories.
### AfterLife.DeathChest
`B:Enable=true` Enables the creation of DeathChests when a player dies

`B:EnableXP=true` Enables DeachChests to store the XP of their player onDeath

`B:enableFencePost=true` Put the DeathChest on a fence post

`I:protectionTime=300` How long the chest should be protected from anything other than the player whose chest it is.

### AfterLife.respawnStats
*note* that Minecraft measures food and health in halves. So a level of 20 means 10 full hearts/food things.

`I:foodlvl=20` The food level the player should have when they respawn.

`I:hp=20` The hp level the player should have when they respawn.

### AfterLife.respawnDebuff
This property is a list of potion effects. They are to be inputted in the format `#ID:#duration:#amplifier`

`4:150:1` Fatigue I for 150 seconds.


# Other Info <a name="other"></a>
Module was coded by Dries007. If you have issues, you might get fastest response if you put @dries007 in the issue info.

The configurations in this module may be converted to PermissionProps so that they can be configureable per-player, per-group, and per-zone.