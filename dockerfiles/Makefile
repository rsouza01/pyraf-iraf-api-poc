.DEFAULT_GOAL := help
.PHONY: all pull

CONTAINER = "iraf-community"
IMAGE = "ghcr.io/rsouza01/iraf-community:0.1"


help:
	@echo 'Available commands:'

pull:
	docker pull $(IMAGE)

run:
	docker run -d --name $(CONTAINER) $(IMAGE) tail -f /dev/null

shell:
	docker exec -it $(CONTAINER) /bin/bash

