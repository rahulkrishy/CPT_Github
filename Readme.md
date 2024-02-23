```sh
// Git & GitHub

01: Install Git - version control software. (https://git-scm.com/downloads)

02: Sign up to Github - remote(online) software development platform,
    it is used for storing, tracking, and collaborating on software projects. (https://github.com/)

03: To check git software is installed on your device, open terminal and type 
    < git >, it will pop up list of feature available on it, is not redownload it properly.

04: Next we need to configure our github account username and email to device, open terminal and type 
    < git config --global user.name 'username' > and 
    < git config --global user.email 'Email Id' >

05: Click Create a "new repository" in Github and name it, then copy the repository https url or
    < git init > command creates a new Git repository. It can be used to convert an existing, unversioned project to a Git repository or initialize a new, empty repository.
    (A Git repository is a virtual storage of your project. It allows you to save versions of your code, which you can access when needed)

06: Open device terminal (*or Vscode editor), and type <git clone repository_Url> to clone repository,
    if done then we will see ".git" folder in hidden views option in the our local directory
    (Do not do any modification to .git folder, its the link between our local and remote(online) repositories).

07: Once the repository is cloned,
    create a project file and follow below steps to push from your local repository to remote(online) GitHub repository. 
    (General Rule: if any changes made in local repo, we need to do nessecary steps reflet in remote repo, and vice versa)
    (from local to remote(online): add(staging)->commit->push, from remote(online) to local: pull)

08: < git add <file> > - command adds a file change in the working directory to the staging area, or 
    < git add . >      - command adds all files change in the working directory to the staging area.
    (git add does not really affect the repository in any significant way—changes are not actually recorded until you run git commit)
    (< git status > to view the state of the working directory and the staging area).

09: < git commit > - command captures a snapshot of the projects currently staged changes, or
    < git commit -m "message/comment" *filename > - command commits with message for filename(*filename is optional to include).

10: < git push > - command is used to upload local repository content to a remote repository, or
    < git push origin [branch] > - command is used to upload local repository content to a specific remote [branch] repository.

11: (To get lastest file from the remote repo to our local repo) use
    < git pull > - command is used to fetch and download content from a remote repository and immediately update the local repository to match that content(git pull=git fetch+git merge) 
    < git pull origin [branch] > - command is used to download content from a remote [branch] repository and immediately update the local repository.

12: Git merge conflicts
    (Version control systems are all about managing contributions between multiple distributed authors (usually developers).
    Sometimes multiple developers may try to edit the same content. 
    If Developer A tries to edit code that Developer B is editing a conflict may occur.)
    (ex: Conflicts generally arise when two people have changed the same lines in a file, or if one developer deleted a file while another developer was modifying it.
    In these cases, Git cannot automatically determine what is correct. Conflicts only affect the developer conducting the merge, the rest of the team is unaware of the conflict.
    Git will mark the file as being conflicted and halt the merging process. It is then the developers responsibility to resolve the conflict.
    The most direct way to resolve a merge conflict is to manually edit the conflicted file.)
    (< git diff > - command helps find differences between states of a repository/files. This is useful in predicting and preventing merge conflicts)  

13: To create an empty file using PowerShell, use
    < New-Item -ItemType file <file_name.txt> > - command creates a new file named file_name.txt
    < echo "Hello, this is the content of the file" | Out-File [file_name.txt] > - command echoes (prints) the specified text to Out-File [file_name.txt]

14: Git Branching and merging
    (Branches allow you to work on different parts of a project without impacting the main branch.
    When the work is complete, a branch can be merged with the main project.
    You can even switch between branches and work on different projects without them interfering with each other)
    < git branch > - List all of the branches in your repository(branch is a new/separate version of the main repository)
    < git checkout -b [branch] > - Create a new branch called [branch]
    < git checkout [branch] > - Switch between branches [branch]
    < git branch -a > - command is used to list all branches in a Git repository, including both local branches and remote branches
    (" -a " option stands for "all").

15: Rename the branch
    (1)(To rename in local branch repo)
    < git checkout [other_branch] > - Before renaming the branch, switch to a branch other than the one you want to rename. You cannot rename the branch you are currently on.
    < git branch -m [old_branch_name] [new_branch_name] > - rename the old_branch_name with new_branch_name
    (2)(To rename in remote branch repo - If the branch has been pushed to the remote repository, you may want to update the remote branch name as well. Use the following command to delete the old remote branch and push the new one)
    < git push origin --delete [old_branch_name] > - ( Renaming a branch in Git does not create a copy of the branch, instead, it directly renames the existing branch. However, when it comes to the remote repository, Git maintains separate references for local and remote branches. 
    when you rename a branch locally using < git branch -m >, the remote repository still has a reference to the old branch name. 
    To update the remote reference and reflect the name change, you use < git push origin --delete [old_branch_name] > to delete the old branch on the remote repository, followed by git push origin [new_branch_name] to push the renamed branch)
    < git push origin <new_branch_name> > - command pushes the renamed branch to the remote repository with the new name.

16: Delete the branch
    (1)(To delete in local branch repo)
    < git checkout [other_branch] > - Before deleting the branch, switch to a branch other than the one you want to deleting. You cannot delete the branch you are currently on.
    < git branch -d [branch_name] > - Deletes the specified branch. If the branch has unmerged changes, Git will prevent the deletion,   and you will need to use "-D" to force the deletion. Or
    < git branch -D [branch_name] > - Forces the deletion of the specified branch, even if it has unmerged changes. Use this with caution, as it discards any changes in the branch.
    (2)(To delete in remote branch repo)
    < git push origin --delete [branch_name] > - To delete a remote branch
    (3)(remove any references to deleted branches from your local repository)
    < git fetch --prune > - command is used to update your local Git repository by fetching changes from the remote repository and pruning (deleting) any remote branches that no longer exist on the remote.
    (To delete a file, just push to branch after changes)

17: git log
    < git log > - command will display the commit history with the most recent commits listed at the top. You can use the arrow keys to navigate through the log, and press q to exit the log viewer.
    < git log --oneline > - will show each commit on a single line, displaying only the commit hash and the commit message.
    < git log [branch_name] > - commit history of a specific branch
    (limit the number of commits displayed or specify a range of commits)
    < git log -n 5 > - Show the last 5 commits
    < git log --oneline -n 5 > - will show last 5 commits on a single line,
    < git log [commit_hash]..HEAD > - Show commits from a specific commit to the latest

18: stash/Revert/Reset the branch
    -( < Git stash > is a command that is used to temporarily save and untrack your local changes that you have not staged yet.
    It is useful when you need to switch branches or work on another task but do not want to lose your uncommitted changes.
    < git stash > - will save your uncommitted changes to a stack and untrack them from your working directory. You can then switch branches or work on another task without having to worry about losing your changes.
    < git stash pop > - will restore your uncommitted changes to your working directory and re-track them.
    < git stash list > - will show you a list of all the stashed changes that you have made.)
    -( < git revert [commit_sha] > - command creates a new commit that undoes the changes introduced by the commit with the hash commit_sha, after running the git revert command, Git will open a text editor (such as Vim or the default text editor) for you to enter a commit message. This message typically describes the reason for the revert. ( type ~ :wq(write and quit) ),Save and close the editor, If there are conflicts during the revert process, Git will mark conflicted areas in the affected files. Manually resolve conflicts in each file marked by Git.) 
    -( < git revert [commit_sha] > - command in Git is a versatile command that is used to manipulate the commit history, move the branch pointer, and modify the staging area and working directory. There are different modes of git reset based on the options provided, they are: 
    < git reset --soft [commit_sha] > - Soft Reset: Moves branch pointer, keeps changes staged.
    < git reset [commit_sha] > - Mixed Reset: Moves branch pointer, unstages changes, keeps changes in working directory.
    < git reset --hard [commit_sha] > - Hard Reset: Moves branch pointer, discards changes in staging area and working directory.
    < git reset [file_name] >- Reset Specific File: Unstages changes for a specific file.)
    (revert vs reset: 
    Revert: Safely undoes changes, preserving commit history.
    Reset: Versatile command for moving the branch pointer, unstaging changes, or discarding changes. Requires caution, especially with --hard option.)    
    
```
