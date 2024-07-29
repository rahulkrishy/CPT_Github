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
It can be used to convert an existing, unversioned project to a Git repository or initialize a new, empty repository.
(A Git repository is a virtual storage of your project. It allows you to save versions of your code, which you can access when needed)

Open your terminal (or VSCode editor) and clone the repository:
```bash
git clone repository_Url
```
if done then we will see ".git" folder in hidden views option in the our local directory
(Do not do any modification to .git folder, its the link between our local and remote(online) repositories).




07: Once the repository is cloned,
    create a project file and follow below steps to push from your local repository to remote(online) GitHub repository. 
    (General Rule: if any changes made in local repo, we need to do nessecary steps reflet in remote repo, and vice versa)
    (from local to remote(online): add(staging)->commit->push, from remote(online) to local: pull)





-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## License

[![license](https://img.shields.io/github/license/rahulkrishy/ELP_Github?style=for-the-badge)](LICENSE)
