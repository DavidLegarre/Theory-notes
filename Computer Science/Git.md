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

to see the history of commits 

To remove a file from staging
```
git reset .
```

# Remote

List current remotes in the local repo:

```
git remote
```

Create a new remote:

```
git remote add origin <url>
```

## Git push

To upload stashed changed (`git commit`):

```
git push -u origin master
```

The `-u` flag is used to set 'origin master' as the upstream remote branch so that git pull and git push can be used without arguments in the future.

## Git merge

Fetch and merge code from the remote repository

```
git fetch
git merge origin/master
```

## Git pull

Or we can combine both into a single command:

```
git pull
```

# Git collaboration

## Git branch

List out branches

```
git branch
```

Create a new branch:

```
git branch awesome
```

Delete a branch:

```
git branch -d awesome
```

## Git checkout

Move into a branch

```
git checkout awesome
```

Create a new branch and move into it:

```
git checkout -b awesome
```

# Pull Request

![Pull Request](https://youtu.be/8lGpZkjnkt4)


# Problem Solving

## How merge conflicts happen

Merge conflicts happen when two commits affect the same line of code at the same time:

1. Feature branch modifies line 5 and commits
2. Master branch modifies line 5 and commits
3. Master branch tries to merge the feature branch

```
git branch feature
# make some changes
git commit -am "awesome branch stuff"

git checkout master
# make some changes to the same code
git commit -am "master branch stuff"

git merge feature
#conflict!
```

To explore a merge conflict use git diff to compare the changes in the feature branch and master branch

```
git diff
```

The easiest way to fix the merge conflict is use the editor to choose between the incoming changes (feature) or the existing changes (master). Then create a *new merge* with the changes you want to keep

```
# choose  preferred code on master branch
git commit -am "resolved merge conflict"
```

If you're not sure, you can abort:

```
git merge --abort
```

## How to resolve ‘fatal: refusing to merge unrelated histories’

Use `--allow-unrelated-histories`

