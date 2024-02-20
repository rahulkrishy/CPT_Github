// Git & GitHub

step 1: Install Git - version control software. (https://git-scm.com/downloads)

step 2: Sign up to Github - remote(online) software development platform, it's used for storing, tracking, and collaborating on software projects. (https://github.com/)

step 3: To check git software is installed on your device, open terminal and type " git ", it will pop up list of feature available on it, it not redownload it properly

step 4: Next we need to configure our github account username and email to device, 
open terminal and type " git config --global user.name "username" " and 
" git config --global user.email "Email Id" "

step 5: Click Create a "new repository" in Github and name it, then copy the repository https url 
(A 'Git repository' is a virtual storage of your project. It allows you to save versions of your code, which you can access when needed.)

step 6: Open device terminal (*or Vscode editor), and type " git clone repository_Url " to clone repository, if done then we will see " .git " folder in hidden views option in the our local directory
(Don't do any modification to .git folder, its the link between our local and remote(online) repositories)  

step 7: Once the repository is cloned, create a project file and follow below steps to push from your local repository to remote(online) GitHub repository 
(from local to remote(online): add(staging)->commit->push, from remote(online) to local: pull)

step 8: " git add <file> " - command adds a file change in the working directory to the staging area 'or 
        " git add . "      - command adds all files change in the working directory to the staging area.
(git add doesn't really affect the repository in any significant way—changes are not actually recorded until you run git commit)
(" git status " to view the state of the working directory and the staging area)

step 9: " git commit " - command captures a snapshot of the project's currently staged changes 'or
        " git commit -m "message/comment" *filename " - command commits with message for filename(*filename is optional to include)

step 10: " git push " - command is used to upload local repository content to a remote repository

step 11: (To get lastest file from the remote repo to our local repo)
         use " git pull " - command is used to fetch and download content from a remote repository and immediately update the local repository to match that content (git pull = git fetch + git merge)

step 12: Git merge conflicts
(Version control systems are all about managing contributions between multiple distributed authors (usually developers).
Sometimes multiple developers may try to edit the same content. 
If Developer A tries to edit code that Developer B is editing a conflict may occur.)

(ex: Conflicts generally arise when two people have changed the same lines in a file, or if one developer deleted a file while another developer was modifying it. In these cases, Git cannot automatically determine what is correct. Conflicts only affect the developer conducting the merge, the rest of the team is unaware of the conflict. Git will mark the file as being conflicted and halt the merging process. It is then the developers' responsibility to resolve the conflict.The most direct way to resolve a merge conflict is to manually edit the conflicted file.)

(" git diff " - command helps find differences between states of a repository/files. This is useful in predicting and preventing merge conflicts)

step 13: Git Branching and merging
"git branch" is a new/separate version of the main repository.
(Branches allow you to work on different parts of a project without impacting the main branch.
When the work is complete, a branch can be merged with the main project.
You can even switch between branches and work on different projects without them interfering with each other.)

" git branch " - List all of the branches in your repository.
" git checkout -b <branch> " - Create a new branch called ＜branch＞
" git checkout <branch> " - Switch between branches ＜branch＞

// newBranch edits





