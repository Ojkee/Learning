Repo is just project directory with `.git` directory in it.

New empty repo
```bash
mkdir project-dir
cd project-dir
git init
```

Git stores every [[Commit]] as some kind of object. The path to the commit uses its [[Hashes|hash]] and becomes
```bash
.git/<first two chars of hash>/<the rest of chars>
```
If Linux (or other Unix-like) has too many files in single directory, weird things happen, to prevent that the first two characters make separate directory spreading out the contents, this technique is called **inode busting**.
