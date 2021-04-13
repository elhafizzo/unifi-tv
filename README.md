![Cover Image](https://i.ibb.co/PmYn5c5/image.png)

# What's this?
This is a m3u8 playlist file for Unifi playTV / Unifi TV. These links don't use normal HLS / MPEG-TS Livestreams, instead, using encrypted ones (MPEG-DASH). Remember, this guide is not used to bypass DRM and doesn't provide Free Links - you need your own unifi TV subscription.  
  
Note that this is also another way to watch Unifi TV through TiviMate through Telekom Malaysia's official servers. It is not required to install the official Unifi TV app.

# Tested on what device / app?
Works well on Tivimate v2.8.0 and TVirl (Xiaomi Mi Box S).
## What Internet Connection?
Tested on Unifi Air. It will play on multiple resolutions according to the Internet speed (ranging from 576p to 1080p). Unifi Fibre Broadband might get better speeds when playing.

# Do you have some of the screenshots for these channels?
[Screenshots from TiviMate (Channels with subtitles)](https://github.com/weareblahs/unifi-tv/blob/main/screenshots/tivimate.md)  
[Screenshots from generic MPD player](https://github.com/weareblahs/unifi-tv/blob/main/screenshots/mpd.md)

# Other special stuffs?
Multiple Audio (if any, mostly Malay / Chinese / English / Other Languages), Subtitles (Mostly Malay / Chinese), Adaptive Resolution (automatic resolution switching according to your Internet connection).

# Known Technical Specs?
128Kbps AAC Audio, H264 Video (Bitrate depends on resolution), Maximum Resolution is 1920x1080.

# Is there cons?
Unable to record, DRM-protected Streams (Widevine / PlayReady), Not HTTPS, no timeshift although the link is capable of timeshifting.

# Recommended Players
Tivimate, TVirl

# Other players that can play this playlist
PVR Live, Kodi (with InputStream Adaptive enabled), [Native MPEG-DASH / HLS Player](https://chrome.google.com/webstore/detail/native-mpeg-dash-+-hls-pl/cjfbmleiaobegagekpmlhmaadepdeedn?hl=en) (You have to insert your Widevine license URL when requested)

# Known players that can't play this playlist
Kodi without InputStream Adaptive installed and enabled), VLC, IPTV Smarters, CosmiDVR (Signal Weak = 403 Access Denied error), Ultimate IPTV Playlist Loader, OTT Navigator, Startup Show, Media Player Classic Home Cinema

# Information
Please note that these links can be only accessed through a Widevine Server (for authorizing). Instructions below.

# And now, the ultimate guide for this particular playlist
## Get Widevine Server URL
1. Go to [this page](https://playtv.unifi.com.my/EPG/WEBTV/index.html#/live-tv/guide).
2. Sign in with your Facebook account / Sign up for unifi playTV through Facebook / phone number / email address.
3. After signing in, follow these steps:
      - Right Click > Inspect Element.
      - Click "Application" > Session Storage > https://playtv.unifi.com.my.
      - Click "wideVine.license.server.url" then copy the url that starts with "https://ottweb.hypp.tv:8064?deviceId=". Make sure to copy in full.
4. That's it, you have the Widevine URL. Let's get into the next step.

## Download the m3u8 file and modify the inputstream.adaptive.license_key to the Widevine Server URL
1. Download "unifi.m3u8" by [clicking here](https://github.com/weareblahs/unifi-tv/raw/main/unifi.m3u8).
      - Using wget? then copy the command: ```wget https://github.com/weareblahs/unifi-tv/raw/main/unifi.m3u8```
      - Or you're using aria2c? then copy the command: ```aria2c https://github.com/weareblahs/unifi-tv/raw/main/unifi.m3u8```
      - Directly opening this playlist in notepad? Follow these steps: ```Open Notepad > Ctrl + O > Paste "https://github.com/weareblahs/unifi-tv/raw/main/unifi.m3u8" into the File Name section > Open```
3. Open it with Notepad. (SHORTCUT: Windows key + R > notepad > Enter)
4. In notepad, press "Ctrl + H" (Replace).
      - In "Find What", type in "WIDEVINE_SERVER_URL_HERE".
      - In "Replace With", paste the Widevine Server URL in full and remove the quotes.
5. Save it. Now you have a m3u8 file ready to import.

## Importing into compatible IPTV players
### Before we start the importing
NOTE: This playlist only supports TiviMate, PVR Live and TVirl.
1. Upload the file to Dropbox / Github / Any file hosting service that support direct link
     - You can also use HFS. I'm using HFS for m3u8 Transfer through local network. [See the guide by clicking here](https://github.com/weareblahs/unifi-tv/blob/main/guide/hfs.md)
     - Offline options: Use File Commander to transfer the playlist to your TV / TV Box
### Uploading your playlist into Dropbox for Tivimate Access
1. Sign in into Dropbox
2. Upload the saved m3u8 file to your Dropbox.
3. Hover on the file name in Dropbox, click Share, then click Create from "Create then Copy Link".
4.  Click on "Copy Link". (the Dropbox link will be copied in your clipboard)
5. Open any text editor, paste it, then change "dl=0" into "dl=1" (at the end of the link).
     -  (Note that you have to memorize this link OR copy this link to your TV at the next step)
6. Done!
### Importing your playlist into Tivimate
1. After opening the app, select "Add Playlist".
2. Select "Enter URL", then type in the link that you've generated.
3. Select "Next".
4. Follow the steps.
    - When asked for XMLTV URL, type / paste "https://weareblahs.github.io/epg/unifitv.xml".
6. You're ready to watch!

# EPG?
EPG Link for partial channels: https://weareblahs.github.io/epg/unifitv.xml  
  Generated through Webgrab+Plus.
