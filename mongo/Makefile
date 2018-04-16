build:
	docker build -t qjex/mongodb .
run:
	-docker rm -f mongodb
	docker run -d --name mongodb -v /srv/dbs/mongodb:/data/db \
	-p 127.0.0.1:27017:27017 qjex/mongodb
help:
	@echo "----BUILDING----"
	@echo "Use 'make build' to build a container."
	@echo ""
	@echo "-----RUNNIG-----"
	@echo "Use 'make run' to run a container."
	@echo "MongoDB will be available at 127.0.0.1:27017"
	@echo "Use 'make reload' to restart container."
reload:
	docker restart mongodb

.PHONY: build run reload help
