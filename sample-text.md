## What is the difference between `git push`, `git pull`, and `git fetch`?

## git push
The command `git push` uploads commits from your local repository to a remote repo.

 `git push` checks to see whether your local branch is tracking a remote branch and, if that is the case, pushes your local changes to the remote branch. Pushing is how you transfer commits from your local repository to a remote repo. This will fail if the remote branch has diverged from your local branch (e.g., if the remote branch contains commits that are not in your local branch). When this happens, your local branch must be synchronized with the remote branch using `git pull` or the combination of `git fetch` and `git merge`.

## git fetch
The command `git fetch` downloads commits from a remote repo into your local repo.


`git fetch` looks for commits in the remote branch that your current branch is tracking and downlads them to your local repo. It does not merge these commits, so your local branch remains unchanged. When you understand and are comfortable with the changes, `git merge` will incorporate them into your current branch

## git pull
The command `git pull` downloads and merges commits from a remote repo into your local repo.

`git pull` actually runs `git fetch` followed immediately by `git merge`. Merging remote upstream changes into your local repository is a common task, but `git pull` assumes that you understand the changes you are merging into your local branch. 