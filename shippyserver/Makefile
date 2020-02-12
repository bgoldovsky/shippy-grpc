.PHONY:server
server: 
	go run ./cmd/server

.PHONY:client
client: 
	go run ./cmd/client -days 20

.PHONY:docker
docker: 
	sudo docker build -t shippy-app . && sudo docker run -p 8080:8081 -it shippy-app

.PHONY:proto
proto:
	protoc -I api/proto --go_out=plugins=grpc:pkg/api api/proto/shippy.proto

.DEFAULT_GOAL := run