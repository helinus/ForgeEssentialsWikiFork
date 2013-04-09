## In the beginning there was Chaos

Welcome to this little tutorial and/or bank of ideas how to use Permissions and Zones to improve your server and add new features.

You will find few examples here and you can practice by copying them into your server/singleplayer test world.

No matter if you find the knowledge on this page useful or not, remember this:

**Creativity is all that matters**

By using imagination and creativity you can accomplish things that developers of ForgeEssentials didn't even think of.

So, what are you waiting for?

Read this page to find out more or proceed to implementing your own ideas on your server!

**NOTE:** This page was created based on a working beta build: 1.5.1-1.2.1.43 and will be continued with next releases.	

## Let's get started

Most of the stuff here is adaptation of mechanics found among Bukkit plugins.

All you need to implement them to your server is Forge Essentials.

Remember, Permissions are easy to edit in flatfile (config outside of Minecraft), but you can work from ingame and it will work just as well. =)

## Quick list of examples

**You can quickly jump to an example of choice.**

[World Guard](https://github.com/ForgeEssentials/ForgeEssentialsMain/wiki/Use-of-ForgeEssentials-in-practice#world-guard)

## World Guard

**Requirements:**

ForgeEssentials, Protection submod

**What is it:**

Our example player is called Bruce. Meet Bruce: he is a new player who just came to our server. He would love to own a plot of land, but is scared of random griefers from the outside!

Poor Bruce, what can we do to help him?
**We make a World Guard around a plot of his choice**

World Guard is disabling or allowing specific permissions for specific groups or players in specific area.
I.e. preventing anyone but Bruce to build, destroy or use items in his own plot.

**How it works:**

You can define zones by selecting an area with a wand (see: _//fewand_ command).
By default, new zones belong to no other zone, but you can then set a 'parent' zone for that specific zone. That will connect groups (and not only) belonging to the parent-zone with the child-zone.

Now, depending on how you created your server groups, you may have a set of totally different groups from the example ones, but that does not matter here.

You can allow or deny permissions for each group to any zone (as long as the group is connected to that zone) and you can do the same for users.

In the example, we will deny protection permissions, but you can deny or allow any permissions you like for any group or user.

**How to:**

In the example, the default group for all regular players is group called "Members".

Bruce is scared of Members griefing his house, so he asks us to make a World Guard around his house.

We have to keep in mind Bruce is part of Members, too!

**1)** Define a zone around Bruce's plot.

To do that, we need to select an area around his plot with a wand.

We assume that you already know how to make a wand (see _//fewand_ command) and select areas by touching blocks with left/right click while holding a wand.

Once we have the plot selected, we can use an //expand command to expand the plot a bit underground and into the air, or on the sides.

Bruce is going to build a basement and a tower on his plot, so we expand the selection up and down a bit, using these commands:

`//expand down 20`

`//expand up 20`

If you have client-side selection mod, you will see how your selection is much taller now.

Now, to define the zone, we will call it _bruceplot_ and use this command:
`/zone define bruceplot`

We will be using the _GLOBAL_ zone as a parent to import the Members group into the zone:
`/zone setparent bruceplot _GLOBAL_`

That's it for the zone.

**2)** Deny (set to false) the protection permissions for all members inside the _bruceplot_ zone

To do that, we have to use following commands:

`/p group Members deny ForgeEssentials.Protection.allowBlockInteractions bruceplot`

`/p group Members deny ForgeEssentials.Protection.allowEdits bruceplot`

Let's explain from the start:

_/p group_ is part of the command where we are 'entering group permissions editing branch of commands' :)

_Members_ is the name of group we are disallowing to build on _bruceplot_

_deny [permission name]_ is of course the part where we choose to deny X permission

_bruceplot_ is the name of zone affected, if you left it blank it would use _GLOBAL_ zone as default

Congratulations, by now you would have disabled permission to build for all Members on _bruceplot_!

**3)** Allow Bruce to build on his plot of land

Bruce is part of Members group, so at the moment he can't build on his plot. Let's fix it by allowing him to! We will use a universal permission:

_ForgeEssentials.Protection.overrideProtection_

which makes the group/user to use their own permissions for Protection instead of those set in the zone.

`/p user Bruce allow ForgeEssentials.Protection.overrideProtection bruceplot`

This is similar in construction to groups, except we are allowing an user's protection permissions to override those set in the zone, and not denying permissions for a group.

This is it! Bruce has now a very own plot of land, where regular players with group Members can't build or destroy blocks.

They also can't interact with blocks (i.e. open chests), so he's safe now! Yay!