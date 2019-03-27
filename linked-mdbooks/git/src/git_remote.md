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

# PULL REQUEST = Code Review
# -> via GitHub?
```