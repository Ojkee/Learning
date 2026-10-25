Because [[Commit]] is just file, we can print its content
```bash
cat .git/objects/<first two hash chars>/<the rest>
```
It shows garbage, because git compressed entire repository into raw bytes.

Git has build in command to print the file (you can provide just 4 first characters of the hash)
```bash
git cat-file -p <hash>
```

Printing commit shows something like this
```bash
❯ git cat-file -p 1a35221
tree 60613ff4c6b581b7eef3f30f3f1bd2bf2a87a11a
author Ojkee <17oju17@gmail.com> 1792949996 +0100
committer Ojkee <17oju17@gmail.com> 1792949996 +0100

A: add contents.md
```

There is `tree` (directory)
```bash
❯ git cat-file -p 60613ff4c6b581b
100644 blob bc3f6dbec0bf0887cd9bc04c9974907388de8863	contents.md
```

That contains `blob` (file)
```bash
❯ git cat-file -p bc3f6dbec0bf0887cd9bc04c
# Contents
```
Which has just the content of staged file.
