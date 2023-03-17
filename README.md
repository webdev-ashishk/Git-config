# Git-Tips-and-Tricks
inside the Git
# How to delete a Git repository
## Steps to delete a local Git repo
1. Open the the local Git repo’s root folder
1. Delete all of the files and folder in the Git repo’s root folder
1. Delete the hidden .git folder with File Explorer or through the command line
1. Run a git status command. A fatal: not a git repository error verifies that the Git repo is deleted

## Command line Git repository delete

If you’re familiar with the terminal window or the DOS prompt, you can easily perform a command line Git repository delete. Just run the rm command with the -f and -r switch to recursively remove the .git folder and all of the files and folders it contains.

This Git repo remove command also allows you to delete the Git repo while allowing all of the other files and folder to remain untouched.

```
rm -fr .git

```

# You have Diveregent branches and need to specify problem in Git
Git push origin master not working 
```
steps
1. git pull --ff-only
2. git pull origin master
```
git push oring master working
