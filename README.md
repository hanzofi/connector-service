# Hanzo Fi Connector Service

Universal payment connector integration framework. Macro-based Rust architecture for building payment provider adapters.

## Features

- Macro-based connector scaffolding
- Unified request/response types across providers
- Built-in error handling and retries
- Webhook normalization
- Connector health monitoring

## Supported Connectors

Stripe, Adyen, Checkout.com, Braintree, Worldpay, Cybersource, NMI, Authorize.net, Square, PayPal, and more.

## Development

```bash
cargo build
cargo test
cargo clippy
```

## Adding a Connector

```rust
use connector_macros::connector;

#[connector(name = "stripe")]
impl StripeConnector {
    async fn authorize(&self, req: AuthorizeRequest) -> Result<AuthorizeResponse> {
        // Implementation
    }
}
```

## License

Apache 2.0 — see [LICENSE](LICENSE)

