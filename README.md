# GitHub Tutorial

by Yu Hang Chen

---
## Git vs. GitHub

What is Git?

Git is a version control system used to take snapshots of code.  
Git does not require github.

What is Github?

Github stores commits within repositories and makes them easier to navigate by providing a GUI.  
Github requires git.

---
## Initial Setup

Follow these steps to set up a Github account.

1. Navigate to [Github](github.com) 
2. Create an account 
    * Follow the signup instructions on the landing page.
3. Navigate to your profile settings.
4. Go to the "SSH and GPG keys" section on the left sidebar.
5. Click on "New SSH Key".
6. Assuming you're using Cloud9, Navigate to your Cloud9 and copy paste the seccond SSH key into Github.
7. Add the SSH key.
8. On Cloud9, type `ssh -T git@github.com`.  
It should display this message: Hi <your username>! You've successfully authenticated, but GitHub does not provide shell access._

---
## Repository Setup

Follow these steps to set up your local repository and your remote (Github) repository.

1. `cd ~/workspace/`  
change the working directory to ~/workspace/

2. `mkdir reponame`  
create a new directory within the workspace directory

3. `git init`  
initialize git within a directory  
turns the directory into a repository.  
**git init should never be used in the ~/workspace/ directory.**
    * `rm -rf .git`  
    will remove the .git directory  
    this "uninitializes" git

4. `git add remote origin URL`  
setup a connection between the local repo and the remote repo
    * `git remote -v`  
    used to check if there is a connection between your local repo and the remote repo.  
    will print the remote repo onto the command line if a remote repo is connected.

---
## Workflow & Commands

There are three parts to a git project.

* **working directory**  
* **staging area**  
* **repository**
1. `git status`  
Use this to check what files have been added to the staging area and which haven't.

1. `git add filename`  
Add a file from the working directory to the staging area.

2. `git commit -m "message"`  
Take a snapshot of the code.
Include a message stating what this commit does.
    * The message should be in the present tense.

3. `git push -u origin master`  
Send a commit from the local repo to the remote repo.  
Next time you push, you only need to type `git push`.

4. `git push`  
Send a commit from the local repo to the remote repo.
    * `git pull`  
    Bring changes from the remote repo to the local repo.

---
## Rolling Back Changes

Use these commands to undo changes.

* `git checkout -- filename`
Use this to undo edits.

* `git reset HEAD filename`
Use this to undo git add.

* `git reset --soft HEAD~1`
Use this to undo a commit.

* `git reset HEAD~1`
Use this to undo a commit and clear the staging area.

* `git reset --hard HEAD~1`
Use this to undo a commit, clear the staging area, and undo edits.  
This takes us back to the previous commit.

Follow these steps to undo `git push`.

1. `git log`
Use this to get the commit SHA and then press q to quit.

2. `git revert commitsha`
A commit sha will always start with letter where a is the most recent commit, be is the second most recent commit, and so on.  
This is followed by a 7 character string of letters and numbers.  
So for example a652dfaa would be the most recent commit.  
b45s8ffa would be the second most recent commit.