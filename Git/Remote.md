Another repo (the 'source of truth' such as github repo is called conventionally 'origin').

```bash
git remote add <name> <uri>
```

```bash
# of our working repo
❯ cd ..

❯ mkdir WebFlyx-local

❯ cd WebFlyx-local

❯ git init
Initialized empty Git repository in /home/ojke/Programming/git-course-boot-dev/WebFlyx-local/.git/

WebFlyx-local git:master
❯ git remote add origin ../WebFlyx
```
Another repo doesn't mean it can't be local.

```bash
WebFlyx-local git:master
❯ ll
total 0
```
Adding remote doesn't mean, that files will spawn automagically, we need to [[Fetch]] them.

