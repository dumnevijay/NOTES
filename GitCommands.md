
In this file i am writing about my learnings from the seven hours master class from youtube, here i will write commands and their uses using git bash

> ls -l 	 is used to know the total number of files present in the folder in the git bash.
> nano filename.txt 	 is used to create a file in git bash.
> ctrl+x 	to save changes.
> y to say yes 	to changes made in the file.
> git init  	is used to initialize git which creates .git folder in the current working folder.
> ls -a  	is used to see the hidden files such as .git is a hidden folder.
> ls -al  	is used list all files including hidden folders also.
> the files start with .foldername are the hidden folders or files.
> git add filename 	is used to add file from non staging area to stagging area.
> git commit 	from this the git track the files.
> after git commit a new file will open 
> use i  to get in to insert mode then enter your commit message
> then to come out use :wq  where w stands for write and q stands for quite from that mode
> touch filename.extension is also used to create new file in terminal
> rm -rf .git/	 is used to remove the .git folder from the folder.
> git init --initial-branch=main     is used to change default name from master to main or we can use any name.
> mkdir foldername 		is used to create a directory or folder.
dont create mutliple git init  for nested folders also have only one git init where the need is there to track files.
git dont track empty folders mainly used to track files.
to track a folder we must have a file in the empty folder.
> git status -v   where v stands for verbose means detailed information.
> git status -s   where s stands for short means short information.
> touch f1.txt f2.txt f3.txt   multiple files have created in single line.
in git status -s  if get op as A then  A stands for added.
> git add . 	is used to add all files in single command.
> git rm --cached f1.txt f2.txt f3.txt   is used to bring files from stagging area to non stagging area. multiple files to non stagging area in single line.
when ever we commit the commit object will be created. it has 4 informations like name, when(time), commit message, snapshot files in stagging area.  to create snapshot git uses encryption uses SHA1(Secure Hashing Algorithm 1) to create 40 character alpha numeric number as commit id.

head always pointer to the latest commit if we want explicitly we can change it.
> git commit -a -m "message"   is used to commit without stagging area this is only for the tracking files not for untracked files.
> git commit --amend    is used to add to existing commit and to save and edit to the existing commit or last commit.
> git commit --amend --no-edit   is used to add file to the existing commit with changing its message.
> git commit -s -m "message"      this is used to sign off or to create new commit object without having any connection with existing commit flow.
> git commit --allow-empty -m "dummy message"   this is used for empty commit for checking fo ci cd of a project.
> git log -n 2    is used to see the recet last 2 commits
> git log --pretty=short   this is used to see logs in short form.
> git log --pretty=full  this is used to see logs in full format.
> git log -p   is used to see in detailed format what has been modified and all changes will appear.
> git log --pretty=oneline   to see all logs in oneline format.
> git log --pretty=format:"%h"   is used to see the only hash codes of all logs.
> git log --pretty=format:"%h %s"    is used to see only hash codes and messages only.
> git log --pretty=format:"%h %s %ae %an"   is used to see only hash codes , messages , author email and author name.
> git log --since="1 week ago"  or "yesterday"  or "one month ago"      is used to see the past log with specified time.
> git log --since="2024-06-16" --until="2024-06-17"  is used to see the commits in between this duration of time.
> git log --author="authorname"   this show all commits of the specific author.
> git log --grep="Modified"   this show the commits which have the mentioned word present in the message of commits.

> git checkout hashcode of commit     is used to go back to particular status of files at that particular moment of commit.
> git commit -m "subject" -m "explanation"    is used to have subject and its explanation(body).

GIT RESET  1. unstage  2.undo  3. discard  (git reset modes soft, mixed and hard).
> git reset --soft hashcode   changes bring to stagging area.
> git reset --mixed hashcode   changes bring to non stagging area which default when we use only git reset without any attribute.
> git reset --hard  hashcode    changes made after this particular commit are going to delete completely, and we need write it again.

UNDOING COMMITS WITH GIT REVERT

> git revert last log hashcode      is used to undo the last commit changes.


Branches

we can create branch inside a branch
> git branch   is used to show all branchs.
> git branch branchname    is used to create new branch.
> git checkout branchname      is used to go into that branch.
> git branch -d branchname       is used to delete the branch.
ever branch name should be unique.

UNDERSTANDING REVISITING BRANCH

> while writing commands u can use tab to auto fill the names ex fe tab to feature. like that.

UNDERSTANDING GIT MERGING 

> git master merge branch   is used to merge the branch into master.

GIT MERGING SCENARIO

conflict will raise when two or more developers work on the same file.

HOW TO USE CHERRY PICK

> git cherry-pick commit hashcode        is used to create copy to commit in master without using merge.

git remote
> git remote add origin https://gitlab.com/git-study-group-vijay/TestAutomationFranmework.git
> git remote   is used to see the whether remote connection is there are not.
> git remote -v    is used to see the remote connection with detailed links.
> git push -u origin master      is used frist time -u is used to create master branch at remote repository.
> git push     will used from second time which directly push changes to particular repository.
> git branch -r    to see all remote branchs.

> git fetch   is used to get remote files changes in all branches  to origin/master  from them we need to merge  it to master branch using   git merge origin/master  try to avoid to use it
> git fetch origin master    this will bring only changes made in origin master in remote repo to master offline repo   try to use this.
> git fetch --all   is used to get all changes different repos at time like gitlab, github etc.
> git pull    is used to get remote files to directly to the master branch.( git pull is combination of git fetch and git merge  avoid to using it as it will raise conflict so use git fetch check all changes the merge them to master.)

git stashing
> git stash  is used to temporarly save changes this is used when will incomplete any feature in code but immediately need to work on other branch then we use to as temporary commit like featrue
> git stash list   to see list of stachs.
> git stash apply stash@{id}   is used to work from the last left work without any perminent commit.
> git stash clear    to clear the stash.

.gitIgnore 
>create a .gitignore  file in that use *.extension or filenaem.extension or folder/ to avoid from tracking.

> git fetch --prune   is used to delete the origin branchs which are deleted on remote repo will also deleted in offline repo with single command.

> git diff (to compare working with the satgging)
