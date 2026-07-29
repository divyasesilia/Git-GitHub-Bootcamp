# Git Stash

## Overview

Git stash is a Git feature that temporarily stores uncommitted changes and returns the working directory to a clean state.

It allows developers to save incomplete work without creating unnecessary commits.

Git stash is useful when a developer needs to:

- Switch branches quickly
- Handle urgent fixes
- Pull latest changes
- Temporarily remove unfinished modifications

---

# What is Git Stash?

`git stash` takes modified tracked files and stores them in a temporary area called the stash.

The changes are removed from the working directory, allowing the developer to continue with a clean project state.

Example:

Before stash:

```
Working Directory

Modified Files

├── analysis.py
├── dashboard.sql
└── report.md
```

After stash:

```
Working Directory

Clean

Stash Storage

├── analysis.py changes
├── dashboard.sql changes
└── report.md changes
```

---

# Why Use Git Stash?

Git stash helps when:

- Work is incomplete
- A quick branch switch is required
- An urgent bug fix needs attention
- Changes are not ready for a commit

---

# Basic Git Stash Workflow

```
Make Changes

      ↓

Stash Changes

      ↓

Switch Branch

      ↓

Complete Required Work

      ↓

Restore Stashed Changes
```

---

# Creating a Stash

Command:

```bash
git stash
```

Example:

```bash
git stash
```

Output:

```
Saved working directory and index state
```

The current changes are temporarily stored.

---

# Checking Stashed Changes

Command:

```bash
git stash list
```

Example:

```
stash@{0}: WIP on main: Update dashboard analysis
stash@{1}: WIP on feature branch
```

`stash@{0}` represents the latest stash.

---

# Applying Stashed Changes

The `git stash apply` command restores changes without removing them from the stash list.

Command:

```bash
git stash apply
```

Example:

```
Restore latest stashed changes
```

---

# Applying a Specific Stash

Command:

```bash
git stash apply stash@{number}
```

Example:

```bash
git stash apply stash@{1}
```

---

# Popping Stashed Changes

`git stash pop` restores changes and removes them from the stash list.

Command:

```bash
git stash pop
```

Difference:

| Command | Result |
|---|---|
| git stash apply | Restores changes, keeps stash |
| git stash pop | Restores changes, removes stash |

---

# Removing a Stash

To delete a specific stash:

```bash
git stash drop stash@{number}
```

Example:

```bash
git stash drop stash@{0}
```

---

# Clearing All Stashes

Command:

```bash
git stash clear
```

This permanently removes all stored stashes.

---

# Real-World Developer Example

A developer is working on a new feature:

```
feature-dashboard
```

Changes are incomplete:

```
Add new charts
Update calculations
```

Suddenly an urgent bug appears in production.

The developer needs to switch branches:

```bash
git switch main
```

But changes are incomplete.

Solution:

```bash
git stash
```

Now the developer can fix the issue safely.

After returning:

```bash
git stash pop
```

The unfinished work is restored.

---

# Git Stash Example for Data Analysts

A Data Analyst is updating:

```
Sales Analysis Project

├── SQL queries
├── Python notebook
└── Dashboard documentation
```

Before finishing, a critical report update is requested.

Instead of committing unfinished analysis:

```bash
git stash
```

The analyst can work on the urgent task and later restore the analysis.

---

# Stash with Message

A meaningful stash message improves organization.

Command:

```bash
git stash push -m "Working on sales dashboard"
```

View:

```bash
git stash list
```

Example:

```
stash@{0}: Working on sales dashboard
```

---

# Important Notes

## Stash is Temporary

Stash is not a replacement for commits.

Use commits for:

- Completed work
- Important milestones
- Project history

Use stash for:

- Temporary unfinished changes

---

# Best Practices

## Use Clear Messages

Good:

```
git stash push -m "Update customer analysis"
```

Avoid:

```
git stash
```

when managing many stashes.

---

## Do Not Keep Stashes Forever

Restore or remove old stashes regularly.

---

# Interview Questions

## 1. What is git stash?

Git stash temporarily stores uncommitted changes and cleans the working directory.

---

## 2. Difference between git stash apply and git stash pop?

`git stash apply` restores changes while keeping the stash, whereas `git stash pop` restores changes and removes the stash.

---

## 3. When should you use git stash?

When you need to temporarily save unfinished changes before switching branches or performing another Git operation.

---

## 4. Is git stash a replacement for commit?

No. Commits permanently save project history, while stash is only temporary storage.

---

# Key Takeaways

- Git stash temporarily stores unfinished changes.
- It helps switch branches safely.
- `stash apply` restores changes without deletion.
- `stash pop` restores and removes changes.
- Commits should be used for permanent project history.

---

# Next Topic

➡️ Git Rebase