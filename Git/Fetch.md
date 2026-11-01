Brings is all the changes.

```bash
❯ git fetch
remote: Enumerating objects: 30, done.
remote: Counting objects: 100% (30/30), done.
remote: Compressing objects: 100% (28/28), done.
remote: Total 30 (delta 9), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (30/30), 2.96 KiB | 2.96 MiB/s, done.
From ../WebFlyx
 * [new branch]      main        -> origin/main
 * [new branch]      update_dune -> origin/update_dune
```

We have all the changes, but they are not integrated yet
```bash
❯ git log
fatal: your current branch 'master' does not have any commits yet

❯ ll
total 0
```

We can log the [[Commit]]s that way
```bash
❯ git --no-pager log origin/main --oneline
f8b6359 (origin/main) G: updated titles.md with one title
6e27cb6 F: Merge branch 'add_classics'
5dbf0b9 E: filled the contents.md
a7fe6b1 D: added classics csv
0ef1c9e C: add quotes
9afb07f B: add titles
1a35221 A: add contents.md
```
