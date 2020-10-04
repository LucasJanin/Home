# Node-Red Automations #

All my simples automation are done in Home Assistant. But when it needs to be more complex, I'm using Node-Red. 
This application permits to build a graph very visual, close to Houdini, the VFX program I'm using for my work.

I decided to share my code to give some ideas or for maybe help some users

- [Low Batteries Sensors Notification](#low-batteries-sensors-notification)
- [Office Light](#office-light)
- [Closet Light](#closet-light)
- [Garden Winter & Spring Prep](#garden-winter--spring-prep)

## Low Batteries Sensors Notification ##
This automation checks every day the level of the sensor battery. If the percentage is below 20%, Node-Red will send a notification. 
These 6 nodes permit to avoid creating one automation for each sensor.

The code: ![[Low Batteries Sensors Notification Json](LowBatteriesSensorsNotification.json)

![[Low Batteries Sensors Notification Graph](LowBatteriesSensorsNotification.png)

## Office Light ##
My office lights are control by a motion sensor (Aqara) and Home Assistant (HA) Mac App activity sensor. 
In the case of usage of my webcam (Zoom, Skype,..), my Aurora light is less saturated color. When the webcam finishes being used, the Aurora light is back to saturated.
- [x] Motion sensor On -> Turn on the lights
- [x] HA Mac App activity sensor On -> Turn on the lights
- [x] Motion sensor Off and HA Mac App activity sensor Off for 20 seconds -> Turn off the lights
- [x] Add an input boolean for turn off automation from HA, Homekit and Siri
- [ ] Control an On-Air light outside of the office base mic usage on the computer

Insert in the configuration.yaml
```yml
input_boolean:
   office_automation:
      name: Office Automation
      icon: mdi:home-automation
      initial: true
```

The code: ![Office Light Json](officeLight.json)

![Office Light Graph](officeLight.png)


## Closet Light ##

One of my first automation was to control the light of my closet with the door sensor (Aqara).
- [x] Door is open -> light go on
	(The intensity and color temperature are control base time of the day and sunrise/sunset)
- [x] Door is close -> light go off 
- [x] Door is open mode than 3 minutes -> light go off
- [x] Add an input boolean for turn off automation from HA, Homekit and Siri
- [ ] Control light intensity form a luminosity sensor in the bedroom

Insert in the configuration.yaml
```yml
input_boolean:
   closet_automation:
      name: Closet Automation
      icon: mdi:home-automation
      initial: true
```

The code: ![Closet Light Json](closetLight.json)

![Closet Light Graph](closetLight.png)


## Garden Winter & Spring Prep ##

Yes  Winter is coming! :-). 
I'm living in Quebec/Canada so winters are very cold. 
The garden needs to be prepared for winter and spring too.

### Winter ###
Winter is trigger if the Celsius temperature go negative the next  5 days (using dark sky integration)
- Watering hose needs to be removed (empty and store inside)
- Some plates go inside the house to survive
- Stair-rubbers are installed

### Spring ###
Sprint is triggered if the temperature didn't go negative the last 20 days (using long storage data in InfluxDB)
- Watering hose need to be install
- Some plates go outside
- Stair-rubbers are removed

Insert in the configuration.yaml
```yml
input_boolean:
   summer:
      name: Summer
      icon: mdi:white-balance-sunny
```

The code: ![Garden Winter & Spring Prep Json](gardenWinterSpringPrep.json)

![Garden Winter & Spring Prep Graph](gardenWinterSpringPrep.png)
