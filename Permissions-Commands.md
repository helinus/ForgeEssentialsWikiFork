## A New Start
Welcome, one and all, to the fantastical explanation you've all been waiting for:  Permissions commands!
That's right, I've deemed the system finished *enough* to warrant documentation.  So, without further adieu, let us begin!
## Where to Begin
Well, let's start off with the basics. 

### Zones
Zones aren't quite fleshed out and in working order yet, but they work enough for this, and so you need to know what they're about.  Zones allow multiple areas of layered permissions.  For more detailed information, see the "Zones":Zones page.  For the purpose of this document, however, I will say this:  The root zone is called _GLOBAL_.  This is the zone that all WORLD zones reside in.  Each dimension has its own unique Zone.

### Creating Groups
<table><tr><td>/p group create &#60group&#62</td></tr></table>
Yes, I have it notated that way for a reason :P

Groups, by default, are created in the _GLOBAL_ zone.  You can change this by specifying a zone for any [zone] parameter in the commands.

Each zone can have multiple groups, and groups can be part of multiple zones (this particular feature not yet implemented).  Groups specified under the _GLOBAL_ zone are frowned upon, but will serve well enough as cross-world group usage in a pinch.

Now for another tag: _SUPER_.  Use this ZoneName if you have any group that needs to have its permissions checked FIRST, before anything else.  _SUPER_ is also global: it spans worlds.  But unlike _GLOBAL_, which is always checked last, a player's _SUPER_ group is always checked first, before any local zones or world zones.
### Modifying Groups
<table><tr><td>/p group &#60group&#62 (prefix|suffix|parent|priority) set &#60value&#62 [zone]</td></tr></table>

The next topic for groups is changing the settings.  You can display the group's current settings by simply using /p group \<group\> \(prefix|suffix|parent|priority\).  If you want to change them, simply add a "set \<value\>" at the end.  Group prefixes use colored markup with the ampersand (&) and the hex characters.  A group's priority is an integer value, ranging from 0-999, 0 being the lowest, 999 being the highest.  Within a zone, a player can be part of multiple groups, and this serves, first, to tell what group's prefix will be added to a player's chat lines, and second, the order in which permission nodes are checked and utilized.
### Modifying Group's Permissions
<table><tr><td>/p group &#60group&#62 (allow|true|deny|false|clear) &#60perm&#62 [zone]</td></tr></table>

Allow == true, deny == false.  You can use this command to change a group's settings.  Allowing a permission will enable anyone in the group in that zone to use it, unless denied by another zone.  Denying will keep anyone in the group from being able to use the node, even if they're allowed in any other zones or in their private permissions, except in the case of _SUPER_ groups and user permissions.
### Deleting Groups
<table><tr><td>/p group delete &#60group&#62 [zone]</td></tr></table>

Last in this area is the delete command.  Like everything else, it defaults to the worldZone, but you can specify the zone.
### "Here"
Also, you can use the keyword "here" to specify the zone you're in.  The zone manager will search for the lowest-level zone, and work its way up to the WorldZones as its highest reach.

##Users
Next is the users section.  Users can be a part of many different groups.  In fact, it's bound to happen throughout the course of your server, as anyone who makes a zone has admin rights over that zone for the users who come into them.  Players also have their own permissions that you can set.  A player's permissions are checked before the zone and allowed unless the zone specifically denies them the permission.  This is always the case, except when a player has a _SUPER_ permission.  Then that is ALWAYS what is used, whether it's allowed or denied.  Any zone that deals with that specific node has no effect on that node.
### Changing Player Settings
<table><tr><td>/p user &#60player&#62 (prefix|suffix) set [&#60value&#62]</td></tr></table>

The players' prefixes and suffixes are stored as part of their PlayerInfo configs, usually found in the FEData folder (.minecraft/<worldFolder>/FEData/ForgeConfig/PlayerInfo/<username>.cfg).  You can also change it there.  Using the command with `set value` will tell you what the player's current personal prefix or suffix is.
### Modifying User Permissions
<table><tr><td>/p user &#60player&#62 (allow|true|deny|false|clear) &#60perm&#62 [zone]</td></tr></table>

This will act for the player the same way its counterpart command does for groups.  There is one variation you can use, however:

<table><tr><td>/p user supers &#60player&#62 (allow|true|deny|false|clear) &#60perm&#62 [zone]</td></tr></table>
Using it this way allows you to modify a player's super permissions, those that are always taken finally, no matter what other groups or zones affect the specified node.
### Player Group Management
<table><tr><td>/p user &#60player&#62 group [set|add|remove] &#60group_name&#62 [zone]</td></tr></table>

Using this without the set, add or remove keywords will allow you to view the player's current group's name.  Using "set" will clear whatever other groups the player is in, either in the specified zone, or in _GLOBAL_ by default, and add them to the specified group.  Adding merely makes them part of the group in addition to whatever others they may be in, and remove takes them out of the group.

