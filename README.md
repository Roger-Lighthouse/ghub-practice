
git config user.name >> returns user name
git config user.password >> returns user password
git config user.email >> returns user email


HEAD-snapshot of your last commit from the working directory

git diff HEAD >> After pulling from orgin master use this command to check differences from last commit(HEAD pointer)
==========================================================
git diff >> looks at changes in your file vs changes in HEAD/latest pull ??
git diff --staged >> looks at changes in staging area vs changes in HEAD/latest pull??

git reset <file> >> removes file from staging area

==========================================================

git log --oneline >> shows log with commit message only

eg.   dgjs63g  added feature A
      7efghef  tested with client
      dey64gf  added function B

to view changes in 'added function B'

rm git checkout dey64gf >> Go To That Entire File

git checkout <file> >> Get Rid Of All Changes Since Last Commit For <file> and replace file with HEAD version.

to go back to master >> git checkout master

git revert <commit>  >> undoes a committed snapshot by undoing the changes AND ADDING A NEW COMMIT.

USE git revert HEAD. after  bad commit, new commit with changes that restore HEAD.

git reset <commit> >> actually goes back to a commit by removing all subsequent commits.
[DANGEROUS]

==========================================================

git branch >> lists all branches and highlights current branch

git branch <new_branch> >> create branch new branch called new_branch
git checkout -b <new_branch>. >> create new branch and switch to it

git checkout new_branch >> get on that branch

[[Do something on that branch eg. git rm '*.txt' AND commit those changes]]

git checkout master >> get back on master branch

git pull >> update your local repo with any remote changes

Before MERGING Option:
git diff <source_branch> <target_branch>

git merge <new_branch> >> merge branch new_branch to master branch

If conflict arises, edit the affected files AND add them again using:
git add <filename>

git branch -d new_branch  >> delete branch new_branch

git push origin <branch_you_want_push>


==========================================================

Fork Repository will copy the fork to your account...automatically

git clone <url of forked repository on your github>  >> clones repository to local machine from your github

git remote add upstream <url of original repository>  >> remote connection to original repository

git remote  >> names of remote repositories

git remote -v  >> view remote repositories and info

===========================================================

Drop local changes and get fresh copy from server

git fetch origin

git reset --hard origin/master

===========================================================

Questions:
1) When creating a branch and working on a file is it one file but each branch stores changes.
2) push remote origin master (Here the master is the branch name on github repo?)
3) when creating a local new branch, and I push this branch(aa-branch) using push origin aa-branch does it updqte master branch on remore rep because this branch branched off the master?