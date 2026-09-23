# Git Tutorial

In this repo, you will find a tutorial on basic usage of Git and Github. By the end you will hopefully be able to 
- Create a Git repo
- Stage and commit changes
- Synchronise those changes with Github
- Undo changes
- Create and use branches
- Stash unsaved changes

# Cheat Sheet


## `git init` 
Initialise a local repo in the current working folder

## `git status`
Determine the current state of your working branch. Determine if there are any changes to stage, commit, merge conflicts, etc.

## `git add`
Adds files to your staging area. This will stage the current version of the file, regardless if you change it after adding it. Rerun this command to update files in your staging area. 

## `git commit -m "Message"`
Commits your changes from the staging area permanently into your git history. Message should be added to give developers information as to what the changes were in this commit without having to read the actual changes in the code. Aim for 20-50 characters long.

## `git push`
Push changes from your local repo out to github

## `git pull`
Pull changes from github into your local repo

`git pull origin main` will pull changes from github's main branch into your current branch. Good for synchronising everything.


## `git fetch`
Retrieves information of any changes from Github but doesn't apply them yet. Basically checks if you're up to date or not.

## `git log`
See commit history. To see a condensed version, `git log --oneline`

## `git diff`
Shows the difference between the current state of your repo to the committed state of the repo

## `git diff --staged`
Shows the difference between the staged version of your repo to the committed state of the repo

## `git restore <filename>`
Restores file `<filename>` to the latest commit, undoing all changes that may have happened since then

## `git reset <hash>`
Restores current branch to the commit referenced by `<hash>`. \

To reset to most recent commit, `git reset HEAD`. 

To reset to nth most recent commit, `git reset HEAD~n`

To reset to most recent commit and destroy all changes since then, `git reset --hard HEAD` (useful if conflicts are getting in the way of resets)

## `git revert <HASH>`
Creates a new commit that undoes the commit performed with commit ID `<HASH>`

## `git branch <branchname>`
Creates a new branch `branchname`. Note that this does NOT switch to the branch, that has to be done seperately.

To create a branch and switch to it immediately, use `git checkout -b <branchname>`

## `git checkout <branchname>`
Switches to a different branch `branchname`

## `git merge <branchname>`
Merges changes from `<branchname>` into current working branch. Generally used to merge branches into `main`, however usage is similar to merge from Github.

e.g. If updates to main on github haven't been downloaded locally yet,
```
git fetch
git merge
```
will pull the external changes locally. These two commands are equivalent to `git pull`


