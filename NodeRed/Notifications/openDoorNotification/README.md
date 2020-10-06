# Open Door Notification #

This automation checks if the outside doors are open for too long time. This delay is set per door and depending on the difference of outside temperature and average of inside temperatures. The delay of each door is stored at the flow level.

The trigger node can't accept variable doe delay, so I play with the switch node and many trigger nodes. I'm still thinking the graph doesn't get too messy :-).

- [x] When a door open calculate the  difference of outside temperature (from Dark Sky) and the average of inside temperatures
- [x] Base on this deference, set a delay for each door inside a function. The value of 0 is used for avoiding notification
- [x] Send a notification if the door is open more than the delay
- [x] Don't send a notification is doos is closed before the delay

![Open Door Notification iOS](openDoorNotification_ios.jpg)

The code: ![Open Door Notification Json](openDoorNotification.json)

![Open Door Notification Graph](openDoorNotification.png)

Back to [NodeRed](../../README.md)
