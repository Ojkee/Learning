Git Reset command undo the last [[Commit]](s) or any changes in [[Index]].

```bash
❯ echo "* The Internship" > titles.md

❯ git add .

❯ git commit -m 'J: Internship'
[update_dune a102ea3] J: Internship
 1 file changed, 1 insertion(+), 8 deletions(-)
```
The whole file was changed and then the change was commited.

```bash
* a102ea3 (HEAD -> update_dune) J: Internship # <- commit with mistake
* 6f09762 I: dune update - mind-killer quote
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

### --soft
```bash
❯ git reset --soft HEAD~1
# or
❯ git reset --soft <HASH> # We would use I's hash
```
`--soft` makes that, you go back to a previous commit, but you keep all of your changes. Changes will be staged instead of commited.

`HEAD` is the commit we are pointing to, `~1` is the number of steps we want to go back.

It resulted in (Undo the changes while maintaining the changes)
```bash
❯ git status
On branch update_dune
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	modified:   titles.md
```


### --hard
```bash
❯ git reset --hard
HEAD is now at 6f09762 I: dune update - mind-killer quote
```
`--hard` undo index and working tree (tracked changes).

```bash
❯ git status
On branch update_dune
nothing to commit, working tree clean
```

You can also use `--hard` to reset changes until specific commit
```bash
git commit --hard <HASH>
```
All of the changes made after are lost.



