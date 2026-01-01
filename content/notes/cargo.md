---
title: "cargo"
date: 2026-1-1
description: "cargo"
tags: ["cargo", "rust", "package management"]
---

## `build`

```shell
cargo build --release
```

- build in release mode (with optimizations)

## `clippy`, `fmt`

```shell
cargo clippy --all-targets --all-features -- -D warnings
```

- run clippy linter on all targets and features, treating warnings as errors

```shell
cargo fmt --all -- --check
```

- check code formatting without making changes

## `test`

```shell
cargo test --all-features
```

- run tests with all features enabled

## `update`

```shell
cargo update -p <crate-name>
```

- update a specific crate to the latest version allowed by `Cargo.toml`

```shell
cargo update -p <crate-name>:<version>
```

```shell
cargo update -p <crate-name>:<old-version> --precise <new-version>
```

- update a specific crate from `<old-version>` to `<new-version>`

```shell
cargo tree --all-features
```

- display the dependency tree with all features enabled

```shell
cargo install cargo-expand
cargo expand
```

- install `cargo-expand` to view expanded macros
- then run `cargo expand` in your project directory to see the expanded code

## `new`

```shell
cargo new --bin <project-name>
cargo new --lib <project-name>
```

- create a new binary or library project with the specified name

## `publish`

```shell
cargo publish --dry-run
```

- simulate publishing the crate to crates.io without actually uploading it

## `generate`

```shell
cargo generate --git <template-repo-url> --name <project-name>
```
