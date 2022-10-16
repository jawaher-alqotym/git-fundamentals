# Git-Fundamentals

# What is Git?
Git is a DevOps tool used for file management enabling multiple developers to work together created by Linus Torvalds in 2005 for the development of the Linux kernel. It is a free and open-source version control system used to handle small to very large projects efficiently. Git is used to tracking changes in any type of files like source code files.

Git thinks of its data more like a series of snapshots of a miniature filesystem. With Git, every time you commit, or save the state of your project, think of it as if Git takes a picture of what all your files look like at that moment and stores a reference to that snapshot.

Before diving deep, let’s explain a scenario before Git:
- Developers used to submit their codes to the central server without having copies of their own
- Any changes made to the source code were unknown to the other developers
- There was no communication between any of the developers

<img width="398" alt="Screen Shot 1444-03-20 at 1 10 56 PM" src="https://user-images.githubusercontent.com/96193859/196031114-6891f996-618c-4a10-9447-090a13a64b06.png">

Now let’s look at the scenario after Git:
- Every developer has an entire copy of the code on their local systems
- Any changes made to the source code can be tracked by others
- There is regular communication between the developer

<img width="413" alt="Screen Shot 1444-03-20 at 12 41 09 PM" src="https://user-images.githubusercontent.com/96193859/196031191-d5a50599-534a-4f6e-827c-d51b996477b5.png">




*files and people



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

## git status

------------------------------------

# Branch

## create

## switch
### Head 

## delete, rename 

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


-------------------------------------
# What’s the difference between git and github

Git is a free, open-source distributed version control tool that may be used for both small and big projects. Git was created to make it easier for programmers and developers to collaborate.

GitHub is a central repository and cloud-based service that allows developers to store and manage their code in the cloud, as well as track and control modifications.









