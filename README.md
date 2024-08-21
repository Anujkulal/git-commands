#### Configuring user information used across all local repositories:
set a name that is identifiable for credit when review version history
```
git config --global user.name “[firstname lastname]”
```

set an email address that will be associated with each history marker
```
git config --global user.email “[valid-email]”
```

set automatic command line colouring for Git for easy reviewing
```
git config --global color.ui auto
```

List the user information
```
git config --list
```

<hr>
#### Initialisation:
```
git init
```

Adding file:
```
git add .
```

View status:
```
git status
```

Save the changes:
```
git commit -m "some message"
```

Transmit local branch commits to the remote repository branch:
```
git push origin main
```

Retrieve an entire repository from a hosted location via URL:
```
git clone <-link->
```

Add a git URL:
```
git remote add origin <-link->
```

<hr>

Display remote repos:
```
git remote -v
```

<hr>


#### Branch:
List branch:
```
git branch
```

To rename branch:
```
git branch -M main
```

Switch to another branch:
```
git checkout <-branch name->
```

To create new branch:
```
git checkout -b <-new branch name->
```

To delete branch:
```
git branch -d  <-branch name->
```

Push code:
```
git push origin <-branch name->
```

<hr>
#### Fetch, pull, merge, diff:
fetch down all the branches from that Git remote
```
git fetch origin main
```

merge a remote branch into your current branch to bring it up to date:
```
git merge origin/main
```

fetch and merge any commits from the tracking remote branch:
```
git pull origin main
```

show the difference between various states of repo:
```
git diff
```

Following the error when doing a git pull origin master:
`fatal: refusing to merge unrelated histories`

Run the below command:
```
git pull origin main --allow-unrelated-histories
```

Error during merge or Error on other git operations:
```
git merge origin/main  --allow-unrelated-histories
```

<hr>

#### Undoing changes:
Staged changes:
```
git reset <-filename->
git reset
```

commited changes:
`For one commit:`  
```
git reset HEAD~1
```

`For many commits:`
```
git reset <-commit->
git reset --hard <-commit->
```

<hr>