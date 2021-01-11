# A Dark but not black qBittorrent WebUI 
**_A darker theme for qBittorrent WebUI_ (made with the help of the Walkerservers community)**


# Features
- It's dark, but not black
- It has different colors for ratio-values (see screenshot)
- It has a mix of Fontawesome and custom icons

# Installation

### Clone this repo (Windows)
1. Clone or download this repo as a .ZIP
2. Move it somewhere where qBittorrent can find it.

### Clone this repo (Linux)
1. `cd /opt`
2. `sudo git clone https://github.com/repslet/nightwalker.git`
3. `sudo chmod -R 777 nightwalker`

### Activate Alterative WebUI in qBittorrent
1. Under `Tools->Preferences->WebUI` enable `Use alternative WebUI`.
2. Choose a location that points to the `Nightwalker` folder, i.e. `/opt/nightwalker`
3. Restart qBittorrent or refresh your browser for changes to take effect.

You can also change these settings via the config file. The relevant entries are:

- WebUI\AlternativeUIEnabled=true
- WebUI\RootFolder=/path/to/Nightwalker

### Update theme (Linux)
1. `cd /opt/nightwalker`
2. `git pull`
3. If it won't update try: `git fetch --all && git reset --hard && git pull`

### Tested
Based on the standard qBittorrent WebUI theme (4.3.2 release).
Tested in 4.3.1 and 4.3.2

![preview][preview]
It should look like this

# Credits
* The Walkerservers (Discord) community
* glibN for the inspiration to use the Fontawesome pack
* Fontawesome for their great fonts
* qBittorrent for the base files

[preview]: preview.png
[qbittorrentsource]: https://github.com/qbittorrent/qBittorrent/tree/master/src/webui/www