## Syntax Explanation
Take this command as an example: "/rules [\<number> \<"remove">|\<new rule>]"  
**/rules:** The command itself. Always preceded by / or in some cases, //  
**[\<number> remove|\<new rule>]:** This is an optional argument. Anything surrounded by [] is optional. Inside of the optional brackets are the required brackets, \<>. These mean that the argument within the \<> is required if the argument within the [] is used. "remove" has quotation marks, meaning that it is a literal word that can be used as an argument. Here are some examples of valid commands:  
**/rules:** All the arguments after the command are surrounded by [], meaning they are optional as a whole.  
**/rules 2 remove:** The optional argument requires 2 sub-arguments. If that optional argument is used at all, all sub-arguments must be provided.  
**/rules 2 No TNT:** This is also valid because one option for the second argument is the enter any new rule that you want. In this case, the new rule can be multiple words. This is not the case with all commands.  
Here are some invalid commands:  
**/rules 2:** The argument is provided, so both sub-arguments are necessary, not just one.  
**/rules remove 2:** The arguments are backwards. The game will think that you want rule number remove to be 2, not rule 2 to be removed. It will likely tell you about this mistake in a hurtful way.  
## User Commands
### /back  
Teleport to your last death point.  
### /butcher [radius] [x, y, z]
Kill all mobs within a certain radius, or 15 blocks by default. Excludes villagers and tamed animals.  
### /home [here|x, y, z]  
Teleports your to your home. "/home here" sets your home to your current location. "/home x y z" sets your home to specific coordinates, where x, y, and z are numbers.  
### /kill [player]  
Kill yourself or the specified player.  
### /motd [new motd]  
Get the message of the day or set a new MOTD.  
### /remove [radius] [x, y, z]  
Remove all item entities within a certain radius, or 15 blocks by default.  
### /rules [\<number> remove|\<new rule>]  
Get the rules of the server. Specify a rule number and either a new rule or "remove" to add or remove a rule, respectively.  
### /smite [me|\<player>]
Strike the block your are looking at with lightning, or specify "me" or a player's name to strike yourself or another player, respectively.

## WorldControl Commands

## Admin Commands
### /restart
Restarts the server.
### /serverdo <command> [arg1] [arg2]...
Allows a player to enter console commands.