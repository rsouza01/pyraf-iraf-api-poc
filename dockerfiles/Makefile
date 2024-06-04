.DEFAULT_GOAL := help
.PHONY: all pull

CONTAINER = "iraf-community"
IMAGE = "ghcr.io/rsouza01/iraf-community"
VERSION = "0.2"


help:
	@echo 'Available commands:'

pull:
	docker pull $(IMAGE):$(VERSION)

run:
	docker run -d --name $(CONTAINER) $(IMAGE):$(VERSION) tail -f /dev/null

shell:
	docker exec -it $(CONTAINER) /bin/bash

