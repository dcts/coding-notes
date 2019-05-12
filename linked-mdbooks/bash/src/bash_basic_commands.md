# Basic Commands

```bash
# access system variables (date & time)
date          # current date and time
cal           # calendar of the current month

# free space & processes
free -h       # RAM space -h short for --human (better readibility)
df -h         # DISC space -h short for --human (better readibility)
ps            # all running processes
ps faux       # all running processes (more detail)

# get help
man <command>  # manual (help) for <command>

# outputting strings (to console)
echo                    # prints to console (can take multiple parameters)
echo "hello World!"     # outputs message to console
echo 'hello World!'     # same (single or double quotes)
echo hello World!       # same (no quotes at all -> takes multiple inputs)
eval                    # evaluates the command first and outputtes result as string
```

```bash
which COMMAND   # shows the path to a given command
which java      # shows path where command "java" is stored
```

```bash
sudo            # use sudo befor calling a command when admin rights are needed
```

```bash
# create aliases (own small programms)
# store aliases in .bash_aliases file to load them on each start of the terminal
alias sayHello="echo 'hello World!'";  # hello World programm
alias goToHome="cd ~";                 # unneccessary but possible

```

```bash
# RUN PROZESSES IN BACKGROUND!
CTRL-z
bg
CTRL+D / exit
```
