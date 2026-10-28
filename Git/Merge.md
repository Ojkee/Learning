After making changes on your [[Branch]], we need to merge our changes into main branch. In that case we create new 'merge commit' that holds the last [[Commit]] of the main and the last commit of the branch as parents and squishes them into one node.

### Before merge
Some changes already could be made on main and the tree looks like this
```bash
* 5dbf0b9 (HEAD -> main) E: filled the contents.md # commit on main
| * a7fe6b1 (add_classics) D: added classics csv   # commit on our branch
|/
* 0ef1c9e C: add quotes # last common commit (base)
* 9afb07f B: add titles
* 1a35221 A: add contents.md
```

### How to merge
```bash
❯ git switch main
Switched to branch 'main'

❯ git merge add_classics # <- branch name
# It will popup the window with commit message, save and quit
Merge made by the 'ort' strategy.
 classics.csv | 6 ++++++
 1 file changed, 6 insertions(+)
 create mode 100644 classics.csv
```

### Result
```bash
#   current VVVVVVV VVVVVVV both parents commits
*   6e27cb6 5dbf0b9 a7fe6b1 (HEAD -> main) F: Merge branch 'add_classics'
|\
| * a7fe6b1 0ef1c9e (add_classics) D: added classics csv
* | 5dbf0b9 0ef1c9e E: filled the contents.md
|/
* 0ef1c9e 9afb07f C: add quotes
* 9afb07f 1a35221 B: add titles
* 1a35221 A: add contents.md
```

### After merging the branch
We no longer need the branch we merged into main, so delete it with
```bash

```

