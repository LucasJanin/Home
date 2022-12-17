# Watchtower #

This docker permit to automatically update all my docker containers.
By default is done every 5 minutes. This created more than 10000 DNS requests per day. 
Thanks, Pi-Hole to flag me the requests (domains used registry-1.docker.io and auth.docker.io).

The 5 minutes was definitely overkilling for my usage. 
I decided to do the process only every day at 7 PM.

Recenlty, I added the notofication using ntfy.sh. 
It's very nice to be aware about all the update.

There is my slack for launch the docker in Portainer:

```
version: '2.1'
services:
    watchtower:
        image: containrrr/watchtower
        container_name: watchtower
        volumes:
            - /var/run/docker.sock:/var/run/docker.sock
        environment:
            - TZ=America/Montreal
            - WATCHTOWER_CLEANUP=true
            - WATCHTOWER_SCHEDULE= 0 0 19 * * *
            - WATCHTOWER_NOTIFICATIONS=shoutrrr
            - WATCHTOWER_NOTIFICATION_URL=generic+https://ntfy.sh/YOURTOPIC?title=WatchtowerUpdates
        restart: unless-stopped

```

