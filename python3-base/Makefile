repo_tag=federicociner

build_dir=latest
image_tag=python3-base:$(build_dir)

full_image_tag=$(repo_tag)/$(image_tag)

buildlocal:
	@echo "Building container"
	sudo docker build $(build_dir) --tag $(full_image_tag)

build:
	sudo docker build $(build_dir)

runlocal:
	@echo "Running container locally"
	sudo docker run --net=host  -it $(full_image_tag) /bin/bash

.PHONY: buildlocal build runlocal

