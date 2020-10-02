# Node Red Automations #

My simple automation are done in Home Assistant. But when it need to be more complex, I'm using Node Red. This application permet to build a graph very visual, cose to Houdini, the VFX program I'm using for my work.

## Closet Light ##

On of my first automation was to control the light of my closet with the door sensor (Aqara).
- Door is open -> light go on
	(The intensity and color temperature are control base time of the day and sunrise/sunset)
- Door is close -> light go off 
- Door is open mode than 3 minutes -> light go off 

![Closet Light Graph](closetLight.png)