# Branches and Merges

```bash
# branches
git branch                    # shows all branches
git checkout -b <newBranch>   # creates new branch and moves into it
git checkout <existingBranch> # switches to an existing branch

# merge branch 
git checkout master        # switch to master branch
git pull origin master     # pull data from remote (to be up to date)
git merge branchToMerge    # master <- branchToMerge        
git push origin master     # push updated masterbranch to remote

# discarding all changes that show up with "git status"
git checkout .          # forgot -> ??
git checkout <file>     # forgot -> ??
```