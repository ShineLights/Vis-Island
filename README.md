DayZ-Central-Economy || Vis Island Map
--------------------------------------------------------------------------------

![alt text](https://i.imgur.com/nvOCB0J.png)

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

DayZ-Central-Economy || Vis Island Map
--------------------------------------------------------------------------------

# Как использовать/установить миссию?

1. Создайте папку с именем dayzOffline.Vis_Island в каталоге mpmissions вашего сервера и извлеките туда файлы миссий.

2. Отредактируйте serverdz.cfg (в вашем каталоге DayZServer). Внизу определите миссию как dayzoffline.Vis_Island, затем сохраните.

`template="dayzOffline.Vis_Island"; // Mission to load on server startup. <MissionName>.<TerrainName>`

3. Скопируйте мод @Vis_Island в каталог DayZServer.

4. Добавьте мод @Vis_Island в .bat-файл вашего сервера или программное обеспечение для управления.

`"-mod=@Vis_Island;"`

# Обновление миссии

1. Удалите содержимое папки вашей миссии (dayzoffline.Vis_Island), **кроме папки Storage**. Это ваши файлы сохранения.

2. Поместите новые файлы миссии в папку с миссией.

3. Перейдите к dayzoffline.Vis_Island\storage\data и удалите типы.001, типы.002 и типы.bin, чтобы повторно инициализировать таблицу добычи.

# Обновление лута/Mapgrouppos

Мы рекомендуем вам самостоятельно обновлять XML-файлы mapgrouppos/mpgroupcluster после обновлений или при добавлении собственных объектов карты.

Отредактируйте файл init.c, который находится в папке вашей миссии. Добавьте эти строки в конец void main() :

`GetCEApi().ExportProxyData( "7500 0 7500", 15000 );  // Generate mapgrouppos.xml`

`GetCEApi().ExportClusterData();                    // Generate mapgroupcluster.xml`

1. Start server, and an export folder will be created. dayzoffline.Vis_Island/Storage/export. Within, you'll find your new XML's. This may take some time depending on system performance.

2. Stop server. Copy/paste your new .xml's to dayzoffline.Vis_Island.

3. Lastly, comment out the export line we added to init.c.
