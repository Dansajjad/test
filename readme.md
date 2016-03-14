#this is a test file

I will be using this repo to play with git & github. Mostly testing commands.
This will also serve as a document to store and shortcuts that I need to remember, which I do not use often.

##Setting up a new SSH Key
* https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/

##Adding a new SSH key to your GitHub account
* https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/


##Misc comments
* to open gedit from termial: **gedit . fileName**
* exit git log file by typing: **q**


##Setting up a new git folder & linking with github
###Create a new repo on the command line
* echo "# test" >> README.md
* git init
* git add README.md
* git commit -m "first commit"

* git remote add origin https://github.com/Dansajjad/test.git
* git push -u origin master
* git remote add origin https://github.com/Dansajjad/test.git
* git push -u origin master

* Username for 'https://github.com': enter Username
* Password for 'https://dan.sajjad@gmail.com@github.com':

* ibm@ibm:~/Documents/test$ git add .
* ibm@ibm:~/Documents/test$ git commit -m "updated readme to describe purpose"
* ibm@ibm:~/Documents/test$ git status
* ibm@ibm:~/Documents/test$ git push -u origin master
* Username for 'https://github.com': enter Username
> Password for 'https://dansajjad@github.com':
> Branch master set up to track remote branch master from origin.
* ibm@ibm:~/Documents/test$ git status
> On branch master
> Your branch is up-to-date with 'origin/master'.
###Markdown quick reference
* http://www.darkcoding.net/software/markdown-quick-reference/

###Working with my Main Projects folder
####Adding and updating a subfolder
* create a folder using mkdir
* "git add" this folder (add a readme also, maybe git doesn't add empty folder')
* "git commit -m 'message'"
* "git push"

#### Other Git Tips:
* You have a great deal of control over exactly what the log command displays. I like the one line format:
>git log --pretty=oneline
* There are a lot of options for selecting which entries are displayed in the log. Play around with the following options:
> git log --pretty=oneline --max-count=2
> git log --pretty=oneline --since='5 minutes ago'
> git log --pretty=oneline --until='5 minutes ago'
> git log --pretty=oneline --author=<your name>
> git log --pretty=oneline --all

* Over time, I’ve decided that I like the following log format for most of my work.
> git log --pretty=format:'%h %ad | %s%d [%an]' --graph --date=short

Let’s look at it in detail:

--pretty="..." defines the format of the output.
%h is the abbreviated hash of the commit
%d are any decorations on that commit (e.g. branch heads or tags)
%ad is the author date
%s is the comment
%an is the author name
--graph informs git to display the commit tree in an ASCII graph layout
--date=short keeps the date format nice and short


* Here’s what I use to review the changes made in the last week. I’ll add --author=jim if I only want to see changes I made.
> git log --all --pretty=format:'%h %cd %s (%an)' --since='7 days ago'

* Both gitx (for Macs) and gitk (any platform) are useful in exploring log history.










##Git notes from codecademy
###Basic workflow
Use Git commands to help keep track of changes made to a project:
* **git init**: creates a new Git repository
* **git status**: inspects the contents of the working directory and staging area
* **git add**: adds files from the working directory to the staging area
* **git diff**: shows the difference between the working directory and the staging area
* **git commit**: permanently stores file changes from the staging area in the repository
* **git commit -a -m "commit message"**: shortcut to add & commit
* **git log**: shows a list of all previous commits

###Backtrack
You've learned three different ways to backtrack in Git. You can use these skills to undo changes made to your Git project.
Let's take a moment to review the new commands:
* **git checkout HEAD filename**: Discards changes in the working directory.
* **git reset HEAD filename**: Unstages file changes in the staging area.
* **git reset SHA**: Can be used to reset to a previous commit in your commit history.
* **git add filename_1 filename_2**: a way to add multiple files to the staging area with a single command

###Git branching
Git branching allows users to experiment with different versions of a project by checking out separate branches to work on.
The following commands are useful in the Git branch workflow.
* **git branch**: Lists all a Git project's branches.
* **git branch branch_name**: Creates a new branch.
* **git checkout branch_name**: Used to switch from one branch to another.
* **git checkout -b branch_name**: shortcut to create new branch and switch to new branch
* **git merge branch_name**: Used to join file changes from one branch to another.
* **git branch -d branch_name**: Deletes the branch specified.
###Git teamwork
In order to collaborate, you and randy need:
* A complete replica of the project on your own computers
* A way to keep track of and review each other's work
* Access to a definitive project version

Now that you've merged origin/master into your local master branch, you're ready to contribute some work of your own. The workflow for Git collaborations typically follows this order:
* Fetch and merge changes from the remote
* Create a branch to work on a new project feature
* Develop the feature on your branch and commit your work
* Fetch and merge from the remote again (in case new commits were made while you were working)
* Push your branch up to the remote for review
* Steps 1 and 4 are a safeguard against merge conflicts, which occur when two branches contain file changes that cannot be merged with the git merge command.
A remote is a Git repository that lives outside your Git project folder. Remotes can live on the web, on a shared network or even in a separate folder on your local computer.
The Git Collaborative Workflow are steps that enable smooth project development when multiple collaborators are working on the same Git project.
We also learned the following commands
* **git clone remote_location clone_name**: Creates a local copy of a remote.
* **git remote -v**: Lists a Git project's remotes.
* **git fetch**: Fetches work from the remote into the local copy. Fetch any new changes Sally may have made to the remote.
* **git merge origin/master**: Merges origin/master into your local branch. Even though Sally's new commits have been fetched to your local copy of the Git project, those commits are on the origin/master branch. Your local master branch has not been updated yet, so you can't view or make changes to any of the work she has added.
* **git push origin branch_name**: Pushes a local branch to the origin remote. Sally can now review your new work and can merge it into the remote's master branch.
* **git push -u origin branch_name**: shortcut -For every branch that is up to date or successfully pushed, add upstream (tracking) reference

###The seven rules of a great git commit message
* Separate subject from body with a blank line
* Limit the subject line to 50 characters
* Capitalize the subject line
* Do not end the subject line with a period
* Use the imperative mood in the subject line
* Wrap the body at 72 characters
* Use the body to explain what and why vs. how
