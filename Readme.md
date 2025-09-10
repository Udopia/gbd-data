# GBD Data Repository

This repository contains the databases used by GBD.
For git-diff to work, the sqlite3 databases are stored as SQL dumps.
To check out the sqlite databases, you must first set git-clean and git-smudge filters by running the following commands:
```
git config --global filter.dumpsql.clean 'tmp=$(mktemp); cat > $tmp; sqlite3 $tmp .dump; rm $tmp'
git config --global filter.dumpsql.smudge 'tmp=$(mktemp); sqlite3 $tmp; cat $tmp; rm $tmp'
```
This requires sqlite3 to be installed.
You can also install the dumpsql filter locally by omitting the "--global" option.
