# Revert outputs (Question 7.2)

This file shows the output of `git log` before and after performing `git revert`
commands during the exercise.

---

## Git log before revert

The commit history before performing any revert operation was:

```text
40eb235 (HEAD -> master) Add line 3
3467130 Add line 2
11902a5 Add line 1
```

---

## Git log after revert operations

After executing the following revert operations:
- `git revert HEAD`
- `git revert <commit-hash>` (Add line 2)
- `git revert HEAD~1` and resolving conflict

The commit history became:

```text
e64ecf9 Resolve conflict after revert with HEAD~1
11f41ec Reapply "Add line 3"
67e121d Revert "Add line 2"
08a7b6d Revert "Add line 3"
40eb235 Add line 3
3467130 Add line 2
11902a5 Add line 1
```

---

## Final file content

The final content of `file.txt` after all revert operations was:

```text
Line 1
Line 3
```