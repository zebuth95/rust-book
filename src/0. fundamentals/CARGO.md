# Cargo
Cargo is the build system and package manager for the Rust programming language. It is essential too for managing Rust projects, handling tasks..

- cargo new my_project (for creation)

## Dependency Management
Cargo manages the external libraries (called "crates" in Rust) that a project depends on. It fetches and builds these dependencies from **crates.io**, the official Rust package registry, ensuring that the correct versions are used for repeatable builds.

- cargo add some_crate

## Building Code
Cargo invokes the Rust compiler (rustc) with the appropriate parameters to compile a project's source code, including dependencies.

- cargo build

## Project Initialization and Structure
Cargo provides commands to create new Rust projects with a standardized directory structure, including src for source code, benches for benchmarks, examples for usage examples, and tests for unit and integration tests.

## Running Tests
Cargo can execute the test defined within a project

- cargo test

## Running Executables
Cargo can compile and run executable binaries within a project.

- cargo run

## Generating Documentation 
Cargo can generate documentation for a project based on its source code comments.

- cargo doc
- cargo doc --open
- cargo doc --no-deps (exclude the documentation for its dependencies)
- cargo doc --document-private-items (only generates documentation for public items)

## Code Format

- cargo fmt

## Code lint

- cargo clippy

## Publishing Crates
Cargo facilitates the process of publishing a project's library crate to crates.io, making it available for others to use as a dependency.

### At the core of every Cargo-managed Rust project is the Cargo.toml file. This manifest file defines the project's metadata (name, version, authors), its dependencies, and various build configurations and features.
### In essence, Cargo streamlines the entire development workflow for Rust projects, from setting up a new project to managing dependencies, building, testing, and even publishing, making it an indispensable tool for Rust developers.


