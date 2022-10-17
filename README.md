# Git-Fundamentals

# What is Git?
Git is a DevOps tool used for file management enabling multiple developers to work together created by Linus Torvalds in 2005 for the development of the Linux kernel. It is a free and open-source version control system used to handle small to very large projects efficiently. Git is used to tracking changes in any type of files like source code files.

Git thinks of its data more like a series of snapshots of a miniature filesystem. With Git, every time you commit, or save the state of your project, think of it as if Git takes a picture of what all your files look like at that moment and stores a reference to that snapshot.

Before diving deep, let’s explain a scenario before Git:
- Developers used to submit their codes to the central server without having copies of their own
- Any changes made to the source code were unknown to the other developers
- There was no communication between any of the developers
<p align="center">
<img width="398" alt="Screen Shot 1444-03-20 at 1 10 56 PM" src="https://user-images.githubusercontent.com/96193859/196031114-6891f996-618c-4a10-9447-090a13a64b06.png">
</p>

Now let’s look at the scenario after Git:
- Every developer has an entire copy of the code on their local systems
- Any changes made to the source code can be tracked by others
- There is regular communication between the developer
<p align="center">
<img width="413" alt="Screen Shot 1444-03-20 at 12 41 09 PM" src="https://user-images.githubusercontent.com/96193859/196031191-d5a50599-534a-4f6e-827c-d51b996477b5.png">
</p>







# Git Init

git init is one way to start a new project with Git. To start a repository, use git init .
To initialize a repository, Git creates a hidden directory called .git. That directory stores all of the objects and refs that Git uses and creates as a part of your project's history. 

```
git init
```



## The Three States of Git
Files in Git can be in one of three following states: WT (working tree), staging, or committed.</br>The fundamental Git workflow is as follows:</br> In your working tree, you alter files. Then you add only those modifications to the staging area and lastly when you commit, the files in the staging area are taken as-is and permanently stored in your Git directory.

### 1) Working Tree

In this stage, you can do whatever you need to the files that exist in the project folder directory. Think of it as the working space where you create, edit, and delete files/file's content and folders.</br>If you need to view the differences between the working tree and the indexed file (files that wore moved to the next [stage](https://github.com/jawaher-alqotym/git-fundamentals/blob/section-A/README.md#2-staging-git-add) ). Git provides you with the command [git status](https://github.com/jawaher-alqotym/git-fundamentals/blob/section-A/README.md#git-status). note here that git compears the working tree with the database residing in .git file when git status is called.

### 2) Staging: Git Add

The staging area sometimes referred to as "index" is a file that resides in your Git directory and contains details about the content of your upcoming commit. To move files to this stage use one of the following commands.

```
git add <file-name>
```
```
git add <.../file-name>
```
```
git add .
```

### 3) DB: Git Commit

Git keeps the object database and metadata for your project in the Git directory. When you clone a repository from another machine, this is what gets copied because it is the most crucial component of Git.
```
git commit -m 'messege'
```
## git status

The git status command shows the current state of the working directory and staging area. It shows you which changes have been staged and which have not.
```
git status
```

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

# Tags
- Tagging is used to tag important commits that are already in the repo history. Tags can be used to specify the different versions of a software during the development process.

## List Tags
- To show all the tags, the following command is used:
<br> `$ git tag` \
by doing so, all tags will be listed in alphabetical order. \
*OR*
- To show the tags of a certain pattern or series, use the following command:
<br> `$ git tag -l "v1.2.0*"` \
by doing so, all tags that starts with **v1.2.0** will be listed.

## Create Tags
- Git has two type of tags:
    1. lightweight tags 
        - a pointer at a certain commit, so it is a file storing the commit checksum.
        - To create a lightweight tags, use the command:
        <br> `$ git tag v1.3.0` \
        by doing so, the tag **v1.3.0** will be created.
    2. annotated tags
        - an object stored in git database, containing more information other than the commit checksum such as tagging message, tagger name, email, and date.
        - To create an annotated tags, use **-a** with tag command:
        <br> `$ git tag -a v1.5 -m "the tagging message you want"` \
        by doing so, a tag named v1.5 with a message you specify will be created.
## Share Tags 
- Tags are created locally and can be shared to the remote server only with the following command:
<br> `$ git push origin v1.5` \
by writing origin after the push command, the remote server will contain the previously created tag **v1.5**.
        

## Delete Tags
- To delete a tag locally, run the following command:
<br> `$ git tag -d v2.0` \
by doing so, the local tag **v2.0** will be deleted.
- To delete a tag on the remote server:
<br> `$ git push origin --delete v2.0` \
by doing so, the remote tag **v2.0** will be deleted.

## Checkout Tags
- To checkout a tag, use the command:
<br> `$ git checkout v3.9.0` \
by doing so, you will be able to view the versions of files that **v3.9.0** is pointing to.

--------------------------------------
# github

GitHub is a website and cloud-based service that allows developers to store, manage, and track changes to their work and collaborate.
# connecting to git hub


To access GitHub you must do it by authenticating to GitHub, you can securely access your account's resources, using different credentials depending on where you authenticate.
Personal access tokens (PATs) are an alternative to passwords for GitHub authentication when using the GitHub API.
This also has the added benefit of raising your rate limit. You will be limited to 60 requests per hour if you do not authenticate. You can make up to 5,000 requests per hour if you authenticate.

# What’s the difference between git and github

Git is a version control system that lets you manage and keep track of your source code history.

GitHub is a central repository and cloud-based service that allows developers to store and manage their code in the cloud, as well as track and control modifications.


# git clone

git clone (download) a repository that already exists on GitHub, including all of the files and commits.

```
git clone [url]
```

# git push/pull

The git pull command downloads changes from a remote repository and saves them to a local repository. It combines changes from upstream into your local repository.

```
git pull
```
Git push is a command that pushes your local modifications to a central repository.

```
git push
```

-------------------------------------








