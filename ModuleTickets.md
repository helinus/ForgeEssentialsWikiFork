* [Installation](#install)
* [Configuration](#config)
* [Usage](#use)
* [Commands](#command)
* [Other Info](#other)

# Installation <a name="install"></a>
Put this module in the mods folder. If the Core is installed, it will be loaded.

# Configuration <a name="config"></a>

``ForgeEssentials/Tickets/config.cfg``

    S:categories <
        griefing
        overflow
        dispute
     >

Add new categories by putting each new one on it's own line

# Usage <a name="use"></a>
There are three categories to create tickets in, griefing, overflow and dispute.
More can be added in the config file.

To create a ticket in the category ``griefing`` with the message ``dries007 put lava in my wooden house`` at the spot where the player stands he/she types ``/ticket new griefing dries007 put lava in my wooden house`` in chat.

When a player with the permission node ``ForgeEssentials.Tickets.admin`` logs in he/she get's the text ``There are 'numberOfOpenTickets' open tickets.`` in chat

# Commands <a name="command"></a>
<table>
	<tr>
		<th>Command Usage</th>
		<th>Aliases</th>
		<th>Permission Node</th>
		<th>Description</th>
	</tr>
	<tr>
		<td>/ticket</td>
		<td>/tickets</td>
		<td>ForgeEssentials.Tickets.command</td>
		<td>Prints usage help in chat</td>
	</tr>
	<tr>
		<td>/ticket list 'page'</td>
		<td></td>
		<td>ForgeEssentials.Tickets.view</td>
		<td>Prints a paged list of tickets in chat</td>
	</tr>
	<tr>
		<td>/ticket new 'category' 'message'</td>
		<td></td>
		<td>ForgeEssentials.Tickets.new</td>
		<td>Creates a new ticket in the specified category with the message you specified</td>
	</tr>
	<tr>
		<td>/ticket view 'id'</td>
		<td></td>
		<td>ForgeEssentials.Tickets.view</td>
		<td>Prints the ticket information in chat</td>
	</tr>
	<tr>
		<td>/ticket tp 'id'</td>
		<td></td>
		<td>ForgeEssentials.Tickets.tp</td>
		<td>Teleports you to the location where the ticket was created</td>
	</tr>
	<tr>
		<td>/ticket del 'id'</td>
		<td></td>
		<td>ForgeEssentials.Tickets.admin</td>
		<td>Deletes the ticket specified</td>
	</tr>
	<tr>
</table>


# Other Info <a name="other"></a>
