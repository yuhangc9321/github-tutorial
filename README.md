# GitHub Tutorial

_by Yu Hang Chen_

---
## Git vs. GitHub

What is git?

git is a version control system used to take snapshots of code.  
git does not require github.

What is github?

github stores commits within repositories and makes them easier to navigate by providing a gui.  
github requires git.

---
## Initial Setup  

go to [github](github.com)
create an account  
copy paste the ssh key
---
## Repository Setup

Use these commands to set up your local git repository.

1. `cd ~/workspace/`  
change the working directory to ~/workspace/

2. `mkdir reponame`  
create a new directory within the workspace directory

3. `git init`  
initialize git within a directory  
turns the directory into a repository.  
**git init should never be used in the ~/workspace/ directory.**

4. `git add remote origin URL`  
setup a connection between the local repo and the remote repo

extra commands
`git remote -v`
used to check if there is a connection between your local repo and the remote repo.
will print the remote repo onto the command line if a remote repo is connected.
---
## Workflow & Commands

three parts to a git project

* working directory  
* staging area  
* repository

`git add filename`

`git commit -m "message"`

`git push -u origin master`

`git push`

---
## Rolling Back Changes

git reset
git checkout