# Watchtower #

This docker permit to automatically update all my docker containers.
By default is done every 5 minutes. This created more than 10000 DNS requests per day. Thanks, Pi-Hole to flag me the requests (domains used registry-1.docker.io and auth.docker.io).

The 5 minutes was definitely overkilling for my usage. I decided to do the process only every 6 hours (argument --interval 21600).

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

