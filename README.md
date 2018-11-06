# Git Kitty
Documentation of frequently used git functionalities

# Initializing

## Create a local git repo from remote
1. Clone the repo from remote
```
git clone https://github.com/NaveenRokkam/Git_Kitty.git
```
---
## Create a Remote Git repo from local
1. Create new repo on github
2. Open Terminal, navigate to the local directory
3. Initialize Git repo
```
git init
```
4. Add files to local git repo
```
git add .
```
5. Commit them
```
git commit -m “First commit"
```
6. Copy Remote repo URL (https://github.com/NaveenRokkam/Git_Kitty.git)
7. Add remote URL info
```
git remote add origin https://github.com/NaveenRokkam/Git_Kitty.git
git remote -v  // > version of remote
```
8. Push change to remote
```
git push -u origin master
```

***
# Branch

#### Show a list of all branches
`git branch`


### Create a new local branch from existing Branch
```
git branch <BName>
```

### Update local work directory files to branch <BName>
```
git checkout <BName>
```

### Fetching a new branch <bNewRemote> from Remote (github) to local repository
```
git fetch & git checkout <bNewRemote>
```

### Submit a Branch to Remote
1. Checkout the branch to submit to remote `git checkout <BName>`
2. Push the changes the Remote `git push origin <BName>`

***
# Rebase

## Play branch <BName> on master
The user is currently making changes in local branch BName and wants to merge to Master

1. Play the changes of branch on Master `git rebase master`
2. Want to add more files `git add <FileName>`
3. Continue rebase i.e. play the new files on master `git rebase -continue`
4. git checkout master
```
Fast forward the master `git merge <BName>``
```



***
# Version of Commit
#### Show Commit history for Branch <BName>:
`git log <BName>`
#### Show the Head and Master in commit History for branch <BName>:
`git log <BName> -- decorate`

```
git worktree list
```
