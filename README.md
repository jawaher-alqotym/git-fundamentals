# Git-Fundamentals

# What is Git?
Git is a DevOps tool used for file management enabling multiple developers to work together created by Linus Torvalds in 2005 for the development of the Linux kernel. It is a free and open-source version control system used to handle small to very large projects efficiently. Git is used to tracking changes in any type of files like source code files.

Git thinks of its data more like a series of snapshots of a miniature filesystem. With Git, every time you commit, or save the state of your project, think of it as if Git takes a picture of what all your files look like at that moment and stores a reference to that snapshot.

Before diving deep, let’s explain a scenario before Git:
- Developers used to submit their codes to the central server without having copies of their own

- Any changes made to the source code were unknown to the other developers

- There was no communication between any of the developers

*files and people



# Git Init

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

GitHub is a website and cloud-based service that allows developers to store, manage, and track changes to their work and collaborate.
# connecting to git hub

# git clone

# git push/pull


-------------------------------------
# What’s the difference between git and github
Git is a version control system that allows you to manage and track the history of your work. While GitHub is a cloud-hosted service that allows you to manage Git repositories.







