Everything written in this file (`.gitignore`), is excluded from adding to commit. It can be file, group of files, directories etc.

Ignores for local repo.

`.gitignore`s can be placed in repo root directory, as well as in deeper directories.

`.gitignore` accepts wildcards, which matches by pattern, commonly used:
```
*.txt
!to_incluce.txt
```
`!` negates the pattern, event tho to_include is txt, it won't be ignored.

Patterns starting with `/` are anchored to the root directory.`/main.py` would be ignored only in repo root directory.

Lines that start with `#` are considered comments.