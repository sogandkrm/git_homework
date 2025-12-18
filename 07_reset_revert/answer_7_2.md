# Answer 7.2 – Git Revert

In this exercise, the behavior of `git revert` was tested using multiple commits
and different revert strategies. The goal was to understand how revert works,
how it differs from reset, and how conflicts can occur during revert.

---

## Initial commits

A file named `file.txt` was created and updated incrementally:

- Commit 1: Add line 1
- Commit 2: Add line 2
- Commit 3: Add line 3

At this point, the file content was:
```
Line 1
Line 2
Line 3
```

---

## Revert last commit (git revert HEAD)

The command `git revert HEAD` was used to revert the last commit (`Add line 3`).

Result:
- A new commit was created: `Revert "Add line 3"`
- Commit history was preserved
- `Line 3` was removed from the file

File content after revert:
```
Line 1
Line 2
```

---

## Revert using commit hash (safe method)

The commit `Add line 2` was reverted using its commit hash:

```bash
git revert <commit-hash>
```

Result:
- A new commit was created: `Revert "Add line 2"`
- Only `Line 1` remained in the file
- This method was safe and unambiguous

File content:
```
Line 1
```

---

## Revert using HEAD~n (educational case)

The command `git revert HEAD~1` was used to revert a previous revert commit.

This caused a conflict because:
- The file state had changed significantly
- Git could not automatically decide which lines to restore

Conflict markers appeared in `file.txt`.

---

## Resolving revert conflict

The conflict was resolved manually by editing `file.txt` and keeping the desired
content:

```
Line 1
Line 3
```

After removing conflict markers, the file was staged and committed:

```bash
git add file.txt
git commit -m "Resolve conflict after revert with HEAD~1"
```

---

## Conclusion

- `git revert` creates a new commit and does not rewrite history
- It is safe to use in shared repositories
- Reverting by commit hash is the safest approach
- Reverting with `HEAD~n` can be risky and may cause conflicts
- Conflicts during revert must be resolved manually and committed