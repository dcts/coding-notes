# Remote (pull, fetch, rebase, push)

```bash
# connect to remote
git remote add origin <githublink>  # connects to remote (which we call "origin" here)
git remote -v                       # check connection to remote

# pull from remote before pushing
# -> in case someone commited changes to the remotes
#    master while you were working on your local repo
git remote -v  # check if connected right
git pull       # pull lates without destroying local changes

# push local changes to master
git push origin master

# pull branch from remote (only works if you have one remote)
# show all branches that are on the remote
git branch -r

# - pull branch "test" from remote
git fetch # fetches all branches from remote (not saved as branches locally yet)
git checkout test # saves the branch test from the remote and makes it locally availible

# PULL REQUEST = Code Review
# -> via GitHub?
```
