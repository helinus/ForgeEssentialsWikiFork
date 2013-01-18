A Zone is first and foremost an area definition. Think regions from WorldGuard. You can select an area, and create a zone of that area. Once a zone has been created, you can set permissions on the zone. This means that a permission that may be denied throughout the server, may be allowed in a certain zone, or even the opposite. You may also set permissions to specific players while they are in zones, or specific groups in the zone. This functionality allows the ForgeEssentials to take the role of Towny, PeX, WorldGuard, Residence, or any other permissions and protection system.

## Automagically generated groups, zones, and players
### the _\_GLOBAL__ zone
The GLIOBAL zone is a zone the encompasses the entire server. Any permissions set here would be set for players and groups no matter where they are on the server. This allows server-wide ranks or protections.

### _WORLD__  zones
The WORLD_ zones are zones that are automatically created for every world that loads on the server. This allows an entire world to be treated as a zone. They are especially useful with MystCraft because it allows you to set permissions for a certain dimension while leaving the GLOBAL permissions intact.

### the _\_DEFAULT__ group
This is an automatically generated group that stands for the zone. Think of anything set here as a WorldGuard flag. This is usually the place where CommandBlocks, Pistons, and liquids check for their permissions if they are allowed to act in a given zone. It is also a fallback for players and groups. See the examples section for the DEFAULT group in action.

### the _\_ENTRY_PLAYER__ player
This is an automatically generated player that is used for any players when they log into a server for the first time. Players will continue to use the Entry Group until they are added to another group via commands or manually imported from the permissions configs. When a server using ForgeEssentials is started for the first time, the ENTRY_PLAYER is added to the Guests group. This means that any player that logs into the server, will be a part of the guests group as well.

## The permission check hierarchy
// incomming picture //
When a permission is checked.. the first thing that happens is the zone the target is in, is found. Lets take a player for example...  
 - 1 - Find the Players Zone.
 - 2 - Check if the Player has this permission allowed in this zone. ? undefined? goto #3
 - 3 - Get all the groups the player is part of in this zone and check them for this permission. ? undefined? goto #4
 - 4 - Get the parent of this zone. goto #1
Using this process, the permission checks will eventually go up to the _\_GLOBAL__ zone if they are not defined. If they are not defined in the _\_GLOBAL__ zone, then they will default to false