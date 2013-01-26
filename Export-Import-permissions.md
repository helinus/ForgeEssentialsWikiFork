Type ``/p export`` in the server console or in-game.

You will get the following files on your ``ForgeEssentials/Permissions/export`` folder:

    players.txt
    groups.txt
    permissions.txt

Edit them in your choice of text editor.

When finnished with the edits you rename the ``ForgeEssentials/Permissions/export`` folder to ``ForgeEssentials/Permissions/import``.

Open the file ``config.cfg`` in the ``ForgeEssentials/Permissions`` folder in your choice of text editor and find the line with ``B:import=false`` in it.

Change that to ``B:import=true``, save the file and restart your server.

Done.