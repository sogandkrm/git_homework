# Question 7.1 - git restore & git reset

## Initial state
- file.txt committed with content: Version 1

## git restore
- Modified file.txt to Version 2
- Used `git restore file.txt`
- Result: Working Directory returned to Version 1
- No new commit created

## git reset --soft
- Created commit "Version 2"
- Used `git reset --soft HEAD~1`
- Result:
  - Commit removed from history
  - Changes moved to staging area
  - Working Directory preserved

## git reset --mixed
- Executed after soft reset
- No effect because HEAD did not move
- Working Directory preserved

## git reset --hard
- Used `git reset --hard HEAD`
- Result:
  - Staging area cleared
  - Working Directory reset to last commit
  - Uncommitted changes removed
