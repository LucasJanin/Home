# Node Red Automations #

My simple automation are done in Home Assistant. But when it need to be more complex, I'm using Node Red. This application permet to build a graph very visual, cose to Houdini, the VFX program I'm using for my work.

- [Closet Light](#closet-light)
- [Garden Winter & Spring Prep](#garden-winter--spring-prep)
- [Office Light](#office-light)

## Closet Light ##

On of my first automation was to control the light of my closet with the door sensor (Aqara).
- Door is open -> light go on
	(The intensity and color temperature are control base time of the day and sunrise/sunset)
- Door is close -> light go off 
- Door is open mode than 3 minutes -> light go off 

### Graph ###![Closet Light Graph](closetLight.png)


## Garden Winter & Spring Prep ##

I'm living in Quebec/Canada so Winter are very cold. 
The garden need to be prepare for winter and spring too.

### Winter ###
Winter si trigger is the Celsius temperature go negative the next  5 days (using dark sky integration)
- Watering hose need to be removed (empty and store inside)
- Some plates go inside the house to survive
- Stair rubber are installed

### Spring ###
Sprint is trigger is the temperature din't go negative the last 20 days (using long storage data in InfluxDB)
- Watering hose need to be install
- Some plates go outside
- Stair rubber are removed

![Closet Light Graph](gardenWinterSpringPrep.png)

## Office Light ##
My office light a control by a motion sensor (Aqara) and Home Assistant (HA) Mac App activity sensor
- Motion sensor On -> Turn on the lights
- HA Mac App activity sensor On -> Turn on the lights
- Motion sensor Off and HA Mac App activity sensor Off -> Turn off the lights

