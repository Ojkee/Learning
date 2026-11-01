Rebase changes the base [[Commit]] of a feature [[Branch]]. Instead of branching off from the old commit, the branch is replayed on top of the latest commit of the target branch (e.g. `main`). The original commits are recreated as new ones with new hashes, so history stays linear without a merge commit ([[Fast Forward Merge]]).

```
Before:  A---B---E  (main)
              \
               C---D  (feature)

After:   A---B---E  (main)
                  \
                   C'---D'  (feature
```

We are on branch that diverged from other (already merged) branch.
```bash
❯ git --no-pager log --oneline --all --graph
* 06d661b (HEAD -> update_dune) I: dune update - mind-killer quote
* e361082 H: dune update - spice must flow quote
| * f8b6359 (update_titles, main) G: updated titles.md with one title
| *   6e27cb6 F: Merge branch 'add_classics'
| |\
| |/
|/|
* | a7fe6b1 D: added classics csv
| * 5dbf0b9 E: filled the contents.md
|/
* 0ef1c9e C: add quotes
* 9afb07f B: add titles
* 1a35221 A: add contents.md
```

```bash
❯ git rebase main
Successfully rebased and updated refs/heads/update_dune.
```

```bash
❯ git --no-pager log --oneline --all --graph
* 6f09762 (HEAD -> update_dune) I: dune update - mind-killer quote
* 47896fe H: dune update - spice must flow quote
* f8b6359 (main) G: updated titles.md with one title
*   6e27cb6 F: Merge branch 'add_classics'
|\
| * a7fe6b1 D: added classics csv
* | 5dbf0b9 E: filled the contents.md
|/
* 0ef1c9e C: add quotes
* 9afb07f B: add titles
* 1a35221 A: add contents.md
```
History became nice and simple.

### DO NOT REBASE MAIN