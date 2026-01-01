---
title: "Git"
date: 2026-1-1
description: "Git"
tags: ["git"]
---

use [conventional commits](https://www.conventionalcommits.org/en/v1.0.0/) for
commit messages.

```shell
git describe
git push --force-with-lease origin <branch>
```

## rebase with latest change(s) from `main`

```shell
git checkout <branch>
git fetch origin # ensure local refs are up to date
git fetch origin main
git rebase origin/main
```

if encountered conflicts:

```shell
git add <file(s)-with-conflicts-resolved>
git rebase --continue
```

then after successful rebase:

```shell
git push --force-with-lease origin <branch>
```

## cleaning commit history

```shell
git rebase -i HEAD~N  # N is number of commits to go back
git rebase -i <commit-hash>^  # commit-hash is the hash of the commit before the first one you want to edit
```

- the `^` is important to include if you want to edit starting from a specific commit
- in the interactive rebase editor, change `pick` to `squash` (or `s`) for
  commits you want to combine into the previous commit
- the different options

if things go wrong during rebase:

```shell
git rebase --abort
```
