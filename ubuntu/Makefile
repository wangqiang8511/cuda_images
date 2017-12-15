REPO=wangqiang8511/cuda
VERSION=9.0

all: build_base build_runtime build_devel push

build_base:
	docker build -t $(REPO):$(VERSION)-ubuntu-base base

build_runtime:
	docker build --build-arg repository=$(REPO) --build-arg version=$(VERSION) -t $(REPO):$(VERSION)-ubuntu-runtime runtime

build_devel:
	docker build --build-arg repository=$(REPO) --build-arg version=$(VERSION) -t $(REPO):$(VERSION)-ubuntu-devel devel

push:
	docker push $(REPO):$(VERSION)-ubuntu-base
	docker push $(REPO):$(VERSION)-ubuntu-runtime
	docker push $(REPO):$(VERSION)-ubuntu-devel