##Examples
Now, I know, when reading that, that it might seem a little confusing.  However, don't worry about the zones too much, as they are a more advanced level of protection and administration.  We made the defaults the way they are so that you don't have to worry about getting your permissions set up quickly.  Any group you create will, by default, be used across all dimensions in your server.  That being said, however, examples are always a great help.  So here's at least one:

Take a player, AbrarSyed.  You want him to be able to use a few commands, and to be able to break and interact with blocks.

The root permission for the Protection module, if you have that installed, is "ForgeEssentials.Protection", and there are four subnodes: "allowEdits", "allowBlockInteractions", "allowEntityInteractions" and "overrideProtection".

Then, say you want him to be able to use /msg, /r, /home, /afk, /bed, /motd, /rules, and /spawn.  If you look over on the [Commands Documentation](Commands), you will find the permission root for /msg and /r are "ForgEssentials.Chat", and the root for the others is "ForgeEssentials.BasicCommands".  You also want to be able to easily assign these permissions to other players.  The answer?  Groups.

What to call our group?  Let's see, most of those are pretty basic, but the ability to modify the world would make it more likely a step above the default, so let's call them Members.  They need a prefix, too, so let's give them dark green which, when referencing the [Minecraft Color Codes](http://www.minecraftwiki.net/wiki/Colors), is 2.  Our color identifier is the ampersand (&), so we'll use &f[&2Member&f] as the prefix code.  So, here's the sequence of commands we would run:

<table><tr><td>/p group create Members</td></tr>
<tr><td>/p group Members prefix set &f[&2Member&f]</td></tr>
<tr><td>/p group Members priority set 10</td></tr>
<tr><td>/p group Members allow ForgeEssentials.BasicCommands.afk</td></tr>
<tr><td>/p group Members allow ForgeEssentials.BasicCommands.bed</td></tr>
<tr><td>/p group Members allow ForgeEssentials.BasicCommands.home</td></tr>
<tr><td>/p group Members allow ForgeEssentials.BasicCommands.home.set</td></tr>
<tr><td>/p group Members allow ForgeEssentials.BasicCommands.motd</td></tr>
<tr><td>/p group Members allow ForgeEssentials.BasicCommands.rules</td></tr>
<tr><td>/p group Members allow ForgeEssentials.BasicCommands.spawn</td></tr>
<tr><td>/p group Members allow ForgeEssentials.Chat.commands.msg</td></tr>
<tr><td>/p group Members allow ForgeEssentials.Chat.commands.r</td></tr>
<tr><td>/p group Members allow ForgeEssentials.Protection.allowEdits</td></tr>
<tr><td>/p group Members allow ForgeEssentials.Protection.allowBlockInteractions</td></tr>
<tr><td>/p group Members allow ForgeEssentials.Protection.allowEntityInteractions</td></tr>
<tr><td>/p group Members allow ForgeEssentials.Protection.pvp</td></tr>
<tr><td>/p user AbrarSyed group set Members</td></tr></table>
And there you go!  AbrarSyed is now a part of the Members group, and can use those specific commands and place/break blocks and utilize right clicks.
## Superperms
Now, what if there was one thing you wanted Abrar, and only Abrar, to be able to do no matter where he was, like, say, /i.  All you'd have to do is run this command:
<table><tr><td>/p user AbrarSyed supers allow ForgeEssentials.BasicCommands.i</td></tr></table>
And bam, Abrar can now give himself whatever he wants, wherever he wants, whenever he wants, no matter what other groups or zones say about that node.  You can do the same for any players you put in staff groups, and make super groups by using the _SUPER_ zone tag.

## Default Groups
Now, there are several default groups that are created for you, to make it a little easier to start off.  They are Guests, Members, ZoneAdmins and Owners.  Here are the permissions each has by default:
### Guests
By default, Guests have no Protection permissions.  They cannot build or destroy, they cannot right-click interact with blocks, and they cannot attack mobs or players or interact with villagers.  However, this is what they do have:<br>
* /list
* /modlist
* /motd
* /rules
* /tps
* /msg
* /r

### Members
Members are where Protection first lets them through.  The have all the permissions the Guests do not.  They also have access to compass teleports.
### Zone Admins
This is basically an admin position, but only in the zones where they have this group.  However, for the initial run, they are essentially global admins.  By default, at the moment, they don't have any more defaults than the other two, but that will probably change shortly.
### Owners
Owners, by default, have all /feperm permissions, and all zone and commands.  The wildcard modifier has not been implemented, though, so you may actually have to make your Owners ops until that can be straightened out.  Eventually, the wildcard will be an _all_ at the end of a node, like "ForgeEssentials.BasicCommands._all_" would give you everything from /afk to /give and /i.

### Setting a default group:

<table><tr><td>/p default set &#60;groupname> [zone]</td></tr></table>