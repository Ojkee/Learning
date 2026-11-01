Brach is a pointer to the [[Commit]], that's why they are cheap. The 'heads' of branches are stored in the `./.git/refs/heads` directory.
![[Pasted image 20261028121024.png]]

### Check current branch
```bash
❯ git --no-pager branch
* master
```

### Rename branch 
```bash
❯ git branch -m master main

❯ git --no-pager branch
* main

```

### Create new
Whenever you create new brach, it takes current location.
```bash
# Create and switches to new branch (use that method)
❯ git switch -c add_classics 
Switched to a new branch 'add_classics'

# Same, but older method
❯ git checkout -b add_classics 
```

### Switching between branches
`checkout` works, but use `switch`.
```bash
❯ git switch main
Switched to branch 'main'

❯ git --no-pager branch
  add_classics * main

❯ git checkout add_classics
Switched to branch 'add_classics'

❯ git --no-pager branch
* add_classics   main
```

### Create and switch branch of given commit
```bash
❯ git --no-pager log --oneline
f8b6359 (HEAD -> main, update_titles) G: updated titles.md with one title
6e27cb6 F: Merge branch 'add_classics'
5dbf0b9 E: filled the contents.md
a7fe6b1 (add_classics) D: added classics csv # We will use that commit
0ef1c9e C: add quotes
9afb07f B: add titles
1a35221 A: add contents.md

						  # VVVVVVV commits hash
❯ git switch -c update_dune a7fe6b1
Switched to a new branch 'update_dune'
```

### After merging the branch
We no longer need the branch we merged into main, so delete it with
```bash
❯ git branch -d add_classics
Deleted branch add_classics (was a7fe6b1).

❯ git branch -D update_titles
Deleted branch update_titles (was f8b6359).
```
`-d` delete
`-D` force delete