## **This page is a response to the reading assigned for Day Three of Code102**

## **The topic of the day is: _Git Intro_**

### **The reading provides an introductory guide to using Git and covers the following topics:** 

- Version Control
- History of Git
- Getting Started
- Setting Up a Git Repository
- Work FLow
- Remote Repository

### Version control ###
**It is essentially a system that allows the user to revisit several versions of ta file(s) by capturing changes in said file(s). This allows mistakes to be corrected**
**There are three types of version control and they are: local, centralized, and distributed (Git is officially a decenctralized version control). Git allows users to create mirrored repositories which can be placed back on the server if data is lost for any unexpected loss of data.**

### Setting Up a Git Repository ###

**To create a new repository (locally) you will, generally, follow these steps:**

1. git init
1. git status
1. touch index.html
  1. git add index.html
  1. git commit -m "creates index.html"
1. git log
1. git add index.html
1. git remote add (URL)
1. git push -u origen master  (GitHub)

### Git Work Flow ###

**Work Flow is the entire process from creating a repository to editing to pushing repositories.**

**The following lists basic commands that can be used during the Git Work Flow process:**

- git (prints all commands available on git)
- git clone <URL> (this copies repository and creates a folder with its original name)
- git status (lets you see what is in the staging area, exists in the local repository and is therefore untracked)
- git add <filename> (adds file to repository and can be commited after it is added)
- git commit -m"insert description of why commit was made" (file still exists locally and has not been synchronized with remote repos)
- git commit (allows you to create a multiline message...using VIM)
- git push (this will synch local repository remotely to GitHub/)
- git pull (locally recieve the most up-to-date repository)

## [Information Source](https://blog.udemy.com/git-tutorial-a-comprehensive-guide/#6) 
