// Git & GitHub

step 01: Install Git - version control software. (https://git-scm.com/downloads)

step 02: Sign up to Github - remote(online) software development platform, 
         it's used for storing, tracking, and collaborating on software projects. (https://github.com/)

step 03: To check git software is installed on your device, open terminal and type 
         " git ", it will pop up list of feature available on it, it not redownload it properly.

step 04: Next we need to configure our github account username and email to device, 
         open terminal and type " git config --global user.name "username" " and 
         " git config --global user.email "Email Id" ".

step 05: Click Create a "new repository" in Github and name it, then copy the repository https url 
         (A 'Git repository' is a virtual storage of your project. It allows you to save versions of your code, which you can access when needed).

step 06: Open device terminal (*or Vscode editor), and type " git clone repository_Url " to clone repository,
         if done then we will see " .git " folder in hidden views option in the our local directory
         (Don't do any modification to .git folder, its the link between our local and remote(online) repositories).

step 07: Once the repository is cloned,
         create a project file and follow below steps to push from your local repository to remote(online) GitHub repository. 
         (General Rule: if any changes made in local repo, we need to do nessecary steps reflet in remote repo, and vice versa)
         (from local to remote(online): add(staging)->commit->push, from remote(online) to local: pull)

step 08: " git add <file> " - command adds a file change in the working directory to the staging area 'or 
         " git add . "      - command adds all files change in the working directory to the staging area.
         (git add doesn't really affect the repository in any significant way—changes are not actually recorded until you run git commit)
         (" git status " to view the state of the working directory and the staging area).

step 09: " git commit " - command captures a snapshot of the project's currently staged changes 'or
         " git commit -m "message/comment" *filename " - command commits with message for filename(*filename is optional to include).

step 10: " git push " - command is used to upload local repository content to a remote repository 'or
         " git push origin <branch> " - command is used to upload local repository content to a specific remote <branch> repository.

step 11: (To get lastest file from the remote repo to our local repo) use
         " git pull " - command is used to fetch and download content from a remote repository and immediately update the local repository to match that content(git pull=git fetch+git merge) 
         " git pull origin <branch> " - command is used to download content from a remote <branch> repository and immediately update the local repository.

step 12: Git merge conflicts
         (Version control systems are all about managing contributions between multiple distributed authors (usually developers).
         Sometimes multiple developers may try to edit the same content. 
         If Developer A tries to edit code that Developer B is editing a conflict may occur.)
         (ex: Conflicts generally arise when two people have changed the same lines in a file, or if one developer deleted a file while another developer was modifying it.
         In these cases, Git cannot automatically determine what is correct. Conflicts only affect the developer conducting the merge, the rest of the team is unaware of the conflict.
         Git will mark the file as being conflicted and halt the merging process. It is then the developers' responsibility to resolve the conflict.
         The most direct way to resolve a merge conflict is to manually edit the conflicted file.)
         (" git diff " - command helps find differences between states of a repository/files. This is useful in predicting and preventing merge conflicts)

step 13: Git Branching and merging
         (Branches allow you to work on different parts of a project without impacting the main branch.
         When the work is complete, a branch can be merged with the main project.
         You can even switch between branches and work on different projects without them interfering with each other)
        " git branch " - List all of the branches in your repository(branch is a new/separate version of the main repository)
        " git checkout -b <branch> " - Create a new branch called ＜branch＞
        " git checkout <branch> " - Switch between branches ＜branch＞
        " git branch -a " - command is used to list all branches in a Git repository, including both local branches and remote branches('-a' option stands for "all").

step 14: Rename the branch
         (1)(To rename in local branch repo)
         " git checkout <other_branch> " - Before renaming the branch, switch to a branch other than the one you want to rename. You cannot rename the branch you are currently on.
         " git branch -m <old_branch_name> <new_branch_name> " - rename the old_branch_name with new_branch_name
         (2)(To rename in remote branch repo - If the branch has been pushed to the remote repository, you may want to update the remote branch name as well. Use the following command to delete the old remote branch and push the new one:)
         " git push origin --delete <old_branch_name> " - ( Renaming a branch in Git doesn't create a copy of the branch; instead, it directly renames the existing branch. However, when it comes to the remote repository, Git maintains separate references for local and remote branches. When you rename a branch locally using git branch -m, the remote repository still has a reference to the old branch name. To update the remote reference and reflect the name change, you use git push origin --delete <old_branch_name> to delete the old branch on the remote repository, followed by git push origin <new_branch_name> to push the renamed branch. )
         " git push origin <new_branch_name> " - command pushes the renamed branch to the remote repository with the new name.

step 15: Delete the branch
         (1)(To delete in local branch repo)
         " git checkout <other_branch> " - Before deleting the branch, switch to a branch other than the one you want to deleting. You cannot delete the branch you are currently on.
         " git branch -d <branch_name> " - Deletes the specified branch. If the branch has unmerged changes, Git will prevent the deletion,   and you'll need to use -D to force the deletion. 'Or
         " git branch -D <branch_name> " - Forces the deletion of the specified branch, even if it has unmerged changes. Use this with caution, as it discards any changes in the branch.
         (2)(To delete in remote branch repo)
         " git push origin --delete <branch_name> " - To delete a remote branch
         (3)(remove any references to deleted branches from your local repository)
         " git fetch --prune " - command is used to update your local Git repository by fetching changes from the remote repository and pruning (deleting) any remote branches that no longer exist on the remote.

step 16: stash/Reset/Revert the branch
         ( 'Git stash' is a command that is used to temporarily save and untrack your local changes that you haven't staged yet. It is useful when you need to switch branches or work on another task but don't want to lose your uncommitted changes.
         "git stash" - will save your 'uncommitted changes' to a stack and untrack them from your working directory. You can then switch branches or work on another task without having to worry about losing your changes.
         "git stash pop" - will restore your uncommitted changes to your working directory and re-track them.
         "git stash list" - will show you a list of all the stashed changes that you have made.)
         ()
         ()




