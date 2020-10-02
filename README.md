# Home
My home network and automation system

The main system are a Synology NAS DS918+ with many Docker container:

- [Home Assistant](https://registry.hub.docker.com/r/homeassistant/home-assistant) : Home automation connected to devices (HomeKit, Ecobee, Nanoleaf lights,..)
- [Node Red](https://registry.hub.docker.com/r/nodered/node-red/) : Advanced automation with node graph (like Houdini for vfx people :-)
- [Mosquito](https://registry.hub.docker.com/_/eclipse-mosquitto/) : Mqtt server for connect Home Assistant to Zigbee2mqtt
- [Zigbee2mqtt](https://registry.hub.docker.com/r/koenkk/zigbee2mqtt/) : Control my Zigbee devices (Aqara and Ikea for now)
- [Unifi](https://registry.hub.docker.com/r/jacobalberty/unifi/) : Controller to my Unifi network gears (router, switch and Access point) use for presence detection
- [InfluxDB](https://registry.hub.docker.com/_/influxdb/) : Long term storage of my Home Assistant data
- [Pi-Hole](https://registry.hub.docker.com/r/pihole/pihole/) : DNS filter ad and tracker
- [Grafana](https://registry.hub.docker.com/r/grafana/grafana/) : Graphic of my Home Assistant data
- [Watchtower](https://registry.hub.docker.com/r/containrrr/watchtower/) : Automatic update all my docker containers

## Some of my configurations and automations ##

- [Node Red](NodeRed) : Some of my automations
- [Watchtower](Watchtower) : My configuration

## Hardware ##
- ⁠Rack 15U
- Internet via cable Videotron 400Mb / 50Mb
- DS918+ with 4 x 8 Tb Seagate Ironwolf with 2x1Gb Ethernet with ⁠⁠Link Aggregation
- UPS CyberPower 1500va AVR
- UniFi USG
- UniFi USW-PRO-24
- ⁠UniFi UAP AC LR
- Zigbee USB Dongle
 
- 4 Aqara door and window sensor sensors
- 4 Aqara temperature and humidity sensors
- 4 Aqara vibration sensors
- 1 Aqara motion sensors - for testing thanks [Rigaan](https://github.com/rigann/))
- 1 Ikea TRADFRI control outlet
- 1 Ikea TRADFRI LED bulb E27
- 1 Ikea TRADFRI ON/OFF switch
- 1 Ecobee 4
- 5 Nanoleaf Aurora
  
  