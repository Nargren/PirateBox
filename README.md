PirateBox Landing Website Design
=========

Website deigns for the 0.5 (lighttpd) version of PirateBox.
For more info please read Wiki or go to http://ubuntuhak.blogspot.com


Most of the modifications I have made have been to add support for station_cnt.

station_cnt is an optional modification for your PirateBox which enables you to see how many clients are connected.
To add it, please see:

http://piratebox.aod-rpg.de/dokuwiki/doku.php?id=modification_list#show_connected_clients


###---How to install---###
####Experimental Install####
This is a test procedure trying to make using my design easier. Do as follows:

- Download pbIMG_ws_NargrensD2.img
- Plug in your PirateBox's USB to your computer
- Copy this file to USB/PirateBox folder
- Rename the file "pbIMG_ws.img" to "pbIMG_ws_BACKUP.img"
- Rename the file "pbIMG_ws_NargrensD2.img" to "pbIMG_ws.img"
- Remove the USB from your computer, plug in to router and boot

If you want to stop using my design, simply rename the files again,keeping in mind that the design contained in te pbIMG_ws.img is always used.

####Normal Install####
- Download the source code as zip or tar.gz and plug your USB stick into your computer.
- Unzip/unpack and place the contents of Design2.0 into

```
PirateBox\Shared\src\
```

- Plug the USB stick into the PirateBox and power it up.
- SSH into your PirateBox and run the following commands:

```
cd /opt/piratebox/www/
cp index.html Shared/src/old_index.html
cp Shared/src/index.html index.html
cp Shared/src/main.css main.css
cp Shared/src/mindex.html mindex.html
cp Shared/src/mobile.css mobile.css
cp Shared/src/piratebox-logo_large.png piratebox-logo_large.png
cp Shared/src/jquery.min.js jquery.min.js
cp Shared/src/chat.html chat.html
```

If you have a www_alt folder, you can just place them there instead.

###---Customize---###
- Specially in Nagren's 2.0 design you can pretty much change any text in the html documents (even the image) as the layout is organized by the css file and it will not (should not) change. If you do not need for example the mobile page, feel free to remove it or do any other alterations to your copy.
- (OPTIONAL)If you already have your own forum, simply copy it over to your /piratebox/www folder and name it forum.html and complete the link to it in index.html

By default the share folder is "/Shared", if you have anything else than this please change index.html accordingly.

###---How to delete---###

```
cd /opt/piratebox/www/
cp Shared/src/old_index.html index.html
rm main.css
rm mindex.html
rm mobile.css
rm piratebox-logo_large.png
```

You can plug your USB stick into your computer and delete all the other files you don't need.
(A copy of the files from Design2.0 will be placed on your USB stick, under PirateBox/Shared/src/ )


###---Credits---###
Nargren for doing 99,999999999% of the work in here (creating Design2.0).

Matthias Strubel for developing the PirateBox.

David Darts for having the awesome idea.
