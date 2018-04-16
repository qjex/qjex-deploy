build:
	docker build -t qjex/santabot .
run:
	-docker rm -f santa
	docker run -d --name santa --link mongodb:mongo qjex/santabot
.PHONY: build run