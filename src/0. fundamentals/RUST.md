# Rust

**Rust** is a compiled language focused on **safety**, **speed**, and **concurrency**. No garbage collector — memory is managed via ownership.

## Key Concepts
- **Ownership** — each value has one owner. Memory freed automatically when owner goes out of scope.
- **Borrowing** — references (`&T`) let you read without owning. `&mut T` lets you mutate exclusively.
- **Lifetimes** — the compiler ensures references never outlive the data they point to.
- **Zero-cost abstractions** — high-level code compiles down to efficient machine code.
- **Pattern matching** — exhaustive, safe handling of enums and options.
- **Strong, static typing** with type inference (`let x = 5` infers `i32`).

```rust
fn main() {
    let x = 42;               // i32 inferred
    let y: f64 = 3.14;        // explicit type
    println!("x = {x}, y = {y}");
}
```

## Use Cases
Systems programming, CLI tools, web servers (via async), WebAssembly, embedded, blockchain.

> **Note:** Rust prevents data races, null pointers, and dangling references at compile time.
