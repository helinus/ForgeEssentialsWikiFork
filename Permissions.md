This was written by Tux2 on the Technicpack forums website, i am simply copying it here for the benefit of others. I do not take any credit for this work


All permissions files are generated on first run of the server and are stored in the folder # ForgeEssentials/permisions.

## 1. groups.cfg
This lists all your groups on the server. Below is a commented entry showing you exactly how to format it.
`#The group name
    Admins {
        #The chat prefix. Notice it uses § and not the typical "&" sign.
        S:chatPrefix=§4[Admin]§f
        #The chat suffix. Same format as chat prefix.
        S:chatSuffix=
        #This is the group priority and must be a number between 0-999 (I found out this the hard way)
        #Also, if a group doesn't have a parent, it can't share the priority of another group.
        I:groupPriority=998
        #The parent group to inherit permissions from.
        #If there's a chat prefix/suffix up there, you can't put a parent. (Probably a glitch)
        S:parent=
    }`

## 2. permissions.cfg
This lists all the permissions for each of the groups you specified. Below is the corresponding entry for the group name above.
`#The group name that you specified in groups.cfg
        Admins {
            #I don't know what the B stands for, but you need it at the front. The rest is the permission that you want to deny or allow.
            B:ForgeEssentials.BasicCommands.ban=true
            B:ForgeEssentials.BasicCommands.kick=true
            B:ForgeEssentials.BasicCommands.pardon=true
            B:ForgeEssentials.BasicCommands.spawn=true
            #The next 3 entries are important if you want this group to be able to open chests, place blocks, or kill mobs. In that order.
            B:ForgeEssentials.Protection.allowBlockInteractions=true
            B:ForgeEssentials.Protection.allowEdits=true
            B:ForgeEssentials.Protection.allowEntityInteractions=true
            #The following is for other stuff that isn't quite implemented yet.
            B:ForgeEssentials.Protection.overrideProtection=true
            B:ForgeEssentials.TeleportCenter.BypassCooldown=true
            B:ForgeEssentials.TeleportCenter.BypassWarmup=true
            B:ForgeEssentials.backup=true
            B:ForgeEssentials.permissions=false
        }`

## 3. players.cfg
All the players that aren't in the default group go in this file. Below is a user in the admin group.
`#The player name
    GingerMay77 {
        #The custom user chat prefix. Uses same format as the group one.
        S:chatPrefix=
        #Custom suffix for chat for this user.
        S:chatSuffix=
        #The groups this user is in. If more than one they are separated by a new line.
        S:group <
            Admins
        >
    }`

Please note that as far as I know the /fereload command doesn't work to reload permissions, so you will have to manually restart your server for every change to the permissions files.

So, there you have it! A quick run down of how to successfully edit your permissions on Tekkit Lite!

# Troubleshooting:
**Problem**: My server crashed and now players can't place blocks, help!
**Answer**: Remove the config folder and delete the sqlite.db located in the ForgeEssentials folder. Then restore the config file from a known good backup. Restart the server and everything should work perfectly.

**Problem**: It doesn't work for me, can I see your entire config files?
**Answer**: sure
## groups.cfg
`# Configuration file
# Generated on 1/7/13 3:34 AM
 
####################
# _GLOBAL_
####################
 
_GLOBAL_ {
    ####################
    # Members
    ####################
 
    Members {
        S:chatPrefix=§2[Member]§f
        S:chatSuffix=
        I:groupPriority=1
        S:parent=
    }
 
    ####################
    # Owners
    ####################
 
    Owners {
        S:chatPrefix=§6[Owner]§f
        S:chatSuffix=
        I:groupPriority=999
        S:parent=
    }
 
    ####################
    # Admins
    ####################
 
    Admins {
        S:chatPrefix=§4[Admin]§f
        S:chatSuffix=
        I:groupPriority=998
        S:parent=
    }
 
    ####################
    # ZoneAdmins
    ####################
 
    ZoneAdmins {
        S:chatPrefix=§6[ZAdmin]§f
        S:chatSuffix=
        I:groupPriority=997
        S:parent=
    }
 
    ####################
    # _DEFAULT_
    ####################
 
    _DEFAULT_ {
        S:chatPrefix=§b[User]
        S:chatSuffix=§f
        I:groupPriority=0
        S:parent=
    }
 
    ####################
    # _PROMOTION_LADDERS_
    ####################
 
    _PROMOTION_LADDERS_ {
        S:DEFAULT <
            Owners
            Admins
            ZoneAdmins
            Members
            _DEFAULT_
        >
    }
 
}`


