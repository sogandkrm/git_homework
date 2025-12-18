# Reset types explanation (Question 7.1)

In this exercise, different types of `git reset` were tested to understand
their effect on commits, staging area, and working directory.

## git reset --soft
- Moves HEAD to the specified commit
- Removes commits from history
- Keeps changes in the staging area
- Working directory is not changed

Use case:
When a commit message or commit structure is wrong, but changes should be kept.

## git reset --mixed
- Moves HEAD to the specified commit
- Clears the staging area
- Keeps changes in the working directory

Use case:
When commits should be removed and changes reviewed again before staging.

## git reset --hard
- Moves HEAD to the specified commit
- Clears the staging area
- Resets working directory to the commit state
- All uncommitted changes are lost

Use case:
When changes are not needed and should be permanently discarded.
