# GitHub Tutorial

_by Yu Hang Chen_

---
## Git vs. GitHub

#### What is git?  
git is a version control system used to take snapshots of code.  
git does not require github.

#### What is github?
github stores commits (repos, code) and makes them easier to navigate by providing a gui.  
github needs git to operate.

---
## Initial Setup

mkdir
use this tocreate a folder within the workspace directory

git init  
to initialize git within a directory  
this turns the directory into a repository (local repo).  
git init should never be used in the ~/workspace/ directory.


---
## Repository Setup

git add remote origin URL  
(explain each part)
to setup a connection between the local repo and the remote repo  

git remote -v  
to check if there is a connection.


---
## Workflow & Commands

three parts of a git project
```
1. working directory  
2. staging area  
3. repository (remote repo / github)
```
git add filename

git commit -m "message"

git push

---
## Rolling Back Changes