```toc
min_depth: 1
```

# Git Basics

## Set up username and email:
```
git config --global user.name "Username"
git config --global user.email "user@mail.com"
```

## Create a new repository

```
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin git@github.com:DavidLegarre/test.git
git push -u origin main
```

## Push an existing repository to origin

```
git remote add origin git@github.com:DavidLegarre/test.git
git branch -M main
git push -u origin main
```

## Git add

```
git add .
git add somefile.txt
```

## Git commit

Make a commit message

```
git commit -m "first commit"
```

Add files at the same time we commit

```
git commit -am "commit message"
```

and we can use 

```
git log
```

to see the history of 

To remove a file from staging
```
git reset .
```

## Problem Solving

### How to resolve ‘fatal: refusing to merge unrelated histories’

Use `--allow-unrelated-histories`