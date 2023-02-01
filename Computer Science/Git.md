```toc
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

## Problem Solving

### How to resolve ‘fatal: refusing to merge unrelated histories’

Use `--allow-unrelated-histories`