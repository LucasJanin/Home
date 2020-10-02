# HomeAutomation
My home automation system

The main system are a Synology NAS DS918+ with many Docker container:

- Home Assistant : Home automation connected to devices (HomeKit, Ecobee, Nanoleaf lights,..)
- Node Red : Advanced automation with node graph (like Houdini fro vfx people :-)
- Mosquito : Mqtt server for connect Home Assistant to Zigbee2mqtt
- Zigbee2mqtt : Control my Zigbee devices (Aqara and Ikea for now)
- Unifi : Controller to my Unifi network gears (router, switch and Access point) use for presence detection
- InfluxDB : Long term storage of my Home Assistant data
- Pi-Hole : DNS filter ad and tracker
- Graphana : Graphic of my ome Assistant data
- Watchtower : Automatic update all my docker containers