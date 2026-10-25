File in Git repo can be in different states, for example:
#### untracked 
Git doesn't know anything about this file, never been added to [[Index]], never been tracked. If you delete that file, you lose every bit of its content.
#### staged
Git will consider those files in commit.
#### committed
Snapshot of repository (staged files).

To find out about status:
```bash
git status
```

