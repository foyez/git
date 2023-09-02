# Git

## Check Git configuration:

```bash
git config -l
```

## Git configuration:

```bash
# setup user info
git config --global user.name "foyez"
git config --global user.email "foyezar@gmail.com"

# edit global git configuration
git config --global --edit 

# set default branch name of git initialization
git config --global init.defaultBranch <name>
```

## Cache Login credential:

```bash
git config --global credential.helper cache
```

## Initialize git

```bash
git init
```

## Stage files

```bash
git add file_name # add a file
git add * # add all files
git add fil* # add all files starting with 'fil'
```

## Check repository status

```bash
git status
```

## Commit changes

```bash
git commit # commit in editor
git commit -m "your message" # commit with message
git commit -am "your message" # add & commit tracked files
```

## Commit history

```bash
git log # see commit history
git log -p # see commit history including changes
git log --stat # see commit history including line(s) changed and file names
git log --graph --oneline # show log graph of a branch
git log --graph --oneline --all # show log graph of all branches
```

## See changes made before committing

```bash
git diff # all unstaged changes
git diff file_name # unstaged changes of a specific file
git diff --staged
```

## Remove tracked files

```bash
git rm filename
```

## Remove tacked files/directories that was tracked already

```bash
git rm --cached <file>
git rm -r --cached <folder> # for directory
```

## Rename files

```bash
git mv old_file new_file
```

## Revert unstaged changes

```bash
git checkout filename # revert unstaged changes from specified file
git checkout -- . # revert unstaged changes from all files
```

## Revert staged changes

```bash
git reset HEAD filename
git reset HEAD -p # specify the changes you want to reset
```

## Amend the most recent commit

```bash
# should avoid amending pushed commits
git commit --amend # modify and add changes to the most recent commit
git commit --amend -m "your message"
```

## Undo last commit

```bash
git reset HEAD~
or 
git reset HEAD~1
```

## Rollback an old commit

```bash
git revert commit_id
```

## Create & switch branch

```bash
git branch branch_name
git checkout -b branch_name # create a new brach & switch to new created branch
git checkout branch_name
```

## Show branch list

```bash
git branch
```

## Rename a branch

```bash
git branch -M <name>
```

## Delete a branch locally & remotely

Delete a local branch:

```bash
git branch -d <branch_name>
```

Delete a remote branch:

```bash
git push <remote_name> -d <branch_name> # remote_name is normally origin
```

## Switch branch & keep changes

1. switch with creating new branch
```bash
git switch -c "new_branch_name"
```

2. switch without creating new branch
```bash
git stash save
git checkout branch
git stash pop
```

## Merge two branches

```bash
git merge branch_name # merge active branch with branch_name
git merge --abort # abort a conflicting merge
```

## Add a remote repository

```bash
git add remote remote_repo_url
```

## See remote URLs

```bash
git remote -v
git remote show origin # get more info about remote repo
```

## Interact with remote repo

```bash
git push -u origin branch_name # push a new branch to a remote repo
git push # push changes to a remote repo
git push -f # force a push request
git fetch # download the latest changes from a remote repo
git pull # download the latest changes from a remote repo and merge them with local branch
git pull -r # download the latest changes from a remote repo and rebase them with local branch
git branch -r # check remote branches
```

## Resolve a conflict

```bash
git pull -r
# Resolve conflicts which changes you want to add
git add .
git rebase --continue
```

## Git rebase (transfer completed work from one branch to another)

```bash
git rebase branch_name
```
