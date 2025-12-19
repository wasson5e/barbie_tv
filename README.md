# barbie_tv
Automated media player for Barbie Dream House

## Test Build on W Zero
```
Re: vlc automatic start at boot up
Tue Sep 11, 2012 1:47 pm

There are a couple of things to learn here:

1. .desktop files
2. m3u playlists (or another playlist format supported by vlc)

Here's an example which I just put together and tested.

First, make a directory in /home/pi/.config/ called autostart
Code: Select all

mkdir /home/pi/.config/autostart
Next, we need to create a .desktop file with the vlc exec instructions, including the location of the playlist.
Code: Select all

nano /home/pi/.config/autostart/autovlc.desktop
Code: Select all

[Desktop Entry] 
Type=Application
Exec=vlc /home/pi/playlist.m3u
Then, we need to populate the playlist file with file locations. Here's the following for example, you'll obviously need to create the correct paths for your music collection.
Code: Select all

nano /home/pi/playlist.m3u
Code: Select all

/home/pi/music/faith-no-more/the-real-thing/01-from-out-of-nowhere.ogg
/home/pi/music/faith-no-more/the-real-thing/02-epic.ogg
/home/pi/music/faith-no-more/the-real-thing/03-falling-to-pieces.ogg
Restart the desktop and it should run :-)

Hope this helps!
```
