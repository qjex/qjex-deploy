build:
	docker build -t qjex/wiki .
run:
	-docker rm -f wiki
	docker run -d --name wiki -v /srv/static/www/wiki:/var/www/html \
	--link mysql:mysql -p 0.0.0.0:8888:80 qjex/wiki
help:
	@echo "----BUILDING----"
	@echo "Use 'make build' to build a container."
	@echo ""
	@echo "-----RUNNIG-----"
	@echo "Use 'make run' to run a container. This will link wiki container with mysql container."
	@echo "And wiki will be available at 0.0.0.0:8888"
	@echo "Also /srv/static/www/wiki will be mounted to container."
	@echo "Use 'make reload' to restart container."
reload:
	docker restart wiki

.PHONY: build run reload help
