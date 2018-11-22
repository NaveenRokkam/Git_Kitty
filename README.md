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
1. Create new repo on github website
2. Create new repo on local machine
2.1 Open Terminal, navigate to the local directory
2.2 Initialize Git repo
```
git init
```
2.3. Add files to local git repo
```
git add .
```
2.4. Commit them
```
git commit -m “First commit"
```
3. Link the remote repo and local repo
3.1 Copy Remote repo URL (https://github.com/NaveenRokkam/Git_Kitty.git)
3.2 Add remote URL info
```
git remote add origin https://github.com/NaveenRokkam/Git_Kitty.git
git remote -v  // > version of remote
```
3.3 Push change to remote
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

# You forked a source and source has moved ahead. How to make your Fork up to date with Source and then apply your local <br> changes to Source.

#### Add a new remote : `Upstream` for the Source git repo
1. ``` git remote add Upstream https://github.com/NaveenRokkam/Git_Kitty.git ( Originial source which was used to fork)
```
2. ``` git remote -v
```

#### Fetch the `Upstream` changes into local master
```git pull upstream master
```

#### Push changes from local master to Originial
``` git push origin master
```
Now the upstream repository changes are available in origin/master and local master branches

Update your local branch <br> with local master using [rebase](#id123)


# When local branch is not in sync with local master (#id123)
``` git checkout <br>
    git rebase master
```
Rebase: The current branch <br> would be brought to the same commit as Master and the delta changes in <br> would be played on top of the master Commit.

Now there is a new commit and the master is behind.
``` git checkout master
    git merge <br>
```
This will fast forward master to the newest commit on <br>
