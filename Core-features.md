This is where all the features of ForgeEssentials exist that are NOT included in a separate module.

# ModList
A list of all the mods loaded and their versions is included in "./ForgeEssentials/modlist.txt"

# Banning recipes
First off its very easy to use.
The file is located in `./ForgeEssentials/banneditems.cfg`
If you wish to ban the crafting of an item you place the item "id:meta" under "S:List" in the #nocraft section. pretty self explanatory.

Now say you didn't want anyone on your server to be able to craft some items. For this example were going to use a TNT (id=46) and a Chunk Loader(id=243). We will also show you how to ban all variants of an item/block. For that we will use a Mining Laser(id=30208:1 and 30208:27). You have 2 meta's for the mining laser for charged and uncharged so to be safe we ban them both by using "-1" to ban them all in one line.
lets see what this looks like in the cfg.


    ####################
    # nocraft
    #===================
    # Configuration options to make an item uncraftable.
    ####################
    nocraft {
        # Use this format: "id:meta". Use meta -1 to ban ALL variants of an item/block.
        S:List <
            243
            46
            30208:-1
         >