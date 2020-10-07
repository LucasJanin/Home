# Open Door Notification #

This automation checks if the outside doors aren't open for too long time. Each door have is own delay base on the difference of outside temperature and average of inside temperatures. This information is stored at the flow level.

The trigger node can't accept variable for delay, so I play with the switch node and many trigger nodes. I'm still thinking the graph doesn't get too messy :-).

- [x] When a door open, the flow calculate the difference of outside temperature (from Dark Sky) and the average of inside temperatures
- [x] Base on this deference, a delay is set for each door with a function. The value of 0 is used for avoiding notification
- [x] Send a notification if the door is open more than the delay
- [x] Don't send a notification if door is closed before the delay

![Open Door Notification iOS](openDoorNotification_ios.jpg)

The code: ![Open Door Notification Json](openDoorNotification.json)

![Open Door Notification Graph](openDoorNotification.png)

Back to [NodeRed](../../README.md)
