VERSION=latest
PROJECT=jgraham20
IMAGE=armhf_zookeeper

all: build

build:
	docker build --pull -t ${PROJECT}/${IMAGE}:${VERSION} .

push: build
	docker push ${PROJECT}/${IMAGE}:${VERSION}

.PHONY: all build push
