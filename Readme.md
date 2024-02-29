# GBD Data Repository

This repository contains the metadatabases used in GBD.
The sqlite3 files are stored as SQL dumps for Git diff to work.
Before cloning this repository, you must have sqlite3 installed and define the `dumpsql` clean and smudge filters by running the following commands:
```
git config --global filter.dumpsql.clean 'tmp=$(mktemp); cat > $tmp; sqlite3 $tmp .dump; rm $tmp'
git config --global filter.dumpsql.smudge 'tmp=$(mktemp); sqlite3 $tmp; cat $tmp; rm $tmp'
```
