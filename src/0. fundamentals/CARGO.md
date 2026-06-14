# Cargo

**Cargo** is Rust's build system and package manager.

## Common Commands

| Command | What it does |
|---|---|
| `cargo new my_project` | Create new project |
| `cargo build` | Compile (debug) |
| `cargo run` | Compile + run |
| `cargo test` | Run tests |
| `cargo check` | Check code without producing binary (fast) |
| `cargo fmt` | Format code |
| `cargo clippy` | Lint (find common mistakes) |
| `cargo doc --open` | Generate and open docs |
| `cargo add some_crate` | Add a dependency |
| `cargo build --release` | Compile with optimizations |

```toml
# Cargo.toml — project manifest
[package]
name = "my_project"
version = "0.1.0"
edition = "2021"

[dependencies]
serde = { version = "1.0", features = ["derive"] }
```

> **Note:** Cargo fetches crates from [crates.io](https://crates.io), the official registry.
