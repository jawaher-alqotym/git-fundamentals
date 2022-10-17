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








