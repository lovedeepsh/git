DAY 1 GIT

Assignment 1
Q - 
Initialize a directory as git repository. 
Create a blank files like a.txt, b.txt. 
Write "Hi Team Ninja" into a.txt 
Write "This is VCS:Git" into b.txt 
Set git config variables. 
Commit both files. 
Create a branch ninja 
Switch into branch ninja 
Update file b.txt with ""This is VCS:Git. This is ninja branch" 
Check for the difference made in the file. 
Commit your changes in ninja branch. 
Check difference between last two commits. 
Rename your file b.txt to c.txt 
Commit your changes. 
Remove file c.txt. 
Commit your changes. 
Create a file text.txt and add it. 
Remove it from the staging area. 

A - 
# mkdir test
# cd test
# git init
# ls -al
# touch a.txt b.txt
# echo “Hi Team Ninja” > a.txt
# echo “This is VCS:Git” > b.txt
# git config - -global user.name “lovedeepsh”
# git config - -global user.email lovedeeps789@gmail.com
# git add -A
# git status
# git commit -m “1st assignment”
# git log
# git branch ninja
# git checkout ninja
# echo “This is VCS:Git. This is ninja branch” > b.txt
# git diff
# git status
# git add -A
# git commit -m “2nd commt”
# git log
# git diff 2a7465..3fc7527
# mv b.txt c.txt
# git add -A
# git status
# git commit -m “rename b.txt c.txt”
# git log
# rm c.txt
# git add -A
# git commit -m “deleted file c.txt”
# git log
# touch text.txt
# git add text.txt
# git reset HEAD text.txt

Final output of my git log

commit 079f9e4c70bef7c0ae79c54e907f10398b29f071
Author: lovedeepsh <lovedeeps789@gmail.com>
Date:   Mon May 28 05:34:46 2018 +0000

    deleted file c.txt

commit 848ddb49bf038ad7e5dff89ed7aec9687b7281de
Author: lovedeepsh <lovedeeps789@gmail.com>
Date:   Mon May 28 05:33:32 2018 +0000

    rename b.txt c.txt

commit 3fc7527f10a31535990180ad8dde915dd4b9abaf
Author: lovedeepsh <lovedeeps789@gmail.com>
Date:   Mon May 28 05:26:50 2018 +0000

    2nd commt

commit 2a74650487db7ec25bb6826573aa232a490213ea
Author: lovedeepsh <lovedeeps789@gmail.com>
Date:   Mon May 28 05:20:18 2018 +0000

    1st assignment
:



Assignment 2
Q -
Create a account on github.com. 
Fork ot-training/gitrepo into your account. 
Clone your repo into your machine. 

A - 
=> Account created on github.com and the ssh key also been added to account for secure push.
=> Forked by clicking on the Fork button on the extreme right. And got it as lovedeepsh/jenkins.
=> cloned the lovedeepsh/jenkins repo in vagrant.
# mkdir forkgit
# cd forkgit
# git clone https://github.com/lovedeepsh/git.git







Assignment 3
Q -
Clone your repo into your machine. 
Add a file to the attendees directory that describes you (ex. filename wouild be your name like saurabh.vajpayee.txt). 
Commit your changes. Write a meaningful message like "Added information about YOUR NAME HERE." 
Save your changes into remote repo. 
Check list of changes in your repo. 
Add your name into attendees/assignments/day1/attendees.md 

A -
=> Repo cloned by me in forkjen directory
```
# cd forkjen
# git clone https://github.com/lovedeepsh/jenkins.git
```

=> 
```
     # cd git
     # touch lovedeep.txt
     # git add lovedeep.txt
     # git commit -m “Added Information about LOVEDEEP SHARMA”
     # git log
```
=>
```
     # git push origin master
```

output :- username - *******
                password - *******

=> 
```
# git diff f1ff55..ece6e8
```

output :- 
diff --git a/attendees/lovedeep.txt b/attendees/lovedeep.txt
new file mode 100644
index 0000000..e69de29
Therefore a file name lovedeep.txt added in attendees directory in the repo.

=> 
```
# cd /forkget/git/attendees/assignments/day1
# cat “LOVEDEEP SHARMA” > attendees.md
# git add -A
# git commit -m “Added my name in attendees.md file”
# git push origin master
```
