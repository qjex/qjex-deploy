run:
	-docker rm -f gogs
	docker run -d --name gogs -v /srv/gogs:/data \
	-p 127.0.0.1:3000:3000 -p 0.0.0.0:2222:2222 gogs/gogs
reload:
	docker restart gogs

.PHONY: build run reload help

