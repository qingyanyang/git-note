# git note

check if git surveillance by checking .git file
```git
ls -a
```
delete this hidden file could remove git surveillance
```git
rm -rf .git
```
create a git local repo
```git
git init my-repo
```
clone from remote repo, git covered by default
```git
git clone <remote repo url>
```
git add from working area to staged area
status from untrack->staged
```git
git add file.text 
git add *.text
git add .
```
discard files in staged area
```git
git rm --cached file.text
```
commit staged files to local repo
```git
git commit -m”” 
```
check commit log
```git
git log
git log --oneline
```
reset commit version
```git
git reset --soft // keep working and staged files
git reset --hard // remove all files from working and staged area
git reset --mixed // only keep working area files
```
check staged files
```git
git ls-files
```
delete staged files
```git
git rm --cached **filename.txt
```
compare diffs
```git
git diff
git diff HEAD
git diff cached
git diff 56476547 7625375
```
remove files in both working and staged area
```git
git rm file.txt
```
only remove file in staged area
```git
git rm --cached file.txt
```
#
in local git repo,  cd .shh
Ssh-keygen -t rsa -b 4096
enter return, to generate ssh key if it is first to config ssh

add remote url to local repo
```git
origin vs upstream
https://blog.csdn.net/weixin_37646636/article/details/129778632
git remote add <remote shortname><url> //eg: git remote add origin https://github.com/user/repo.git
git remote rm <remote shortname>
git remote rename old-name new-name
// list remote repos (not branches)
git remote -v
// eg:
// origin  https://github.com/user/repo.git (fetch)
// origin  https://github.com/user/repo.git (push)

// delete a branch from remote
git push origin --delete <branch-name>
// push to remote repo
git push -u <remote shortname><remote branchname>:<local branchname>

git fetch <remote shortname> <branch-name> // update remote changes to local remote info
git pull // git pull Without Specifying Branch: fetch and merge changesfrom tracked remote repo into local repo

// check which remote branch my current branch is tracking with
git branch -vv

// change my remote tracking
git branch --set-upstream-to=origin/feature-branch
```

branch commands
```git
//list all local branches
git branch
// list all remote branches
git branch -r

// create new branch but not switch to it
git branch <new-branch-name>
//create new branch and switch to it
git checkout -b <new-branch-name>
//switch to a existing branch
git checkout/switch <branch-name>

//change branchname
git branch -m <new-branch-name> //will change current local name to new one
git branch -m <old-branch-name> <new-branch-name> // if you are on different branch

// delete local branch
git branch -d <branch-name> // -d: delete branch that has been merged already
git branch -D dev // -D: force to delete branch

```
Git rebase
```git
git checkout feature
git rebase main
```