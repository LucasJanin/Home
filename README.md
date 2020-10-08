# Home
After months of working on different components of my homelab (software and hardware), I decided to share my system.

The brain of the system is a Synology NAS DS918+ with many different Docker containers:

- [Home Assistant](https://registry.hub.docker.com/r/homeassistant/home-assistant) : Home automation connected to my devices
- [Node Red](https://registry.hub.docker.com/r/nodered/node-red/) : Advanced automation with node graph (like Houdini for vfx people :-)
- [Mosquito](https://registry.hub.docker.com/_/eclipse-mosquitto/) : Mqtt server for communication in-between Home Assistant and Zigbee2mqtt
- [Zigbee2mqtt](https://registry.hub.docker.com/r/koenkk/zigbee2mqtt) : Control Zigbee devices (Aqara and Ikea for now)
- [Unifi](https://registry.hub.docker.com/r/jacobalberty/unifi) : Controller for Unifi network gears
- [InfluxDB](https://registry.hub.docker.com/_/influxdb) : Long term storage of Home Assistant data
- [Pi-Hole](https://registry.hub.docker.com/r/pihole/pihole) : DNS filters for blocking advertisings and trackers
- [Grafana](https://registry.hub.docker.com/r/grafana/grafana) : Graphic for display Home Assistant's data
- [Portainer](https://registry.hub.docker.com/r/portainer/portainer) Yes a container for managing containers :-)
- [Watchtower](https://registry.hub.docker.com/r/containrrr/watchtower) : Automatic update of all my docker containers

## Some of my configurations and automations ##

- [Node Red](NodeRed) : Some of my automations
- [Home Assistant](HomeAssistant) : Some tips
- [Watchtower](Watchtower) : My configuration


## Hardware ##
### Homelab ###
- ⁠Rack 15U
- Internet via cable Videotron 400Mb / 50Mb
- DS918+ with 4 x 8 Tb Seagate Ironwolf with 2x1Gb Ethernet with ⁠⁠Link Aggregation
- UPS CyberPower 1500va AVR
- UniFi USG
- UniFi USW-PRO-24
- ⁠UniFi UAP AC LR
- Zigbee USB Dongle with USB extension cable for extended range
- Remote Synology DS219j for offsite backup over VPN (Thanks Max)

### IoT ###
- 4 Aqara door and window sensor sensors
- 4 Aqara temperature and humidity sensors
- 4 Aqara water Leak sensors
- 4 Aqara vibration sensors (not all used yet)
- 1 Aqara motion sensor - for testing thanks [Rigann](https://github.com/rigann/)
- 1 Ikea TRADFRI control outlet
- 1 Ikea TRADFRI LED bulb E27
- 1 Ikea TRADFRI ON/OFF switch
- 1 Ecobee 4
- 5 Nanoleaf Aurora
- 3 Vocolink Smart Plug (not yet fully integrated into HA)
- 1 HP ENVY 4520 Printer

### Medias ###
- 1 AppleTV 4k
- 1 Homepod
- 1 Sonos play:5
- 3 Sonos SL  
