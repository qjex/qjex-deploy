run:
	-docker rm -f mongodb
	docker run -d --name mongodb -v /srv/db:/data/db \
	-p 0.0.0.0:27017:27017 mongo --storageEngine wiredTiger --auth --bind_ip 0.0.0.0
reload:
	docker restart mongodb

.PHONY: build run reload help

