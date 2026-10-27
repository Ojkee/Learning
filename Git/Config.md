Its some file that git uses while operating. Only certain keys are used, so you can place there whatever and it will still works. 

There might be several git config files.
![[Pasted image 20261027181259.png]]

# Global
All changes for `--global` lands in `~/.gitconfig` file.
```bash
git config --add --global user.name "Ojkee"
git config --add --global user.email "...@email.com"
git config --add --global init.defaultBranch master"
```

# Local
Local git configuration in `./.git/config` in project repo. Used for project specific configuration.
```bash
git config --add --local weblyx.ceo Ojke
	             ^^^^^^^
git config --add --local weblyx.cto JohnOjke
git config --add --local weblyx.valuation mid
```

# System and Worktree
Almost never used.

### View contents
```bash
❯ git config --list --local
core.repositoryformatversion=0
core.filemode=true
core.bare=false
core.logallrefupdates=true
webflyx.ceo=Ojke
webflyx.cto=JohnOjke
webflyx.valuation=mid
```

or just Linux cat
```bash
❯ cat .git/config
[core]
	repositoryformatversion = 0
	filemode = true
	bare = false
	logallrefupdates = true
[webflyx]       # section
	ceo = Ojke  # key
	cto = JohnOjke
	valuation = mid

# git config --add --local weblyx.ceo Ojke
						# section.key
```

### View certain keys
```bash
❯ git config --get webflyx.ceo
Ojke

# You can ommit --get, it's default operation
❯ git config webflyx.ceo
Ojke
```

### Remove key with `--unset`
```bash
❯ git config --unset webflyx
error: key does not contain a section: webflyx
# You can't unset whole section

❯ git config --unset validation
error: key does not contain a section: validation
# You can't unset key without specifying section first

❯ git config --unset webflyx.cto

❯ git --no-pager config --list --local
core.repositoryformatversion=0
core.filemode=true
core.bare=false
core.logallrefupdates=true
webflyx.ceo=Ojke
# no contains longer cto key here
webflyx.valuation=mid
```

Git doesn't replace keys when you `--add` them, it appends to the end and takes the last one.
```bash
❯ git --no-pager config --list --local
core.repositoryformatversion=0
core.filemode=true
core.bare=false
core.logallrefupdates=true
webflyx.ceo=Ojke
webflyx.valuation=mid
webflyx.ceo=Guy1
webflyx.ceo=Guy2
webflyx.ceo=Guy3

❯ git --no-pager config webflyx.ceo
Guy3
```

To remove all keys use `--unset-all`.
```bash
❯ git config --unset webflyx.ceo
warning: webflyx.ceo has multiple values

❯ git config --unset-all webflyx.ceo
```

### Remove whole section with `--remove-section`
```bash
❯ git config --remove-section webflyx

❯ git --no-pager config --list --local
core.repositoryformatversion=0
core.filemode=true
core.bare=false
core.logallrefupdates=true
```