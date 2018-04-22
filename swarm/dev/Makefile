.PHONY: build cluster test

default: build

build:
	go build -o bin/swarm    github.com/decrx/go-decrx/cmd/swarm
	go build -o bin/decrx     github.com/decrx/go-decrx/cmd/decrx
	go build -o bin/bootnode github.com/decrx/go-decrx/cmd/bootnode

cluster: build
	scripts/boot-cluster.sh

test:
	go test -v github.com/decrx/go-decrx/swarm/...
