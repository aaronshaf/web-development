## branches

### delete

```
git branch -d clean_up
```

### rebase

* "Don’t rebase branches you have shared with another developer." http://www.jarrodspillers.com/git/2009/08/19/git-merge-vs-git-rebase-avoiding-rebase-hell.html

## log

```
git log -n1
git log --oneline --decorate
```

## config

### Turn color on

```
git config --global color.ui auto
````

## Tips

* commits are like snapshots -- but use deltas
* branches are simply references to deltas
* branch early, branch often

## Clients / GUIs

* gitk
* gitx
* Git Tower
* SourceTree
* GitBox
* GitHub (OSX, Windows)