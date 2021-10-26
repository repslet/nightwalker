# A Dark but not black qBittorrent WebUI 
**_A darker theme for qBittorrent WebUI_ (made with the help of the Walkerservers community)**

![preview][preview]

# Features
- It's dark, but not black
- It has different colors for ratio-values (see screenshot)
- It has a mix of Fontawesome and custom icons

# Installation

### Clone this repo (Windows)
1. Clone or download this repo as a .ZIP
2. Move it somewhere where qBittorrent can find it.
3. Ensure you use a trailing slash.

### Clone this repo (Linux)
1. `sudo git clone https://github.com/brettpetch/nightwalker.git /opt/nightwalker`
3. `sudo chown -R nobody:nogroup /opt/nightwalker/`

### Activate Alterative WebUI in qBittorrent
1. Under `Tools->Preferences->WebUI` enable `Use alternative WebUI`.
2. Choose a location that points to the `nightwalker` folder, i.e. `/opt/nightwalker/`
3. Restart qBittorrent or refresh your browser for changes to take effect.

You can also change these settings via the config file. The relevant entries are:

- `WebUI\AlternativeUIEnabled=true`
- `WebUI\RootFolder=/opt/nightwalker/`

### Update theme (Linux)
1. `git -C /opt/nightwalker checkout main`
2. `git -C /opt/nightwalker fetch origin main`
3. `git -C /opt/nightwalker reset --hard origin/main`
4. `sudo chown -R nobody:nogroup /opt/nightwalker`

### Tested
Based on the standard qBittorrent WebUI theme (4.3.8 release).
Tested in Updated to 4.3.8

#### A note for those who used the [Theme Park][theme.park] nginx mod
Modify your nginx config and remove the lines that introduced the external css, anything after `rewrite ^/qbittorrent/(.*) /$1 break; ` (non inclusive) is something that can be removed. Do not leave -modded, or any other files that are not necessary for nginx to function in the `/etc/nginx/apps/` directory. Reload nginx after making changes by doing `sudo service nginx configtest`, if it returns OK, then proceed and do `sudo service nginx reload`. 

# Credits
* The Walkerservers (Discord) community
* glibN for the inspiration to use the Fontawesome pack
* Fontawesome for their great fonts
* qBittorrent for the base files

[preview]: preview.png
[qbittorrentsource]: https://github.com/qbittorrent/qBittorrent/tree/master/src/webui/www1\
[theme.park]: https://github.com/gilbN/theme.park/wiki/qBittorrent
