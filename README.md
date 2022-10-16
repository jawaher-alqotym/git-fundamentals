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
## rename 

# Reading the Git History

## Git Log
Each branch has a history of commits to check them you can run the command: `$ git log ` .It lists the details of all the commits made in the repository starting with most recent commit first. The details will include a unique identifier called a **hash**  which is written as a 40-character hexadecimal string like `7c35a3ce607a14953f070f0f83b5d74c2296ef93`. The details will also have the author's name and email, the date and the commit message.

###  git log --oneline

There are other various options to the git log command that are very useful. First, the `$ git log --oneline` command it is very useful when there is a lot of commits, it would view each commit on a single line with a brief description which will show the first seven characters of the commit's hash and the commit message. 

### git log --graph

Another useful command is `$ git log --graph`  it shows the branch and merge history as a text-based graphical representation on the left hand side of the output. You can combine this command with 
--oneline option `$ git log --oneline  --graph `. 

## Git Diff

Another command for reading the history is `$ git log diff`  it is used to see the difference between your working tree and your staging area when you want to know exactly what has been changed inside the files it shows the exact lines added and removed.




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












