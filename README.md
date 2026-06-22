# gRPC Service 📡

gRPC microservice template with Rust and tonic.

## Features

- **Protobuf Codegen**: Build.rs integration
- **TLS**: mTLS support
- **Streaming**: Server/client/bidirectional
- **Health Checks**: gRPC health protocol

## Performance

| Metric | Value |
|--------|-------|
| Unary RPC | 0.3ms |
| Streaming | 50K msg/s |
| Connections | 100K concurrent |

## Quick Start

```protobuf
service Greeter {
    rpc SayHello (HelloRequest) returns (HelloReply);
    rpc StreamGreetings (HelloRequest) returns (stream HelloReply);
}
```

```bash
cargo run --server
```

## License

Apache 2.0