```
# TOML

**TOML** (Tom's Obvious, Minimal Language) es un formato de configuración utilizado por Cargo (`Cargo.toml`). Simple, legible.

## Sintaxis

```toml
[package]
name = "my_crate"
version = "0.1.0"
edition = "2024"

[dependencies]
rand = "0.8"
```

## Parsear TOML con Rust

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

> **Nota:** Usa los crates `serde` + `toml` para parsear TOML en structs de Rust.
```
