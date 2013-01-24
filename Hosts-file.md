How to check if your linux computer/system can run ForgeEssentials

You can usually find the hosts file in ``/etc/hosts`` on Debian based systems

In this example "UbuntuServer" is the hostname of the computer running the Minecraft server with ForgeEssentials.


### If your hostsfile looks like this:

    127.0.0.1       localhost
    127.0.1.1       ubuntuServer.lan        ubuntuServer

or this:

    127.0.0.1       localhost
    127.0.1.1       ubuntuServer

**ForgeEssentials will work fine**

### But if it looks like this:

    127.0.0.1       localhost
    127.0.1.1       ubuntuServer.lan

**ForgeEssentials will not work**