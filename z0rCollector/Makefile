build:
	docker build -t qjex/z0rCollector .
run:
	-docker rm -f z0rCollector
	docker run -d --name z0rCollector -v $(shell pwd)/data:/srv/data \
	I--restart=always qjex/z0rCollector
help:
	@echo "----BUILDING----"
	@echo "Use 'make build' to build a container."
	@echo ""
	@echo "-----RUNNIG-----"
	@echo "Use 'make run' to runn a container."
	@echo "Use 'make reload' to restart container."
reload:
	docker restart z0rCollector

.PHONY: build run reload help

