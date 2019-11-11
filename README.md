# Fixing Common Git Mistakes Notes

My notes after taking Chris Achard's workshop on [Fixing Common Git Mistakes](https://github.com/chrisachard/fixing-git-mistakes).

Files can be in different states:

- Working directory for making changes to files

- Your remote repo 

- Stashing to save things for later

You have full features of git on your computer. In the staging index, we usually clean up our commits here. 

`Git stash` is used to save things for later

`Git status` shows the state of working area and staging area

`Git log` shows us the history of our commits with hashes

`Git branch` —vv shows which branches are tracked

`git log —oneline` great way to see concise

`HEAD` is just a special name for a pointer to a branch or to a commit. git checkout {HEAD} is a detached head pointing to a specific commit, not something that automatically updates. Be careful because you can lose changes when using this. 

`git branch` shows which branch we are on and which ones we have.

When we `git push` and get `fatal—current branch has no upstream`, this just means that we need to set our upstream and tell GitHub to make ea new branch. 

Git will often tell you what to do when you get stuck

`git branch -d` deletes a branch locally, but deleting a branch in git doesn’t necessarily mean you’ll get rid of it. You also need to tell GitHub to delete the branch:

`git push -delete origin first-branch`

Deleting a branch in git doesn’t necessarily mean you’ll get rid of it.

`Git ref log —all` shows all the action we’ve taken on all our branches. 

When we want to push another change to our file in the same commit:

`git commit -amend -no-edit` 

`git log —oneline -graph` to show a diagram of our commits/history

Kinds of resets in git: 

- Soft goes from commit tree to staging. You can move your commit back, change it and push it again. 

- Mixed moves it back to the working directory.

- Hard: back to working directory, resetting changes

`git remote prune origin` lists branches that can be deleted

`git cherry pick` can be used to get any commit and move it to the top of any branch you’re putting it on. 

`Git rebase and reflog` are the magical commands that allow you to re-write anything you want.
