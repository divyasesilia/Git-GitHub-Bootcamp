# Git Reset and Revert

## Overview

Git provides multiple ways to undo changes.

Two important commands are:

- `git reset`
- `git revert`

Although both can undo changes, they work differently.

Understanding when to use each command is important for maintaining a clean and safe project history.

---

# Git Reset

## What is Git Reset?

`git reset` moves the current branch pointer (HEAD) to another commit.

It can modify:

- Commit history
- Staging area
- Working directory

Reset is mainly used for local changes.

---

# Git Reset Syntax

```bash
git reset commit-id
```

Example:

```bash
git reset abc1234
```

This moves the branch back to the specified commit.

---

# Types of Git Reset

Git provides three reset modes:

1. Soft Reset
2. Mixed Reset
3. Hard Reset

---

# 1. Git Reset --soft

## Purpose

Soft reset moves HEAD backward but keeps changes staged.

Command:

```bash
git reset --soft HEAD~1
```

Example:

Before:

```
A---B---C
        ^
       HEAD
```

After:

```
A---B
    |
    Changes from C remain staged
```

Use case:

You want to edit the previous commit message or combine commits.

---

# 2. Git Reset --mixed

## Purpose

Mixed reset removes changes from staging but keeps them in the working directory.

Command:

```bash
git reset HEAD~1
```

This is the default reset mode.

Example:

Before:

```
Commit
   |
   File staged
```

After:

```
Commit removed

File remains modified
```

---

# 3. Git Reset --hard

## Purpose

Hard reset removes commits and deletes associated changes.

Command:

```bash
git reset --hard HEAD~1
```

Example:

Before:

```
A---B---C
        ^
       HEAD
```

After:

```
A---B
```

Commit C and its changes are removed.

---

# Warning About Hard Reset

`git reset --hard` can permanently delete changes.

Use carefully.

Avoid using it on shared branches.

---

# Git Revert

## What is Git Revert?

`git revert` creates a new commit that reverses the changes introduced by an earlier commit.

Unlike reset, revert does not delete history.

---

# Git Revert Syntax

```bash
git revert commit-id
```

Example:

```bash
git revert abc1234
```

Git creates a new commit:

```
A---B---C---D

D = Reversal of C
```

---

# Reset vs Revert

| Git Reset | Git Revert |
|---|---|
| Removes or moves commits | Creates a new reversing commit |
| Changes history | Preserves history |
| Mainly for local work | Safe for shared branches |
| Can delete changes | Keeps complete history |

---

# When to Use Git Reset

Use reset when:

- Working locally
- Cleaning unfinished commits
- Removing recent commits before pushing
- Reorganizing commit history

Example:

You created unnecessary commits:

```
Add file

Fix typo

Fix another typo
```

You can reset and create a cleaner commit.

---

# When to Use Git Revert

Use revert when:

- Changes are already pushed
- Working with a team
- You need a safe undo operation

Example:

A production change caused an issue.

Instead of deleting history:

```bash
git revert commit-id
```

creates a new commit undoing the problem.

---

# Real-World Team Example

A developer pushes a feature:

```
Commit A
Commit B
Commit C
```

Commit C introduces a bug.

For a shared repository:

Recommended:

```bash
git revert Commit-C
```

Result:

```
Commit A
Commit B
Commit C
Commit D (undo C)
```

The history remains visible.

---

# Data Analytics Example

A Data Analyst updates a SQL analysis:

```
Commit 1:
Add sales queries

Commit 2:
Update customer analysis

Commit 3:
Incorrect calculation logic
```

If changes are local:

```bash
git reset --hard HEAD~1
```

may remove the incorrect commit.

If already shared:

```bash
git revert HEAD
```

creates a safe correction.

---

# Checking Commit History

Before undoing changes, review history:

```bash
git log --oneline
```

Example:

```
a123 Add dashboard
b456 Update SQL queries
c789 Initial setup
```

---

# Best Practices

## Prefer Revert for Shared Branches

Especially:

- main branch
- production branches
- team repositories

---

## Use Reset Carefully

Especially:

```bash
git reset --hard
```

because changes can be lost.

---

## Review Before Undoing

Always check:

```bash
git log
```

before changing history.

---

# Common Commands Summary

| Command | Purpose |
|---|---|
| git reset --soft | Undo commit, keep staged changes |
| git reset | Undo commit, keep files modified |
| git reset --hard | Remove commit and changes |
| git revert | Create undo commit |
| git log | View commit history |

---

# Interview Questions

## 1. Difference between git reset and git revert?

`git reset` changes existing history, while `git revert` creates a new commit that reverses changes.

---

## 2. Which is safer for shared branches?

`git revert` is safer because it preserves history.

---

## 3. What does git reset --hard do?

It moves HEAD backward and removes associated changes permanently.

---

## 4. When should you use git reset?

For local changes before sharing commits with others.

---

# Key Takeaways

- Reset modifies existing history.
- Revert safely creates an undo commit.
- Use reset mainly for local cleanup.
- Use revert for shared repositories.
- Understand the difference before undoing changes.

---

# Next Topic

➡️ Git Tags and Releases