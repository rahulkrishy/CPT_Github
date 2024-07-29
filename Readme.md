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
(git add does not really affect the repository in any significant way—changes are not actually recorded until you run git commit) <br>
View the state of the working directory and the staging area:
```bash
git status
```
Commit the changes:
```bash
git commit 
```
(command captures a snapshot of the projects currently staged changes) <br>
Or commit with a message for a specific file:
```bash
git commit -m "message/comment" *filename
```
(*filename is optional to include)

## Pushing Changes to Remote Repositories

## Pulling Changes from Remote Repositories

10: < git push > - command is used to upload local repository content to a remote repository, or
    < git push origin [branch] > - command is used to upload local repository content to a specific remote [branch] repository.

11: (To get lastest file from the remote repo to our local repo) use
    < git pull > - command is used to fetch and download content from a remote repository and immediately update the local repository to match that content(git pull=git fetch+git merge) 
    < git pull origin [branch] > - command is used to download content from a remote [branch] repository and immediately update the local repository.



-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## License

[![license](https://img.shields.io/github/license/rahulkrishy/ELP_Github?style=for-the-badge)](LICENSE)
