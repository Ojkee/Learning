Logging commit history:
```bash
git log --oneline --parents --graph -p
```
`--oneline` shows commit in single-line format.
`--parents` shows parents of commit.
`--graph` shows graphically how commits were marged.
`-p` shows the differences

```bash
git log --oneline --graph <branch_1> <branch_2> ... <branch_n>
```
You can specify branches (by names) while graphing.

Shows who made a commit, when the commit was made and what was changed.

```bash
git --no-pager log -n 10
```
`--no-pager` makes, that there is no entire 'second screen'.
`-n 10` shows last 10 commits.

