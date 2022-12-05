# Software

The brain of the system is a Synology NAS DS918+ with 16 Gb of memory. This NAS is running many different Docker containers:

- [Home Assistant](https://registry.hub.docker.com/r/homeassistant/home-assistant) : Home automation connected to my IoT devices
- [Node Red](https://registry.hub.docker.com/r/nodered/node-red/) : Advanced automation with node graph (like Houdini for vfx people :-)
- [Mosquito](https://registry.hub.docker.com/_/eclipse-mosquitto/) : MQTT server for communication in-between Home Assistant and Zigbee2mqtt
- [Unifi](https://registry.hub.docker.com/r/jacobalberty/unifi) : Controller for Unifi network gears
- [InfluxDB](https://registry.hub.docker.com/_/influxdb) : Long term storage of Home Assistant data
- [Pi-Hole](https://registry.hub.docker.com/r/pihole/pihole) : DNS filters for blocking advertisings and trackers
- [Grafana](https://registry.hub.docker.com/r/grafana/grafana) : Graphic for display Home Assistant's data
- [ESPHome](https://esphome.io) : Control ESP8266/ESP32 by simple yet powerful configuration files and control them remotely through Home Automation system
- [Portainer](https://registry.hub.docker.com/r/portainer/portainer) Yes a container for managing containers :-)
- [Watchtower](https://registry.hub.docker.com/r/containrrr/watchtower) : Automatic update of all my docker containers

On my Mac:

- [Atom](https://atom.io) : A fantastic open source editor
- [Home Assistant Mac Companion](https://www.home-assistant.io/blog/2020/09/18/mac-companion/) : Permit to have HA sensors for my Mac. Currently in beta but very stable
- [MQTT Explorer](http://mqtt-explorer.com/) : For investigating MQTT via a human interface

On ESP8266:
- [ESPHome](https://esphome.io) : Control ESP8266/ESP32 by simple yet powerful configuration files and control them remotely through Home Automation system
- [WLED](https://github.com/Aircoookie/WLED) : A fast and feature-rich implementation of an ESP8266/ESP32 webserver to control NeoPixel (WS2812B, WS2811, SK6812) LEDs or also SPI based chipsets like the WS2801 and APA102!
