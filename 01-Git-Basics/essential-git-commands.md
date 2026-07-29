# Essential Git Commands

## Overview

Git commands allow developers to interact with repositories, track changes, manage versions, and collaborate with teams.

This section covers the fundamental Git commands used in everyday development workflows.

---

# 1. git init

## Purpose

`git init` creates a new Git repository in the current directory.

It initializes Git tracking for a project.

## Syntax

```bash
git init
```

## Example

```bash
mkdir Data-Analysis-Project

cd Data-Analysis-Project

git init
```

Output:

```
Initialized empty Git repository
```

After initialization, Git creates a hidden `.git` folder containing repository information.

---

# 2. git status

## Purpose

`git status` displays the current state of the repository.

It shows:

- Modified files
- New files
- Staged files
- Branch information

## Syntax

```bash
git status
```

Example:

```text
Untracked files:
    analysis.ipynb
```

---

# 3. git add

## Purpose

`git add` moves changes from the working directory to the staging area.

The staging area prepares changes before committing.

## Add a specific file

```bash
git add filename
```

Example:

```bash
git add README.md
```

## Add all changes

```bash
git add .
```

---

# 4. git commit

## Purpose

A commit saves staged changes permanently in the local repository.

Each commit represents a snapshot of the project.

## Syntax

```bash
git commit -m "commit message"
```

Example:

```bash
git commit -m "Add data cleaning script"
```

---

# 5. git log

## Purpose

`git log` displays the commit history of a repository.

It shows:

- Commit ID
- Author
- Date
- Commit message

## Syntax

```bash
git log
```

Compact view:

```bash
git log --oneline
```

Example:

```text
a83f91 Add Git introduction documentation
b29c12 Create repository structure
```

---

# 6. git branch

## Purpose

Branches allow developers to create separate versions of a project.

## View branches

```bash
git branch
```

## Create a branch

```bash
git branch feature-name
```

Example:

```bash
git branch dashboard-feature
```

---

# 7. git switch

## Purpose

Switch between branches.

## Syntax

```bash
git switch branch-name
```

Example:

```bash
git switch dashboard-feature
```

---

# 8. git clone

## Purpose

Creates a local copy of a remote repository.

Commonly used when downloading a GitHub repository.

## Syntax

```bash
git clone repository-url
```

Example:

```bash
git clone https://github.com/user/project.git
```

---

# 9. git remote

## Purpose

Manages connections between local and remote repositories.

## View remote connections

```bash
git remote -v
```

Example:

```text
origin https://github.com/user/project.git
```

---

# 10. git push

## Purpose

Uploads local commits to a remote repository such as GitHub.

## Syntax

```bash
git push origin branch-name
```

Example:

```bash
git push origin main
```

---

# 11. git pull

## Purpose

Downloads changes from a remote repository and integrates them into the local repository.

## Syntax

```bash
git pull
```

---

# Basic Git Workflow

The commonly used workflow:

```
Create/Edit Files

        ↓

git status

        ↓

git add .

        ↓

git commit -m "message"

        ↓

git push

        ↓

GitHub Repository Updated
```

---

# Git Command Summary

| Command | Purpose |
|---|---|
| git init | Create repository |
| git status | Check changes |
| git add | Stage changes |
| git commit | Save snapshot |
| git log | View history |
| git branch | Manage branches |
| git switch | Change branch |
| git clone | Copy repository |
| git remote | Manage remote |
| git push | Upload changes |
| git pull | Download changes |

---

# Interview Questions

## 1. What is the difference between git add and git commit?

`git add` moves changes to the staging area, while `git commit` permanently saves those staged changes in the local repository.

---

## 2. What does git status show?

It shows the current condition of the working directory and staging area.

---

## 3. What is a commit?

A commit is a snapshot of changes stored in the Git repository history.

---

## 4. Difference between git clone and git pull?

`git clone` creates a new local copy of a repository, while `git pull` updates an existing local repository.

---

# Next Topic

➡️ Understanding Git Workflow and Repository Architecture