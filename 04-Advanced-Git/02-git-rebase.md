# Git Rebase

## Overview

Git rebase is a Git operation used to integrate changes from one branch onto another branch by moving or replaying commits.

Rebase helps create a cleaner and more linear project history compared to traditional merging.

It is commonly used by development teams to keep commit history organized before merging changes into the main branch.

---

# What is Git Rebase?

Rebase takes commits from one branch and applies them on top of another branch.

Example:

Before rebase:

```
main

A---B---C


feature

A---B---D---E
```

After rebasing feature onto main:

```
main

A---B---C

        \
         D'---E'
```

The feature commits are recreated on top of the latest main branch.

---

# Why Use Rebase?

Rebase helps teams:

- Maintain clean commit history
- Avoid unnecessary merge commits
- Organize development work
- Prepare branches before merging
- Make project history easier to understand

---

# Merge vs Rebase

| Merge | Rebase |
|---|---|
| Combines branch histories | Replays commits on another branch |
| Creates merge commits | Creates linear history |
| Preserves original history | Rewrites commit history |
| Safer for shared branches | Better for local branches |

---

# Git Merge Example

Before merge:

```
main

A---B---C


feature

A---B---D---E
```

After merge:

```
A---B---C------M
        \     /
         D---E
```

A new merge commit is created.

---

# Git Rebase Example

Before rebase:

```
main

A---B---C


feature

A---B---D---E
```

Command:

```bash
git rebase main
```

After:

```
A---B---C---D'---E'
```

The history becomes linear.

---

# Basic Rebase Workflow

Professional workflow:

```
Update Main Branch

        ↓

Create Feature Branch

        ↓

Develop Changes

        ↓

Rebase Feature Branch

        ↓

Resolve Conflicts

        ↓

Merge Feature
```

---

# Starting a Rebase

First switch to the branch you want to update.

Example:

```bash
git switch feature-dashboard
```

Then:

```bash
git rebase main
```

Git applies the feature commits on top of the latest main branch.

---

# Rebase Conflict Resolution

Rebase conflicts can happen when Git cannot automatically apply changes.

Example:

```
CONFLICT (content): Merge conflict
```

Steps:

### 1. Check Status

```bash
git status
```

---

### 2. Resolve the File

Open the conflicted file and choose the correct changes.

---

### 3. Stage the Resolution

```bash
git add filename
```

---

### 4. Continue Rebase

```bash
git rebase --continue
```

---

# Abort a Rebase

If you want to cancel a rebase:

```bash
git rebase --abort
```

This returns the repository to the state before the rebase started.

---

# Interactive Rebase

Interactive rebase allows developers to edit commit history.

Command:

```bash
git rebase -i HEAD~n
```

Example:

```bash
git rebase -i HEAD~3
```

This allows editing the last three commits.

---

# Squashing Commits

Squashing combines multiple commits into one cleaner commit.

Before:

```
Commit 1:
Add dashboard

Commit 2:
Fix dashboard layout

Commit 3:
Update dashboard chart
```

After squash:

```
Commit:
Complete dashboard implementation
```

Benefits:

- Cleaner history
- Easier review
- Better project documentation

---

# When to Use Rebase

Use rebase for:

✅ Personal feature branches  
✅ Cleaning local commit history  
✅ Preparing changes before merge  
✅ Keeping development history simple  

---

# When NOT to Use Rebase

Avoid rebasing:

❌ Public shared branches  
❌ Production branches  
❌ Commits already used by other developers  

Reason:

Rebase changes commit history.

---

# Real-World Team Example

A developer is working on:

```
feature-sales-dashboard
```

Meanwhile, another developer updates:

```
main
```

Before merging:

Update feature branch:

```bash
git rebase main
```

Now the feature branch contains the latest main changes and can be merged cleanly.

---

# Git Rebase Example for Data Analysts

A data analytics team works on:

```
Sales Analysis Project

main

 |
 |
 └── feature-customer-analysis
```

The analyst creates several commits:

```
Add customer query

Fix SQL calculation

Update visualization
```

Before submitting the work, interactive rebase can combine these into:

```
Complete customer analysis
```

This creates a cleaner project history.

---

# Important Rule

Never rewrite history that other team members are already using.

Good:

```
Local feature branch
```

Avoid:

```
Shared main branch
```

---

# Common Rebase Commands

| Command | Purpose |
|---|---|
| git rebase main | Rebase current branch onto main |
| git rebase --continue | Continue after conflict resolution |
| git rebase --abort | Cancel rebase |
| git rebase -i | Interactive rebase |

---

# Interview Questions

## 1. What is Git rebase?

Git rebase moves or reapplies commits from one branch onto another branch to create a cleaner history.

---

## 2. Difference between merge and rebase?

Merge combines histories and creates a merge commit, while rebase rewrites commits to create a linear history.

---

## 3. Why is rebase considered risky?

Because it rewrites commit history and can affect other developers if used on shared branches.

---

## 4. When should you use rebase?

Use rebase mainly on local feature branches before merging changes.

---

# Key Takeaways

- Rebase creates cleaner commit history.
- Rebase replays commits on top of another branch.
- Interactive rebase helps organize commits.
- Avoid rebasing shared branches.
- Understanding rebase is important for professional Git workflows.

---

# Next Topic

➡️ Git Reset and Revert