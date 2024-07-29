# Welcome to Explore-Learn-Practice(ELP) Repository for Git and GitHub!

## Table of Contents

1. [Installation](#installation)
2. [GitHub Sign-Up](#github-sign-up)
3. [Initial Configuration](#initial-configuration)
4. [Creating and Cloning Repositories](#creating-and-cloning-repositories)
5. [Working with Local and Remote Repositories](#working-with-local-and-remote-repositories)
6. [Git Staging and Committing](#git-staging-and-committing)
7. [Pushing Changes to Remote Repositories](#pushing-changes-to-remote-repositories)
8. [Pulling Changes from Remote Repositories](#pulling-changes-from-remote-repositories)
9. [Handling Merge Conflicts](#handling-merge-conflicts)
10. [Creating Files with PowerShell](#creating-files-with-powershell)
11. [Branching and Merging](#branching-and-merging)
12. [Renaming and Deleting Branches](#renaming-and-deleting-branches)
13. [Viewing Commit History](#viewing-commit-history)
14. [Stashing, Reverting, and Resetting Changes](#stashing-reverting-and-resetting-changes)

## Installation

Install Git, a version control software, from the official website:

[Download Git](https://git-scm.com/downloads)

## GitHub Sign-Up

Sign up for GitHub, a remote (online) software development platform used for storing, tracking, and collaborating on software projects:

[Sign up for GitHub](https://github.com/)

## Initial Configuration

Verify Git installation by opening your terminal and typing:
```bash
git
```
If installed correctly, a list of features will appear. If not, re-download and install Git properly.

Then Configure Git with your GitHub account username and email:
```bash
git config --global user.name 'username'
git config --global user.email 'Email Id'
```

## Creating and Cloning Repositories
Create a "new repository" on GitHub and name it. Copy the repository HTTPS URL or To initialize a new Git repository, use:
```bash
git init
```
It can convert an existing, unversioned project to a Git repository or initialize a new, empty repository
(A Git repository is a virtual storage of your project. It allows you to save versions of your code, which you can access when needed).

Open your terminal (or VSCode editor) and clone the repository:
```bash
git clone repository_Url
```
if done then we will see the '.git' folder in the hidden views option in our local directory
(Do not modify the '.git' folder, it is the link between our local and remote(online) repositories).

## Working with Local and Remote Repositories
Once the repository is cloned, create a project file. To reflect changes from your local repository to the remote GitHub repository, follow these general rules:
(General Rule: if any changes are made in the local repo, we need to do the necessary steps to reflect in the remote repo, and vice versa). <br> 
From local to remote(online): add (staging) -> commit -> push <br> 
From remote(online) to local: pull

## Git Staging and Committing
Add file changes in the working directory to the staging area:
```bash
git add [file]
```
Or add all file changes:
```bash
git add .
```
(git add does not affect the repository in any significant way—changes are not recorded until you run git commit) <br>
View the state of the working directory and the staging area:
```bash
git status
```
Commit the changes:
```bash
git commit 
```
(command captures a snapshot of the project's currently staged changes) <br>
Or commit with a message for a specific file:
```bash
git commit -m "message/comment" *filename
```
(*filename is optional to include)

## Pushing Changes to Remote Repositories
Push local repository content to a remote(online) repository:
```bash
git push
```
Or push to a specific remote branch repository:
```bash
git push origin [branch]
```

## Pulling Changes from Remote(online) Repositories
Fetch and download content from a remote repository and immediately update the local repository: (git pull=git fetch+git merge)
```bash
git pull
```
Or download content from a specific remote branch and update the local repository:
```bash
git pull origin [branch]
```

## Handling Merge Conflicts
(Version control systems are all about managing contributions between multiple distributed authors (usually developers).
Sometimes multiple developers may try to edit the same content. 
If Developer A tries to edit code that Developer B is editing a conflict may occur.)
(ex: Conflicts generally arise when two people have changed the same lines in a file, or if one developer deleted a file while another developer was modifying it.
In these cases, Git cannot automatically determine what is correct. Conflicts only affect the developer conducting the merge, the rest of the team is unaware of the conflict.
Git will mark the file as being conflicted and halt the merging process. It is then the developer's responsibility to resolve the conflict.
The most direct way to resolve a merge conflict is to manually edit the conflicted file.) <br>

i.e. Conflicts arise when multiple developers edit the same content. Git will mark the file as conflicted and halt the merging process. Manually resolve conflicts in each file marked by Git. 
To find differences between states of a repository/files, Use:
```bash
git diff
```

## Creating Files with PowerShell
Create an empty file using PowerShell:
```powershell
New-Item -ItemType file [file_name.txt]
```
Echos(prints) content into a Out-File [file_name.txt]:
```powershell
echo "Hello, this is the content of the file" | Out-File [file_name.txt]
```


14: Git Branching and merging
    (Branches allow you to work on different parts of a project without impacting the main branch.
    When the work is complete, a branch can be merged with the main project.
    You can even switch between branches and work on different projects without them interfering with each other)
    < git branch > - List all of the branches in your repository(branch is a new/separate version of the main repository)
    < git checkout -b [branch] > - Create a new branch called [branch]
    < git checkout [branch] > - Switch between branches [branch]
    < git branch -a > - command is used to list all branches in a Git repository, including both local branches and remote branches
    (" -a " option stands for "all").
    
## Branching and Merging
Branches allow you to work on different parts of a project without impacting the main branch. Create a new branch:

bash
Copy code
git branch
List all branches:

bash
Copy code
git branch -a
Create a new branch:

bash
Copy code
git checkout -b [branch]
Switch between branches:

bash
Copy code
git checkout [branch]

## Renaming and Deleting Branches
Rename a branch in the local repository:

bash
Copy code
git checkout [other_branch]
git branch -m [old_branch_name] [new_branch_name]
Rename a branch in the remote repository:

bash
Copy code
git push origin --delete [old_branch_name]
git push origin [new_branch_name]
Delete a branch in the local repository:

bash
Copy code
git checkout [other_branch]
git branch -d [branch_name]
Force delete a branch with unmerged changes:

bash
Copy code
git branch -D [branch_name]
Delete a branch in the remote repository:

bash
Copy code
git push origin --delete [branch_name]
Remove references to deleted branches from your local repository:

bash
Copy code
git fetch --prune




-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## License

[![license](https://img.shields.io/github/license/rahulkrishy/ELP_Github?style=for-the-badge)](LICENSE)
