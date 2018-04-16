build:
	docker build -t qjex/snake .
run:
	-docker rm -f snake
	docker run -d --name snake -v $(shell pwd)/data:/srv/data \
	-p 0.0.0.0:9760-9770:9760-9770 --restart=always qjex/snake
help:
	@echo "----BUILDING----"
	@echo "Use 'make build' to build a container."
	@echo ""
	@echo "-----RUNNIG-----"
	@echo "Use 'make run' to run a container."
	@echo "Use 'make reload' to restart container."
reload:
	docker restart snake

.PHONY: build run reload help

