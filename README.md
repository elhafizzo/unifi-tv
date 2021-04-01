# What's this?
This is a m3u8 playlist file for Unifi playTV / Unifi TV. These links don't use normal HLS / MPEG-TS Livestreams, instead, using encrypted ones (MPEG-DASH). Remember, this guide is not used to bypass DRM and doesn't provide Free Links - you need your own account.

# Tested on what device / app?
Works well on Tivimate v2.8.0 and TVirl (Xiaomi Mi Box S)
## What Internet Connection?
Tested on Unifi Air. It will play on multiple resolutions according to the Internet speed (ranging from 576p to 1080p). Unifi Fibre Broadband might get better speeds when playing.

# Other special stuffs?
Multiple Audio (if any, mostly Malay / Chinese / English / Other Languages), Subtitles (Mostly Malay / Chinese), Adaptive Resolution (automatic resolution switching according to your Internet connection).

# Known Technical Specs?
128Kbps AAC Audio, H264 Video (Bitrate depends on resolution), Maximum Resolution is 1920x1080.

# Is there cons?
Unable to record, DRM-protected Streams (Widevine / PlayReady), Not HTTPS, Subtitles won't work on apps other than Tivimate.

# Information
Please note that these links can be only accessed through a Widevine Server. Instructions on how to get the server URL below.

# Get Widevine Server URL
1. Go to [this page](https://playtv.unifi.com.my/EPG/WEBTV/index.html#/live-tv/guide).
2. Sign in with your Facebook account / Sign up for unifi playTV through Facebook / phone number / email address.
3. After signing in, follow these steps:
      - Right Click > Inspect Element.
      - Click "Application" > Session Storage > https://playtv.unifi.com.my.
      - Click "wideVine.license.server.url" then copy the url that starts with "https://ottweb.hypp.tv:8064?deviceId=". Make sure to copy in full.
4. That's it, you have the Widevine URL. Let's get into the next step.

# Download the m3u8 file
1. Download "unifi.m3u8" from this repository.
2. Open it with Notepad. (SHORTCUT: Windows key + R > notepad > Enter)
3. In notepad, press "Ctrl + H" (Replace).
      - In "Find What", type in "WIDEVINE_SERVER_URL_HERE".
      - In "Replace With", paste the Widevine Server URL in full and remove the quotes.
4. Save it. Now you have a m3u8 file ready to import.

# Importing into compatible IPTV players
## Before we start the importing
NOTE: This playlist only supports TiviMate, PVR Live and TVirl.
1. Upload the file to Dropbox (or Github, BUT you have to set it to private otherwise someone will get your links and make it into a public IPTV playlist and I don't know what to do next if someone finds you and say "why your links can't watch" or something)
## GUIDE: Uploading your playlist into Dropbox for Tivimate Access
1. Sign in into Dropbox
2. Upload the saved m3u8 file to your Dropbox.
3. Hover on the file name in Dropbox, click Share, then click Create from "Create then Copy Link".
4.  Click on "Copy Link". (the Dropbox link will be copied in your clipboard)
5. Open any text editor, paste it, then change "dl=0" into "dl=1" (at the end of the link).
     -  (Note that you have to memorize this link OR copy this link to your TV at the next step)
6. Done!
## GUIDE: Importing your playlist into Tivimate
1. After opening the app, select "Add Playlist".
2. Select "Enter URL", then type in the link that you've generated.
3. Select "Next".
4. Follow the steps.
5. You're ready to watch!
