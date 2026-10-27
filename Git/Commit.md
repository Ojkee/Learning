Commit is just snapshot of repository, done by:
```bash
git commit -m 'comment/message about commit'
```

Git stores the entire history per commit, not just diffs.

It stores unique hash of a tree, but every blob that didn't change is a pointer (same blob hash as in previous commit).


```bash
❯ git --no-pager log --oneline
9afb07f (HEAD -> master) B: add titles # LAST COMMIT 
1a35221 A: add contents.md             # PARENT COMMIT
```

[[cat-file]] of parent commit
```bash
❯ git cat-file -p 1a35221
tree 60613ff4c6b581b7eef3f30f3f1bd2bf2a87a11a # TREE HASH 
author Ojkee <17oju17@gmail.com> 1792949996 +0100
committer Ojkee <17oju17@gmail.com> 1792949996 +0100

A: add contents.md

❯ git cat-file -p 60613ff4c6b581b7eef3f30f3f1bd2bf2a87a11a # CAT-FILE TREE
100644 blob bc3f6dbec0bf0887cd9bc04c9974907388de8863    contents.md # BLOB HASH
```

[[cat-file]] of last commit
```bash
❯ git cat-file -p 9afb07f
tree d7658a3b13493b67f2ddf0410099f5491e35f862 # OTHER TREE HASH
parent 1a35221860ae45d9214bfb4746d3c18c5ff194f1
author Ojkee <17oju17@gmail.com> 1792952942 +0100
committer Ojkee <17oju17@gmail.com> 1792952942 +0100

B: add titles

❯ git cat-file -p d7658a3b13493b67f2ddf0410099f5491e35f862
100644 blob bc3f6dbec0bf0887cd9bc04c9974907388de8863    contents.md # THIS FILE DIDN'T CHANGE SO BLOB HASH IS THE SAME AS IN PARENT COMMIT
100644 blob e2c253ef323e5a8dd97c87dabee6d4a842a61c45    titles.md
```
