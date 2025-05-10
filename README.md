# important git commands


------- GIT CHECKOUT ----------- switch, create, specific commit or file
IMP NOTE: use checkout command cautionly as it modifies the state of branch (discards uncommited changes while switching)
    git checkout -b "feature_1" ->  switch to brnach, if not present then create and switch

------ GIT BRANCH --------------
NOTE: 
1. git branch -> show current branch
3. git add . OR git add <filename> -> add file to staging area
4. git branch -d <branch_name> -> delete the merged branch, -D deletes non merged branch

------- GIT COMMIT ----------
NOTE: adding file to local repo
    git commit -m "fix-for -dropdown"

------- GIT PUSH ----------
NOTE: pushing changes in local repo to remote repo
    git push <remote repo name> <branch name>
    git push origin master

------- GIT PULL ----------
NOTE: pulls changes from remote to local repo as well as to working dir

------- GIT FETCH ----------
NOTE: pulls changes from remote to local repo
    git fetch upstream
-------- GIT MERGE ---------
NOTE: 
    git merge origin/master

Merge feature-branch into main
    git merge feature-branch

-------- GIT STASH ---------------
NOTE: git stash save the changes temporarily to working dir, helpful when want to switch branch but not ready for commit yet
    
        git stash
        git stash save "message"
        git stash list
        git stash apply stahs@{2} -> apply specific stash to working dir
        git statch drop - > 

------- add a remote and push ---------
    git remote add origin https://github.com/yourusername/git-project.git 
    git branch -M main git push -u origin main

---------  Check Git Remotes ------------
    git remote -v

-------- git RESET and REVERSE ---------
    Completely Remove the Last Commit
        git reset --hard HEAD~1   --hard -> Removes the commit and discards changes.
        git reset --soft HEAD~1   --soft -> want to undo the commit but keep the changes.

-------- # Revert a specific commit by hash -----------
    git revert d3f3c12

-------- Git REBASE ----------
git rebase is a command that moves or combines commits from one branch onto another, rewriting commit history in a linear way.

-------- git LOG ------------
View Recent Commits
    git log --oneline -n 5

    