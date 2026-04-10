# AP Generated Protocol Buffer Code

This repository contains auto-generated Go code from the protocol buffer definitions in the `ap-protos` repository.

## Directory Structure

```
ap-pb/
├── payment/
│   ├── payment.pb.go
│   └── payment_grpc.pb.go
├── order/
│   ├── order.pb.go
│   └── order_grpc.pb.go
├── go.mod
└── README.md
```

## Important

⚠️ **AUTO-GENERATED CODE** - Do not manually edit files in this repository.

All `.pb.go` and `_grpc.pb.go` files are automatically generated from the proto definitions in the `ap-protos` repository.

## Regenerating Code

To regenerate the code after updating proto files:

1. Update proto files in `ap-protos`
2. Run `make generate` in the `ap-protos` repository
3. Commit and push changes to this repository

## Dependencies

- `google.golang.org/protobuf` - Protocol buffer runtime
- `google.golang.org/grpc` - gRPC Go implementation

## Usage

Services import the generated code:

```go
import pb "github.com/yourorg/ap-pb/payment"
```

Example:

```go
client := pb.NewPaymentServiceClient(conn)
resp, err := client.CreatePayment(ctx, &pb.CreatePaymentRequest{
    OrderId: "order-123",
    Amount:  5000,
})
```
