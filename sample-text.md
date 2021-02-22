## What is the difference between push, pull, and fetch?

## git push
The command `git push` uploads commits from your local repository to a remote repo.

 `git push` checks to see whether your local branch is tracking a remote branch. If it is, your local changes are pushed to the remote branch. Pushing is how you transfer commits from your local repository to a remote repo. This will fail if the remote branch has diverged from your local branch (for example, if the remote branch contains commits that are not in your local branch). When this happens, your local branch needs to be synchronized with the remote branch using `git pull` or the combination of `git fetch` and `git merge`.

## git fetch
The command `git fetch` downloads commits from a remote repo into your local repo.

`git fetch` looks for commits in the remote branch that your current branch is tracking and downlads them to your local repo. It does not merge these commits, so your local branch remains unchanged. `git merge` will incorporate the changes into your current branch

## git pull
The command `git pull` downloads and merges commits from a remote repo into your local repo.

`git pull` actually runs `git fetch` followed immediately by `git merge`. Merging remote upstream changes into your local repository is a common task, but it assumes that you understand the changes you are merging into your local branch.
