# gRPC Notes

## Installing protoc plugins

```shell
go install google.golang.org/protobuf/cmd/protoc-gen-go@latest

go install google.golang.org/grpc/cmd/protoc-gen-go-grpc@latest
```

## Generate Protobuf and gRPC code

```shell
protoc --go_out=./golang \
  --go_opt=module=github.com/thegodeveloper/grpc-notes \
  --go-grpc_out=./golang \
  --go-grpc_opt=module=github.com/thegodeveloper/grpc-notes \
  ./proto/account.proto
```

### Generate Protobuf Order

```shell
protoc -I ./proto \
  --go_out ./golang \
  --go_opt paths=source_relative \
  --go-grpc_out ./golang \
  --go-grpc_opt paths=source_relative \
  ./proto/order.proto
```