Logging commit history:
```bash
git log --oneline --parents --graph
```
`--oneline` shows commit in single-line format.
`--parents` shows parents of commit.
`--graph` shows graphically how commits were marged.

Shows who made a commit, when the commit was made and what was changed.

```bash
git --no-pager log -n 10
```
`--no-pager` makes, that there is no entire 'second screen'.
`-n 10` shows last 10 commits.

