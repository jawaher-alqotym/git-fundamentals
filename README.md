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
<br> `$ git branch B` \
by doing so, a branch named **B** has been created.

### Head 
- it is a special pointer to know the active branch you are working with.
    Note: creating a new branch doesn't mean that the head is pointing to the new branch. A switch is needed to change where the head is pointing. 

## switch
- To switch to the previously created branch **B**, the command **git checkout** is used:
<br> `$ git checkout B` \
by doing so, now the active branch is **B**. 


## delete
- To delete a branch locally, use the following command:
<br> `$ git branch -d B` \
*OR*
<br> `$ git branch --delete B` \
by doing so, the branch **B** will be deleted. 

## rename 
- It takes three mandatory steps to fully change the name of a branch:
1. rename it locally by using the command:
<br> `$ git branch --move B C` \
by doing so, the branch **B** will be replaced with **C**. 

2. push it to the remote repo:
<br> `$ git push --set-upstream origin C` \
by doing so, the branch **C** can be seen by other collaborators on the remote repo. 

3. showing all the branches (optional)
<br> `$ git branch --all` \
by doing so, all existing branches will be displayed. This step helps us checking if the rename process is correct. Yet, it can be noticed that the old branch **B** still exists. Therefore, step 4 is needed.
4. delete the old branch 
<br> `$ git push origin --delete B` \
by doing so, the branch **B** will be deleted. 

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












