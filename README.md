DayZ-Central-Economy Setup Guide | Vis Island DayZ Map
--------------------------------------------------------------------------------

Vis is an island in the Adriatic Sea, in the southern part of Croatia, not far from the coast of Dalmatia. Vis has an area of ​​90.26 square kilometers. This is a huge island with many beautiful places and cities. Despite the pleasant summer weather, you will have to face equally dangerous infected, animals and other survivors.

Features:
*Map based on a real island
*New level of map detail
*Custom assets, surfaces, loadingscreens, and more...

![alt text](https://i.imgur.com/nvOCB0J.png)

Vis Island (Steam) - https://steamcommunity.com/sharedfiles/filedetails/?id=3031438368

Vis Island Winter Version (Steam) - https://steamcommunity.com/sharedfiles/filedetails/?id=3067553021


Map under development. For all comments, suggestions, instructions, questions, mission files, help and more, please join our Discord - https://discord.gg/barKHWyRQJ


![alt text](https://i.imgur.com/ZuzqlOa.png)

# How to use/install mission?

1. Create a folder called dayzOffline.Vis_Island in your server's mpmissions directory, and extract the Mission Files there.

2. Edit serverdz.cfg (in your DayZServer direcory). Near the bottom, define mission as dayzoffline.Vis_Island, then save.

`template="dayzOffline.Vis_Island"; // Mission to load on server startup. <MissionName>.<TerrainName>`

3. Copy @Vis_Island mod to your DayZServer directory.

4. Add @Vis_Island mod to your server .bat, or management software.

`"-mod=@Vis_Island;"`

# How to update mission

1. Delete the contents of your mission folder ( dayzoffline.Vis_Island), **except for the Storage folder**. These are your persistence files.

2. Place new mission files in your mission folder.

3. Navigate to dayzoffline.Vis_Island\storage\data and delete types.001, types.002, and types.bin to reinitialize the loot table.

# Updating Loot/Mapgrouppos (end-user)

We recommend you update mapgrouppos/mpgroupcluster xml's yourself after updates, or when adding your own map object's.

Edit init.c, found within your mission folder. Add these lines to the bottom of void main() :

`GetCEApi().ExportProxyData( "7500 0 7500", 15000 );  // Generate mapgrouppos.xml`

`GetCEApi().ExportClusterData();                    // Generate mapgroupcluster.xml`

1. Start server, and an export folder will be created. dayzoffline.Vis_Island/Storage/export. Within, you'll find your new XML's. This may take some time depending on system performance.

2. Stop server. Copy/paste your new .xml's to dayzoffline.Vis_Island.

3. Lastly, comment out the export line we added to init.c.
