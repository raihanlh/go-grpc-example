## Introduction
Beginner tutorial for creating gRPC server and client using the latest version of protoc-gen-go to date (Dec 28 2021). Created because some tutorials are outdated.

## Install protoc
> go install google.golang.org/protobuf/cmd/protoc-gen-go@v1.26
> go install google.golang.org/grpc/cmd/protoc-gen-go-grpc@v1.1

# Add path to environment variable
> echo 'export GOPATH=$HOME/go' >> $HOME/.bashrc
> source $HOME/.bashrc

> echo 'export PATH=$PATH:$GOPATH/bin' >> $HOME/.bashrc
> source $HOME/.bashrc

## Generate
> protoc --go_out=./chat --go_opt=paths=source_relative --go-grpc_out=./chat --go-grpc_opt=paths=source_relative ./chat.proto

## Run
> go run server/server.go
> go run client/client.go

## Reference
- https://tutorialedge.net/golang/go-grpc-beginners-tutorial/


