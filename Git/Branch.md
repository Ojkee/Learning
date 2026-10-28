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

