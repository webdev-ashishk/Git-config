# Git-Tips-and-Tricks

# Configure Git   
```
git config --global user.name "your_username"
```
```
git config --global user.email "your_email_address@example.com"
```
```
git config --global --list
```

### Don't write every time userName and Password 
#### Write user & password first time and along with this write below code that specify when timerout expires
---
```
git config --global credential.helper "cache --timeout=86400"

```








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
# Divergent branch problem <First solution>
### You have divergent branches and need to specify how to reconcile them
```
1. git pull --ff-only
```
```
2. git pull origin master
```
Your code uploaded to github
# Divergent branch problem <Second solution>
### when Previous solution not working then Use This technique

1. click Code copy HTTPS LINKS
2. Run
```
   git clone <HTTPS LINK>
```
3. Paste Your previous file Which not uploading to github
4. 
```
   git push origin master
```
Your code uploaded to github

# How to visit(Traverse) previous commits
#### list of previous commits and show #code's
```
git log --oneline
```
```
git checkout <#code>
```
# How to Revert to a Previous Commit Using the git reset command
### git reset works with local repository

#### list of previous commits and show #code's
```
git log --oneline
```
##### undo the previous commit 
```
git reset <#code> --hard
```
### git revert works with online repository
``` 
git revert <#code>
```
# How to Rename Branch
##### list of branch
```
git branch
```
##### Rename branch
```
git branch -m <oldBranchName> <newBranchName>
```

# How to Rename Previous commit 
```
git commit --amend -m "New commit message."

```
# Fix issue
## Solve any issue in Git You must run this command after every command to see What going on
```
git status
```

---
   
# github CLI setup
```
 sudo apt install gh
```
```
gh auth login
```





   * https://youtu.be/8Iljd2rZEIA

---
# Giving permission to github CLI delete the repo
```
 gh auth refresh -h github.com -s delete_repo
```
---
## Create a repo at one click
```
gh repo new/create <repo name> --public
                               --private
                               --internal
                               
```

## Delete a repo at one click
```
gh repo delete <repo name> --confirm
```

## Rename a repo
```
gh repo rename <new-repo-name>
```


---
# Most used github shortcuts
![most used github shortcut](https://user-images.githubusercontent.com/127021921/232833458-b2ebde14-f48b-4e8e-bb48-0f7331ae221e.png)


---
 # When something change remote but not present locally and wanted to push my code to remote then this proble occurs
   ## First solution 
   ```
   git push origin master -f
   ```
   
   ![Screenshot from 2023-05-19 22-49-22](https://github.com/webdev-ashishk/Git-info/assets/127021921/04a620d2-1a70-46fc-8ebd-d3580a16f7f0)

   ## Second Solution(recomended)
   ```
   git pull origin master
   git push origin master
   ```

---
   
