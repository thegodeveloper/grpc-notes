# gRPC Notes

## Installing protoc plugins

```shell
go install google.golang.org/protobuf/cmd/protoc-gen-go@latest

go install google.golang.org/grpc/cmd/protoc-gen-go-grpc@latest
```

## Generate Protobuf and gRPC code

```shell
protoc --go_out=. --go_opt=module=github.com/thegodeveloper/grpc-notes --go-grpc_out=. --go-grpc_opt=module=github.com/thegodeveloper/grpc-notes proto/account.proto
```