# Watchtower #

This docker permit to automatically update all my docker containers.
By default is done very 5 minutes, I found more than 10000 DNS requests on my PiHole due Watchtower trying to find update on all my containers via domains (registry-1.docker.io and auth.docker.io).

5 minutes was definitely ovr kill ofr my usage. I decided to reduce the process every 6 hours (argument --interval 21600).

```
docker run -d \
	--name watchtower \
	--debug \
	--cleanup \
	--interval 21600 \
	-e TZ="America/Montreal" \
	-v /var/run/docker.sock:/var/run/docker.sock \
	containrrr/watchtower
```

