build:
	docker build -t qjex/redu .
run:
	-docker rm -f redu
	docker run -d --name redu --link mongodb:mongodb qjex/redu
.PHONY: build run
