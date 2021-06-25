DAY 3 GIT

Assignment 1

Create account on each
1. Github 
2. Gitlab 
3. Bitbucket
 
 Try to findout key features and major differences between all.
1. Github
A social repository for open source code projects that use Git for source code versions control. 
This host site is a distributed file version management systems. 
Linus Torvalds created this project for Linux kernel development control. 
Such projects like Chromium, jQuery, PHP, MediaWiki etc. use Git. 
This free software is released under GNU GPL license version 2.
Apart from being a good tool, GitHub is a large educational source.
Key features
-Bug tracking
-Find your project easily
-Meet new developers
-Share your experience
-Coordinate your projects together
-Integrated code search
-High compatibility

       





2. GitLab
Developed on the basis of Git version control system, GitLab is one of the best web platforms for hosting project source codes. 
Although GitLab is similar to GitHub in terms of functionality, it seems to be a better choice for teamwork than its famous counterpart and GitLab features may be different somewhat.
GitLab exists in two forms. 
The first one is SAAS - website with open registration, and the second one is an individual solution GitLab Community Edition. 
They both can be perfectly customized to any service.
Key Features
-Free service
-Open source code repository
-Free hosting
-Bug tracking mechanism
-Files editing in the web interface
-LDAP integration


      3. BitBucket
It can be called as a real worthy competitor to GitHub. 
You just need to create to register on the official website and then you can create your personal account. 
In fact, it is based on a source code management mechanism. 
You can simultaneously use the code with integrated comments, and also make requests, manage and share your Git repositories. 
It is possible to create a flexible deployment model for any team. 
Moreover, you can get access to private and public repositories without any difficulties.
Key Features
-Free for small teams
-Query management system
-Authentication via GitHub
-Integrated JIRA tool
-Repositories importing


Assignment 2

Check for organization and repository level permission for team and users over repositories and branches.
When you create a repository, you specify wheather its private or public. If your repository is public, anyone can access it. If your repository is private, you can grant access to individuals and groups of users.
        a) Organization level permissions for team and users over repositories and branches :-
There are three types of repository permissions available on organization level i.e. read, write & admin.

Assignment 3

Create a test repo in your github account, write some demo commits. 
```
# mkdir test
# git clone https://github.com/lovedeepsh/test.git
# cd git
# touch a.txt
# echo “Hi” > a.txt
# git add -A
# git commit -m “demo commit”
# git push origin master
```

Add this test repo as submodule inside your git repo.
```
# git submodule add https://github.com/lovedeepsh/multiplebranch.git
( Multibranch@commitid cloned and .gitmodule added.) 
# git status
( Multibranch@commitid and .gitmodule untracked)
#git add -A
#git commit -m “.gitmodule added” 
# git push origin master
```



Clone git repo with submodule. 
```
            # mkdir test2
            # git clone https://github.com/lovedeepsh/test.git
            # cd git
            (First you will se a black multibranch folder)
            # git submodule update - -init
            (git is being cloned through sub module)
```            
