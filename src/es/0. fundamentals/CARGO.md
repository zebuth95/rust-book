```
# Cargo

**Cargo** es el sistema de compilación y gestor de paquetes de Rust.

## Comandos comunes

| Comando | Qué hace |
|---|---|
| `cargo new my_project` | Crear un nuevo proyecto |
| `cargo build` | Compilar (debug) |
| `cargo run` | Compilar + ejecutar |
| `cargo test` | Ejecutar pruebas |
| `cargo check` | Verificar código sin generar binario (rápido) |
| `cargo fmt` | Formatear código |
| `cargo clippy` | Lint (encontrar errores comunes) |
| `cargo doc --open` | Generar y abrir documentación |
| `cargo add` | Agregar dependencias |
| `cargo remove` | Eliminar dependencias |
| `cargo tree` | Mostrar árbol de dependencias |
| `cargo update` | Actualizar dependencias en Cargo.lock |
| `cargo build --release` | Compilar con optimizaciones |

```toml
# Cargo.toml — project manifest
[package]
name = "my_project"
version = "0.1.0"
edition = "2024"

[dependencies]
serde = { version = "1.0", features = ["derive"] }
```

> **Nota:** Cargo obtiene crates de [crates.io](https://crates.io), el registro oficial.
```
