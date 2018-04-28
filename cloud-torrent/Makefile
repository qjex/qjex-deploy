run:
	-docker rm -f cloud-torrent
	docker run -d --name cloud-torrent -v /srv/cloud-torrent:/downloads \
	-p 0.0.0.0:3003:3000 cloud-torrent jpillora/cloud-torrent
reload:
	docker restart cloud-torrent

.PHONY: build run reload help

