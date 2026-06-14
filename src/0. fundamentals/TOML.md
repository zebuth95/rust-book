# TOML

**TOML** (Tom's Obvious, Minimal Language) is a config format used by Cargo (`Cargo.toml`). Simple, readable.

## Syntax

```toml
[package]
name = "my_crate"
version = "0.1.0"
edition = "2021"

[dependencies]
rand = "0.8"
```

## Parsing TOML with Rust

```rust
use serde::Deserialize;

#[derive(Deserialize)]
struct Config {
    name: String,
    version: String,
}

fn main() {
    let toml_str = r#"
        name = "demo"
        version = "1.0.0"
    "#;

    let cfg: Config = toml::from_str(toml_str).unwrap();
    println!("{} v{}", cfg.name, cfg.version);
}
```

> **Note:** Use `serde` + `toml` crate to parse TOML into Rust structs.
