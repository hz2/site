---
title: "Nix"
description: "nix"
tags: ["nix", "linux"]
---

```shell
nix develop
```

```shell
nix develop --comand bash -c "cargo clippy --all-targets --all-features -- -D warnings"
```

- run clippy in nix dev shell

```shell
nix develop -c env RUSTFLAGS="-A warnings" cargo build
```

- ignore warnings

```shell
nix flake check
```

- run checks defined in `flake.nix`

```shell
nix-collect-garbage -d
```

- delete old nix store items
- `-d` deletes all unused items

```shell
nix flake lock --update-input <input-name>
```

- update a specific input in `flake.nix`

## remote builders

```shell
nix build --max-jobs 0 --eval-store auto --system <target-system> --print-out-paths -L
```

<!-- TODO(hz2) -->