## permissions.cfg
`# Configuration file
# Generated on 1/7/13 3:34 AM
 
####################
# _GLOBAL_
#===================
# the last stop where permissions get checked before their defaults
####################
 
_GLOBAL_ {
    ####################
    # groups
    ####################
 
    groups {
        ####################
        # ZoneAdmins
        ####################
 
        ZoneAdmins {
            B:ForgeEssentials.BasicCommands.spawn=true
            B:ForgeEssentials.Protection.allowBlockInteractions=true
            B:ForgeEssentials.Protection.allowEdits=true
            B:ForgeEssentials.Protection.allowEntityInteractions=true
            B:ForgeEssentials.Protection.overrideProtection=true
            B:ForgeEssentials.permissions.zone.setparent=true
        }
 
        ####################
        # Members
        ####################
 
        Members {
            B:ForgeEssentials.BasicCommands.spawn=true
            B:ForgeEssentials.Protection.allowBlockInteractions=true
            B:ForgeEssentials.Protection.allowEdits=true
            B:ForgeEssentials.Protection.allowEntityInteractions=true
            B:ForgeEssentials.Protection.overrideProtection=false
        }
 
        ####################
        # _DEFAULT_
        ####################
 
        _DEFAULT_ {
            B:ForgeEssentials.Protection.allowBlockInteractions=true
            B:ForgeEssentials.Protection.allowEdits=true
            B:ForgeEssentials.Protection.allowEntityInteractions=true
            B:ForgeEssentials.Protection.overrideProtection=false
        }
 
        ####################
        # Owners
        ####################
 
        Owners {
            B:ForgeEssentials.BasicCommands.ban=true
            B:ForgeEssentials.BasicCommands.kick=true
            B:ForgeEssentials.BasicCommands.pardon=true
            B:ForgeEssentials.BasicCommands.spawn=true
            B:ForgeEssentials.Protection.allowBlockInteractions=true
            B:ForgeEssentials.Protection.allowEdits=true
            B:ForgeEssentials.Protection.allowEntityInteractions=true
            B:ForgeEssentials.Protection.overrideProtection=true
            B:ForgeEssentials.TeleportCenter.BypassCooldown=true
            B:ForgeEssentials.TeleportCenter.BypassWarmup=true
            B:ForgeEssentials.backup=true
            B:ForgeEssentials.commands.reloadquery=true
            B:ForgeEssentials.permissions=true
        }
 
        ####################
        # Admins
        ####################
 
        Admins {
            B:ForgeEssentials.BasicCommands.ban=true
            B:ForgeEssentials.BasicCommands.kick=true
            B:ForgeEssentials.BasicCommands.pardon=true
            B:ForgeEssentials.BasicCommands.spawn=true
            B:ForgeEssentials.Protection.allowBlockInteractions=true
            B:ForgeEssentials.Protection.allowEdits=true
            B:ForgeEssentials.Protection.allowEntityInteractions=true
            B:ForgeEssentials.Protection.overrideProtection=true
            B:ForgeEssentials.TeleportCenter.BypassCooldown=true
            B:ForgeEssentials.TeleportCenter.BypassWarmup=true
            B:ForgeEssentials.backup=true
            B:ForgeEssentials.permissions=false
        }
 
    }
 
}`

## players.cfg
`# Configuration file
# Generated on 1/7/13 3:34 AM
 
####################
# _GLOBAL_
#===================
# This is interpretted as the SUPER. Meaning it is layered on TOP of everything specified in other places (groups, zones etc.) This applies only to the Suffix and Prefix properties.
####################
 
_GLOBAL_ {
    ####################
    # AbrarSyed
    ####################
 
    AbrarSyed {
        S:chatPrefix=§4[DevLead]§f
        S:chatSuffix=
        S:group <
            Owners
        >
    }
 
    ####################
    # An_Sar
    ####################
 
    An_Sar {
        S:chatPrefix=§2[AwesomeGuy]§f
        S:chatSuffix=
        S:group <
            Members
        >
    }
 
    ####################
    # Luacs1998
    ####################
 
    Luacs1998 {
        S:chatPrefix=§c[Dev]§f
        S:chatSuffix=
        S:group <
            ZoneAdmins
        >
    }
 
    ####################
    # MysteriousAges
    ####################
 
    MysteriousAges {
        S:chatPrefix=§c[Dev]§f
        S:chatSuffix=
        S:group <
            ZoneAdmins
        >
    }
 
    ####################
    # Bob_A_Red_Dino
    ####################
 
    Bob_A_Red_Dino {
        S:chatPrefix=§c[Dev]§f
        S:chatSuffix=
        S:group <
            ZoneAdmins
        >
    }
 
    ####################
    # Dries007
    ####################
 
    Dries007 {
        S:chatPrefix=§c[Dev]§f
        S:chatSuffix=
        S:group <
            ZoneAdmins
        >
    }
 
    ####################
    # Tux2
    ####################
 
    Tux2 {
        S:chatPrefix=
        S:chatSuffix=
        S:group <
            Owners
        >
    }
 
    ####################
    # GingerMay77
    ####################
 
    GingerMay77 {
        S:chatPrefix=
        S:chatSuffix=
        S:group <
            Admins
        >
    }
 
    ####################
    # Sean_McCarthyism
    ####################
 
    Sean_McCarthyism {
        S:chatPrefix=
        S:chatSuffix=
        S:group <
            Admins
        >
    }
 
    ####################
    # crunkatog
    ####################
 
    crunkatog {
        S:chatPrefix=
        S:chatSuffix=
        S:group <
            Admins
        >
    }
 
    ####################
    # PrinceNightFire
    ####################
 
    PrinceNightFire {
        S:chatPrefix=
        S:chatSuffix=
        S:group <
            Admins
        >
    }
 
}`