How to check if your linux computer/system can run ForgeEssentials

You can usually find the hosts file in ``/etc/hosts`` on *nix systems

In this example "ubuntuServer" is the hostname of the computer running the Minecraft server with ForgeEssentials.

To see content of hosts file open file with vi/gedit/nano or run `cat /etc/hosts` - this will print out content of file into console.

### If your hostsfile looks like this:

    127.0.0.1       localhost
    127.0.1.1       ubuntuServer.lan        ubuntuServer

or like this:

    127.0.0.1       localhost
    127.0.1.1       ubuntuServer

**ForgeEssentials will work fine**

### But if it looks like this:

    127.0.0.1       localhost
    127.0.1.1       ubuntuServer.lan

**ForgeEssentials will not work until the hosts file is changed**