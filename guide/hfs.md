# A guide for how to transfer your m3u8 playlists through HFS (HTTP File System) through your local network
1. Download HFS [Here](https://www.rejetto.com/hfs/download)  
## NOTE: Antivirus (False Positive)
[VirusTotal Result](https://www.virustotal.com/gui/file/e678899d7ea9702184167b56655f91a69f8a0bdc9df65612762252c053c2cd7c/detection)  
     - This is a false-positive. Please add hfs.exe to the exclusion list.

# Starting the app and use it
0. Double-click "HFS".  
1. Right click on "Virtual File System" > "Add Folder from Disk". ![enter image description here](https://i.ibb.co/dtFtsWB/image.png)
2. Browse for your "Downloads" folder. (Click on your user name > "Downloads" > OK)
3. Browse for the file that you've just edited. (See https://github.com/weareblahs/unifi-playtv-mpd#download-the-m3u8-file-and-modify-the-inputstreamadaptivelicense_key-to-the-widevine-server-url for editing guide)
4. Open Command Prompt. (Shortcut: Windows Key + R > type "cmd" > Run)
5. Type "ipconfig" then press the "Enter" key.
6. If your computer is connected using Wi-Fi, find the line "``Wireless LAN adapter Wi-Fi``" then find the "``  IPv4 Address``" part. Copy the IP address.
7. This is the Tivimate address for the "Enter URL" section (below).
 ``http://(Your copied IP address)/Downloads/unifi.m3u8``
