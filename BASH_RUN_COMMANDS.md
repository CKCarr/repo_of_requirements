# BASH RUN COMMANDS
##### my `~/.bashrc` cheatsheet

Personalize Bash shell 
and set
ALIASES for environments
make sure to run source  on the ~/.bashrc<br> and if still not working try restarting terminal before troubleshooting further.

```
step 1.  update file
vim ~/.bashrc
step 2. (add to bottom)
alias alias_name='script or command to replace with alias'
step 3. run on command line to update the bash environment.
source ~/.bashrc
```
***
To change the current directory to your home directory when a new interactive shell session is started.
set ~ as your cwd in ~/.bashrc

```vim ~/.bashrc```<br>
add the command<br>

```cd ~ ```
<br>
I just add all my personal setting to bottom of file to find easier.<br>
After saving and Exiting file run the following on the command line,<br>
to update the environment to your new specifications

```source ~/.bashrc```

***
### Python3 alias

create an alias to avoid typing python3 each time you want to run a Python script. 

```
vim ~/.bashrc

alias py='python3'

source ~/.bashrc
```

***
### Pycodestyle alias

```
get apt-install pycodestyle
```

```
vim ~/.bashrc
alias pycs="pycodestyle"
source ~/.bashrc
```

***
### Bash Script: Git Add, Commit, Push 
For Github : add, commit, push - alias

~/scripts/gacp.sh

I make a directory called ~/scripts
for bash scripts and save this in that folder

I create bash file for git commit add push
(my example filename and script)

gacp.sh 

```
#!/bin/bash

# Prompt for the commit message
read -p "Enter commit message: " commit_message

# Add all changes to the staging area
git add .

# Show the commit message
echo "Commit Message: $commit_message"

# Confirm the commit
read -p "Press enter to confirm the commit or Ctrl+C to cancel"

# Commit changes with the provided commit message
git commit -m "$commit_message"

# Push changes to the specified branch
git push
```


I then go on to add an alias for this script to be ran globally.

```
vim ~/.bashrc
alias gacp="bash ~/scripts/gacp.sh"
source ~/.bashrc
```

***
for w3c_validator
clone repo to root folder

```
git clone https://github.com/holbertonschool/W3C-Validator.git
```
add alias

```
vim ~/.bashrc

alias w3c='python3 ~/W3C-Validator/w3c_validator.py'

source ~/.bashrc
```
