GOPATH ?= $(PWD)/godir

all: tir

tir: tir.go
	GOPATH="$(GOPATH)" go get -d .
	GOPATH="$(GOPATH)" go build -o $@ tir.go

clean:
	rm -rf tir godir
