DAY 2 GIT

Assignment 1

Create a script to generate a merge conflict. 
```
#!/bin/bash
mkdir /home/vagrant/magic
cd /home/vagrant/magic
git init
touch a.txt
echo "Hi lovedeep" > a.txt
git add -A
git commit -m "1st master change"
git status
git branch slave
git checkout slave
echo "Hi anshu" > a.txt
git add -A
git commit -m "1st slave change"
git status
git checkout master
echo "Hi lovedeep!" > a.txt
git add -A
git commit -m "2nd master change"
git merge slave
```








Create muliple braches and push changes for each branch into remote repo. 
![Job DSL Plugin](https://github.com/lovedeepsh/multiplebranch/tree/slave1)
          

Create a script to clone remote repo and check out all existing remote branch. 
```
#!/bin/bash
git clone https://github.com/lovedeepsh/multiplebranch.git
cd multiplebranch
git branch -a
```

Clone a particular folder from a remote repo. 
```
# mkdir dd
# cd dd
# git init
# git remote add origin -f https://github.com/lovedeepsh/git.git
# git config core.sparsecheckout true
# echo "attendees/*" >> .git/info/sparse-checkout
# git pull origin master
# ls
```
 





Assignment 2

Use both https and ssh protocal to clone your remote repo. 
        Https
- Clone using http link.
- But while pushing you have to give ID and password.
        Ssh
- Clone using ssh link from remote repo.
- Save the idrsa_pub to github setting – ssh & gpt – add key
- While pushing you dont need any ID & password.

Change your working copy into a clonable remote repo
system1
```
# mkdir practice
# cd practice
# git init
(create ssh to system where you want to clone)
system2
# cd <path-where-you-want-to-clone>
# git clone ssh://username@ipaddress/path-of/remote-repo/practice
```
 
Use file system protocal in both local and remote mode(clone from another machine using file protocal) to clone your repo. 




Ignore backup, swp and pyc file from being commited. 
```
#  cd /path/local repo/
# touch .gitignore 
# git config --global core.excludesFile ~/.gitignore
# touch love.pyc  or *.pyc
# git add -A
# git commit -m “ignore try”
# echo love.pyc > .gitignore
# git rm - -cached love.pyc (removes the file from the local repo but stay in working directory)
# git commit -m “start ignoring”
# git status 
```

Now it will start ignoring the file.




Assignment 3

Add remote name parent for ot-training/git to your own repo. 
```
        # cd /home/vagrant/git
        # git remote add parent https://github.com/lovedeepsh/git.git
```
        
Check and verify two remotes.
```
# git remote -v
```

(Now you can push using parent name)




 
Git fetch changes from parent repo.
```
# git clone https://github.com/lovedeepsh/git.git
(After cloning, changes are being made)
# git fetch parent master 
```

Git merge changes into your branch.
```
# git merge parent/master
# ls
```
 
Git pull changes from parent repo.
```
 # git pull parent master
 # ls
```

Check for difference in fetch and pull also create a solutions.md file inside attendees/assignments/day2 with steps and snapshots. 
In the simplest terms, git pull does a git fetch followed by a git merge. You can do a git fetch at any time to update your remote-tracking branches under refs/remotes/<remote>/. This operation never changes any of your own local branches under refs/heads, and is safe to do without changing your working copy.
```
# cd /home/vagrant/git/attendees/assignments/day2/
# touch solutions.md
```








Assignment 4

Rename remote name from parent to main.
![Job DSL Plugin](https://github.com/lovedeepsh/git/blob/master/git%20day2%20images/Screenshot%20from%202018-05-29%2017-33-49.png)


Remove main remote. 
![Job DSL Plugin](https://github.com/lovedeepsh/git/blob/master/git%20day2%20images/Screenshot%20from%202018-05-29%2017-34-47.png)


Assignment 5
Save your solutions.md into your repo.
```
# git -a A
# git commit -m “saving solutions.md”
  (file solutions.md is saved in local repo)
```

Try to push solutions.md into parent repo.
https://github.com/lovedeepsh/git/tree/master/attendees/assignments/day2

Create a pull request from your repo to master of parent repo. 



Assignment6
Create tags in your repo. 
```
# git branch (your tag will be done on current branch)
# git tag tt (tt is the tag name)
```

Push tags into remote repo. 
```
# git push origin - -tags
Now you can check tags
```

Create tag on a one day old commit.
```
# git log (search for the commit of last day)
# git tag -a ld ba67a79e23f6d71794e24fad8d2a890b764114c8 -m "last day commit tag" 
```

Checkout to a tag. 
```
# git checkout ld
```

Clone a repo with tag name.
```
# git clone - -branch tt https://github.com/lovedeepsh/git.git
```

Clone a repo with specific branch (other than master) 
```
# git clone - -branch n https://github.com/lovedeepsh/git.git
```

Clone a repo on a specific commit. 
```
# git clone https://github.com/lovedeepsh/git.git <commitID>
```




Assignment 7
Create git alias for different commands 
```
# git config --global alias.pu push
# git config --global alias.a add
# git config --global alias.l log
# git config --global alias.c commit
# git config --global alias.st status
# git config –list
```

Share your aliases in attendees/assignments/day2/alias.md
https://github.com/lovedeepsh/git/tree/master/attendees/assignments/day2 



Assignment 8
A developer is working on a feature on a branch, unfortunately he/she made a wrong commit. How would he/she recover from this situation without cleaning the working directory.
```
# git log 
# git checkout <commit-of-last-version>
```

You are working on a branch of a project. After modification, you thought that these modifications are quite less important but will work on later and for the time being, you should do some other implementation on the project using other branch. Is there any way to save your previous state of modification and get back it when required?
Yes there is a very usefull command for saving a previous state of modification and get back it when recquired by using “git stash” function:-
For saving
```
# git stash save “any-message-you-want”
For retrieving
# git stash apply <index-no.-of-stash-saved>
or
# git stash pop (This will pop out the last stash)
```

 
Try to list all the cases, where you can use checkout in GIT. 
List of cases where we can use checkout in GIT :-
- git checkout -b <new-branch> 
This will make a new branch and also checkout in it.
- git checkout <branchname>
This will checkout in already created branch.
- git checkout - -orphan <newbranch>
This will create an orphan branch. The changes commit to this branch will have no parents and it will start a new history.
- git checkout <commit-ID>
This will checkout to the specific commit.  


make a script in which you will pass a git repo path and it will generate a html report of last 5 days commits. html report should contain
commit message
commit ID
author name
Commit Date 
Script:-
``` 
#!/bin/bash
mkdir gittest
cd gittest
sudo git clone https://github.com/apache/hadoop.git -y
sudo chmod 777 hadoop
cd  hadoop
sudo git log –since=”5 days” --pretty=format:’%cd,                                  %an,%B,%cm’ > log.csv
cat log.csv
```
