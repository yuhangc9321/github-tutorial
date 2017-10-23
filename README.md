# GitHub Tutorial

_by Yu Hang Chen_

---
## Git vs. GitHub

What is git?

git is a version control system used to take snapshots of code.  
git does not require github.

What is github?

github stores commits (repos, code) and makes them easier to navigate by providing a gui.  
github requires git.

---
## Initial Setup

go to [github](github.com)
create an account
copy paste the ssh key
---
## Repository Setup

1. `mkdir filename`  
use this to create a folder within the workspace directory

2. `git init`  
to initialize git within a directory  
this turns the directory into a repository (local repo).  
git init should never be used in the ~/workspace/ directory.

3. `git add remote origin URL`  
to setup a connection between the local repo and the remote repo  

4. `git remote -v` 
to check if there is a connection.


---
## Workflow & Commands

three parts to a git project

* working directory  
* staging area  
* repository
    * this is the local repo

`git add filename`

`git commit -m "message"`

`git push -u origin master`

`git push`

---
## Rolling Back Changes

git reset
git checkout