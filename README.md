# Git-Fundamentals

# What is Git?
*files and people

# Git Init

## The Three Steps of git

### 1) WT
*Git Status link

### 2) Staging: Git Add

### 3) DB: Git Commit

## git status

------------------------------------

# Branch
- What is Branching?
    - Unlike other VCS which could be a heavy process to create a branch, Git has a lightweight method when it comes to branching. By creating a branch, you are creating a non static pointer to one of the commits.
    - The main purpose of branching is to work separately from the main development branch such as **main/master**.

## create
- A new movable pointer (branch) can be created by using **git branch** command:
\ `$ git branch B` \
by doing so, a branch named **B** has been created.

### Head 
- it is a special pointer to know the active branch you are working with.
    Note: creating a new branch doesn't mean that the head is pointing to the new branch. A switch is needed to change where the head is pointing. 

## switch
- To switch to the previously created branch **B**, the command **git checkout** is used:
\ `$ git checkout B` \
by doing so, now the active branch is **B**. 


## delete
## rename 

# reading the git history
## git log, git log oneline, git log oneline graph, git diff

# merging
## fast forword
## three way
### conflict

# tags

--------------------------------------
# github

# connecting to git hub

# git clone

# git push/pull












