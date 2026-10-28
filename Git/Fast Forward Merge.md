If the target [[Branch|branch]] (e.g. main) has no new [[Commit|commits]] since the other branch was created, the target is a direct ancestor of the other branch. In that case Git doesn’t create a merge commit. It just moves the target branch pointer forward to the other branch’s latest commit. This is called a fast-forward merge.

```
Before:  A---B  (main)
             \
              C---D  (feature)

After:     A---B---C---D  (main, feature)
```


```bash
❯ git switch main
Switched to branch 'main'

❯ git --no-pager log --oneline
6e27cb6 (HEAD -> main) F: Merge branch 'add_classics'
5dbf0b9 E: filled the contents.md
a7fe6b1 (add_classics) D: added classics csv
0ef1c9e C: add quotes
9afb07f B: add titles
1a35221 A: add contents.md

❯ git merge update_titles
Updating 6e27cb6..f8b6359
Fast-forward # <--- HERE 
 titles.md | 1 +
 1 file changed, 1 insertion(+)
```

```bash
* f8b6359 6e27cb6 (HEAD -> main, update_titles) G: updated titles.md with one title # Notice, that there is no split
*   6e27cb6 5dbf0b9 a7fe6b1 F: Merge branch 'add_classics'
|\
| * a7fe6b1 0ef1c9e (add_classics) D: added classics csv
* | 5dbf0b9 0ef1c9e E: filled the contents.md
|/
* 0ef1c9e 9afb07f C: add quotes
* 9afb07f 1a35221 B: add titles
* 1a35221 A: add contents.md
```