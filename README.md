# test-v0.1
## acronym
- WD = working directory
- SA = staging area
- Rp = Repository


## commands

### START
`git init`


### commit
`git status`\
`git add`\
`git commit`\
**or**\
`git add . ; git commit`\
`git add . ; git commit -m "description"`\
**+ push**\
`git add . ; git commit -m "description" ; git push -u origin main`

### log
`git log --graph --oneline --branches`\
`git log --oneline --branches --graph -- index.html`\
`git log --oneline --branches --graph -- index.*`

### checkout
- switch to previous commits\
`git checkout master`\
`git checkout hash`\
`git checkout HEAD~3`

### blame (show changes in a file)
`git blame --color-lines README.md`
___

### Branches
> show all existing branches\
`git branch`

> creates a new branch\
`git branch BRANCH NAME`

> switches to a branch\
`git checkout BRANCH NAME`

> create a new branch and switch directly to it\
`git checkout -b BRANCH NAME`

### FAST-FORWARD-MERGE
> merge branches\
`git checkout master` `git merge BRANCH NAME`

> delete branch after the merge\
`git checkout master` `git branch -d BRANCH NAME`

### 3-WAY-MERGE
**from:**

          A---B---C FEATURE BRANCH
         /
    D---E---F---G MAIN

**to:**

          A---B---C FEATURE BRANCH
         /         \
    D---E---F---G---H MAIN


`git checkout master` `git merge FEATURE BRANCH`

- delete branch after the merge\
`git checkout master` `git branch -d BRANCH NAME`

### rebase 313
`git checkout BRANCH`\
`git rebase MAIN`\
`  git add FILE`\
`  git commit -m "DESCRIPTION"`\
`  git rebase --continue`\
`git checkout MAIN`\
`git merge BRANCH`\
`git branch -d BRANCH`
### merge conflict 30

### git diff
- difference between WD <--> SA\
`git diff`

- difference between SA <--> Rp\
`git diff --cached`

**or**\
`git diff hash1 hash1`\
`git diff hash1 hash1 -- index.html`

### delete commit history

`git checkout --orphan latest_branch` &&
`git add -A` &&
`git commit -am "commit message"` &&
`git branch -D main` &&
`git branch -m main` &&
`git push -f origin main`


### git fetch
- downloads commits and branches from a remote repository\
`git log --graph --oneline --branches origin/main`\
`git branch -vv`\
`git fetch` && `git merge origin/main`
#### ENDE
