# GBD Data Repository

This repository contains the metadatabases used in GBD.
The sqlite3 files are stored as SQL dumps for Git diff to work.
To use them, you must have sqlite3 installed before checkout and run the following commands:
```
git config filter.dumpsql.clean 'sqlite3 %f .dump'
git config filter.dumpsql.smudge sqlite3
```

Alternatively, you can also add the following lines manually to your Git configuration:
```
[filter "dumpsql"]
	smudge = sqlite3
	clean = sqlite3 %f .dump
```