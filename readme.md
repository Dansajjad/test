#this is a test file 

I will be using this repo to play with git & github. Mostly testing commands.
This will also serve as a document to store and shortcuts that I need to remember, which I do not use often. 

##Setting up a new SSH Key
* https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/

##Adding a new SSH key to your GitHub account 
* https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/


##Misc comments
* to open gedit from termial: gedit . fileName


##Setting up a new git folder & linking with github


 push an existing repository from the command line

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
** Password for 'https://dansajjad@github.com': 
** Branch master set up to track remote branch master from origin.
* ibm@ibm:~/Documents/test$ git status
** On branch master
** Your branch is up-to-date with 'origin/master'.

