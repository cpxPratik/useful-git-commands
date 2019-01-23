# useful-git-commands

## Delete remote branch then delete local branch

```sh
git push origin --delete <branch_name>
git branch -d <branch_name>
```

## Clean-up old remote git branches. IOW, prune tracking branches not on the remote

```sh
git fetch origin --prune
git fetch origin --prune --dry-run # dry run the command
or
git remote prune origin
```

## List git branches variations

```sh
git branch -r
git branch -a
git remote show origin
git ls-remote --heads origin
```

## Remove cached tracking of files on git

```sh
git rm -r --cached .
```

## Checking out remote branch `test` in local

```sh
git fetch origin
git branch -v -a
git checkout -b test origin/test
```

## Reset previous commit without staging into the working directory

```sh
git reset HEAD^
```

## Reset previous commit with staging

```sh
git reset --soft HEAD^
```

## Reset to origin/master with staging

```sh
git reset --soft origin/master
```


## Remove git tracked file which is now gitignored

source: <https://stackoverflow.com/a/19095988/2137210>

```sh
git rm --cached . -r
git add .
git commit -am 'Remove ignored file'
```

## Merge branch with no common commits, IOW, with unrelated histories

source: <https://stackoverflow.com/a/53663271/2137210>

```sh
git pull origin <remote_branch_name> --allow-unrelated-histories
```
