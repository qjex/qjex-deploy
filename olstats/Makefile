build:
	docker build -t qjex/olstats .
run:
	-docker rm -f olstats-web
	docker run -d --name olstats-web --link mongodb:mongodb \
	-p 8081:8081 qjex/olstats
.PHONY: build run
