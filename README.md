# Git

## Check Git configuration:

```bash
git config -l
```

## Setup Git configuration:

```bash
git config --global user.name "Foyez"
git config --global user.email "foyezar@gmail.com"
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
