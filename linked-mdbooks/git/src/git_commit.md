# Commits

### 2-step process
1. adding changes to **staging area**
```bash
git status            # shows changes made on local machine
git diff <filename>   # displays all changes of a modified file

# adding files or full directory to "staging area"
git add <file>
git add .

# removing files from "staging area"
git rm --cached <file>

# commits changes (that were added staging area) to current branch
git commit -m 'commit message'
```

2. **commiting** changes in staging area to current branch
```bash
# commits changes (that were added staging area) to current branch
git commit -m 'commit message'
```

### Overview: log of all Commits and Branches
```bash
# complete (long) format
git log
```
```bash
# pretty format
git log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit --date=relative
```