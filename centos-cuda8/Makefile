REPO=wangqiang8511/cuda
VERSION=8.0

all: build_base build_runtime build_devel push

build_base:
	docker build -t $(REPO):$(VERSION)-centos-base base

build_runtime:
	docker build --build-arg repository=$(REPO) --build-arg version=$(VERSION) -t $(REPO):$(VERSION)-centos-runtime runtime

build_devel:
	docker build --build-arg repository=$(REPO) --build-arg version=$(VERSION) -t $(REPO):$(VERSION)-centos-devel devel

push:
	docker push $(REPO):$(VERSION)-centos-base
	docker push $(REPO):$(VERSION)-centos-runtime
	docker push $(REPO):$(VERSION)-centos-devel
