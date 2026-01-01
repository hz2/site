---
title: "blob"
date: 2026-1-1
description: "blob"
tags: ["blob"]
---

```shell
tree -d -L 2 -I 'target'
```

- to only show 2 levels of directories and ignore `target` directories

```shell
rg "<pattern> -g "*.{toml,rs}""
```

- to search for `<pattern>` only in files with extensions `.toml` and `.rs`

```shell
markdownlint-cli --fix "**/*.md"
```

- to lint and fix all markdown files recursively

```shell
sed 's/\x1B\[[0-9;]*[a-Za-z]//g' <file-with-ansi-codes> > <output-file>
```

- to remove ANSI color codes from a file
- note the `>` to redirect output to a new file

```shell
ssh -L <local-port>:<localhost>:<remote-port> <user>@<remote-host>
```

- to create an SSH tunnel forwarding `<local-port>` on your machine to
  `<remote-port>` on the remote host

<!-- TODO(hz2) -->