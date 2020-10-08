# Software

The brain of the system is a Synology NAS DS918+ with 16 Gb of memory. This NAS is running many different Docker containers:

- [Home Assistant](https://registry.hub.docker.com/r/homeassistant/home-assistant) : Home automation connected to my IoT devices
- [Node Red](https://registry.hub.docker.com/r/nodered/node-red/) : Advanced automation with node graph (like Houdini for vfx people :-)
- [Mosquito](https://registry.hub.docker.com/_/eclipse-mosquitto/) : Mqtt server for communication in-between Home Assistant and Zigbee2mqtt
- [Zigbee2mqtt](https://registry.hub.docker.com/r/koenkk/zigbee2mqtt) : Control Zigbee devices (Aqara and Ikea for now)
- [Unifi](https://registry.hub.docker.com/r/jacobalberty/unifi) : Controller for Unifi network gears
- [InfluxDB](https://registry.hub.docker.com/_/influxdb) : Long term storage of Home Assistant data
- [Pi-Hole](https://registry.hub.docker.com/r/pihole/pihole) : DNS filters for blocking advertisings and trackers
- [Grafana](https://registry.hub.docker.com/r/grafana/grafana) : Graphic for display Home Assistant's data
- [Portainer](https://registry.hub.docker.com/r/portainer/portainer) Yes a container for managing containers :-)
- [Watchtower](https://registry.hub.docker.com/r/containrrr/watchtower) : Automatic update of all my docker containers

On my Mac:

- [Atom](https://atom.io) : A fantastic open source editor
- [Home Assistant Mac Companion](https://www.home-assistant.io/blog/2020/09/18/mac-companion/) : Permit to have HA sensors for my Mac. Currently in beta but very stable.
