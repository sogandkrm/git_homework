# GitHub Collaboration and Pull Behavior

This document explains basic collaboration concepts in GitHub, including
adding collaborators, differences between `git fetch` and `git pull`,
pull behavior configuration, and best practices for writing a good README.

---

## Adding a collaborator on GitHub

A collaborator is another GitHub user who is granted access to a repository.

### Steps to add a collaborator:
1. Go to the repository on GitHub
2. Click on **Settings**
3. Open **Collaborators**
4. Click **Add people**
5. Enter the GitHub username or email
6. Send invitation and wait for acceptance

After accepting the invitation, the collaborator can clone, pull, push,
and contribute to the repository based on the given permissions.

---

## Difference between git fetch and git pull

### git fetch
- Downloads changes from the remote repository
- Does NOT modify the working directory
- Does NOT merge changes automatically
- Safe to use for checking updates

Example:
```bash
git fetch origin
```

### git pull
- Downloads changes from the remote repository
- Automatically merges changes into the current branch
- May cause merge conflicts

Example:
```bash
git pull origin main
```

### Summary
- `git fetch` = download only
- `git pull` = download + merge

---

## Pull behavior configuration

Git allows configuring how `git pull` behaves.

### Default merge behavior
```bash
git config --global pull.rebase false
```

### Rebase instead of merge
```bash
git config --global pull.rebase true
```

### Fast-forward only
```bash
git config --global pull.ff only
```

Choosing the correct pull behavior helps avoid unnecessary merge commits
and keeps the commit history clean.

---

## How to write a better README

A good README should include:
- Project title
- Short description
- Installation steps
- Usage instructions
- Contribution guidelines
- License information

README files help collaborators and users understand the project quickly
and improve overall collaboration.