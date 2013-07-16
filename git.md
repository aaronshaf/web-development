## commit

```
git commit --amend
```

## push

```
# -u remembers so that next time you can just use git push
git push -u origin master
```

## branches

### delete

```
git branch -d clean_up
```

## rebase

* "Don’t rebase branches you have shared with another developer." http://www.jarrodspillers.com/git/2009/08/19/git-merge-vs-git-rebase-avoiding-rebase-hell.html

```
git rebase master
```

```
# Interactive rebase of last two commits
git rebase -i HEAD~2
```

## cherry-pick

## log, show, status

```
git status
git show
git log -n1
git log --oneline --decorate
```

## config

### Turn color on

```
git config --global color.ui auto
````

## Gerrit-specific

```
git push origin HEAD:refs/for/master
git push origin <local branchname>:refs/for/<remote branchname>
git push origin <local>:refs/draft/master
git push origin <local>:refs/publish/master
```

## Tips

* Commits are like snapshots -- but use deltas
* Branches are simply references to deltas
* Branch early, branch often
* Know the difference between rebase, reset, and revert

## Clients / GUIs

* gitk
* gitx
* Git Tower
* SourceTree
* GitBox
* GitHub (OSX, Windows)