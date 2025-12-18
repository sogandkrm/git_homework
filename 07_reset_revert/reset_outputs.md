# Reset outputs (Question 7.1)

## After git reset --soft HEAD~1

### git log --oneline
```text
f328a21 (HEAD -> master) Version 1
```

### git status
```text
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   file.txt

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   file.txt
```

---

## After git reset --mixed HEAD~1

### git log --oneline
```text
f328a21 (HEAD -> master) Version 1
```

### git status
```text
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   file.txt

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   file.txt
```

---

## After git reset --hard HEAD

### git log --oneline
```text
f328a21 (HEAD -> master) Version 1
```

### git status
```text
On branch master
nothing to commit, working tree clean
```
