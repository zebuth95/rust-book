# Rust

**Rust** es un lenguaje compilado enfocado en **seguridad**, **velocidad** y **concurrencia**. No tiene recolector de basura — la memoria se gestiona mediante ownership.

## Conceptos clave
- **Ownership** — cada valor tiene un dueño. La memoria se libera automáticamente cuando el dueño sale de ámbito.
- **Borrowing** — las referencias (`&T`) permiten leer sin ser dueño. `&mut T` permite mutar de forma exclusiva.
- **Lifetimes** — el compilador asegura que las referencias nunca superen la vida de los datos a los que apuntan.
- **Zero-cost abstractions** — el código de alto nivel se compila a código máquina eficiente.
- **Pattern matching** — manejo exhaustivo y seguro de enums y opciones.
- **Tipado estático y fuerte** con inferencia de tipos (`let x = 5` infiere `i32`).

```rust
fn main() {
    let x = 42;               // i32 inferred
    let y: f64 = 3.14;        // explicit type
    println!("x = {x}, y = {y}");
}
```

## Casos de uso
Programación de sistemas, herramientas CLI, servidores web (vía async), WebAssembly, embebidos, blockchain.

> **Nota:** Rust previene condiciones de carrera, punteros nulos y referencias colgantes en tiempo de compilación.
