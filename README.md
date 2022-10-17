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

# Reading the Git History

## Git Log
Each branch has a history of commits to check them you can run the command: `$ git log ` .It lists the details of all the commits made in the repository starting with most recent commit first. The details will include a unique identifier called a **hash**  which is written as a 40-character hexadecimal string like `7c35a3ce607a14953f070f0f83b5d74c2296ef93`. The details will also have the author's name and email, the date and the commit message.

###  git log --oneline

There are other various options to the git log command that are very useful. First, the `$ git log --oneline` command it is very useful when there is a lot of commits, it would view each commit on a single line with a brief description which will show the first seven characters of the commit's hash and the commit message. 

### git log --graph

Another useful command is `$ git log --graph`  it shows the branch and merge history as a text-based graphical representation on the left hand side of the output. You can combine this command with 
--oneline option `$ git log --oneline  --graph `. 

## Git Diff

Another command for reading the history is `$ git diff`  it is used to see the difference between your working tree and your staging area when you want to know exactly what has been changed inside the files it shows the exact lines added and removed.


# Merging
Git merging combines commit's sequences  into one unified history of commits. There are two main ways Git will merge: Fast Forward and Three way.

## Fast Forward 
After creating a new branch **A**  and doing some commits now you want to merge the work with your main branch, in this case you only need to switch back to the main branch  `$ git checkout main ` and merge from there,  `$ git merge A` , then Git simply moves the pointer forward to the last commit in branch A. 

## Three Way

Suppose you created another branch **B** and while working on it the main branch progresses so it has some commits ahead from your branch **B**. Then when you are done from branch **B** you want to merge the work back with main. Git will create a new snapshot that results from this three-way merge and automatically creates a new commit that points to it. This is referred to as a merge commit, and is special in that it has more than one parent.  First checkout to branch main `$ git checkout main ` then merge it with branch **B** `$ git merge main ` 

### Conflicts
Occasionally, this process doesn’t go smoothly. If you changed the same part of the same file differently in the two branches you’re merging in this case your branch main and branch, therefore Git will pause the commit while you resolve the conflict. To check which files are unmerged because of the conflict run `$ git status ` . To resolve the conflict open the file with that has the conflict, Git will indicate the changes pointing out what the  caused the conflict so you can solve them manually. After resolving the conflict commit it. 

# tags

--------------------------------------
# github

# connecting to git hub

# git clone

# git push/pull












