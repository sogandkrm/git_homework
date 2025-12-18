# Revert vs Reset

In this section, the differences between `git revert` and `git reset` are explained
based on practical experiments performed in this homework.

---

## git reset

`git reset` is used to move the HEAD pointer to a previous commit.
Depending on the option used, it may also modify the staging area
and the working directory.

### Key characteristics:
- Can remove commits from history
- Can change the staging area and working directory
- Rewrites commit history
- Not safe for shared repositories

### Typical use cases:
- Undo local commits that have not been pushed
- Fix recent mistakes before sharing the repository

---

## git revert

`git revert` is used to undo the effect of a commit by creating a new commit.
It does not remove any commit from history.

### Key characteristics:
- Creates a new commit
- Preserves commit history
- Safe for shared repositories
- Can cause conflicts if file history is complex

### Typical use cases:
- Undo changes in public or shared repositories
- Safely revert commits that are already pushed

---

## Main differences

| Feature | git reset | git revert |
|------|----------|-----------|
| Removes commits | Yes | No |
| Creates new commit | No | Yes |
| Rewrites history | Yes | No |
| Safe for shared repos | No | Yes |
| Can cause conflicts | Rare | Possible |

---

## Conclusion

- `git reset` is powerful but dangerous when used on shared branches
- `git revert` is safer and preferred for undoing changes in public repositories
- Choosing the correct command depends on whether commit history must be preserved
