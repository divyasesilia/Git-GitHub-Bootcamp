# Merging Branches

## Overview

Merging is the process of combining changes from one branch into another branch.

In a professional development workflow, developers usually create separate branches for features or fixes and merge them into the main branch after completion and review.

---

# What is Git Merge?

`git merge` combines the commit history and changes from one branch into the current branch.

Example:

Before merge:

```
main

A---B---C


feature-dashboard

A---B---C---D---E
```

After merge:

```
main

A---B---C-------M
             /   
            D---E

```

The changes from the feature branch become part of the main branch.

---

# Why Merge Branches?

Merging helps teams:

- Combine completed features
- Maintain stable main branches
- Collaborate safely
- Track development history
- Integrate different work streams

---

# Basic Merge Workflow

Professional workflow:

```
Create Feature Branch

        ↓

Develop Feature

        ↓

Commit Changes

        ↓

Switch to Main Branch

        ↓

Merge Feature Branch

        ↓

Push Updated Main Branch
```

---

# Switching to Target Branch

Before merging, move to the branch where changes should be added.

Example:

```bash
git switch main
```

---

# Merging a Branch

## Syntax

```bash
git merge branch-name
```

Example:

```bash
git merge feature-dashboard
```

This merges the `feature-dashboard` branch into the current branch.

---

# Example Workflow

Create a feature branch:

```bash
git switch -c feature-dashboard
```

Make changes:

```
Add dashboard charts
Add KPI cards
```

Commit:

```bash
git commit -m "Add dashboard features"
```

Switch back:

```bash
git switch main
```

Merge:

```bash
git merge feature-dashboard
```

---

# Types of Git Merge

Git mainly performs two types of merges:

1. Fast-forward merge
2. Three-way merge

---

# Fast-Forward Merge

## Definition

A fast-forward merge happens when the main branch has no new commits after the feature branch was created.

Example:

Before:

```
main

A---B


feature

A---B---C---D
```

After:

```
main

A---B---C---D
```

Git simply moves the main branch pointer forward.

---

## Example

```bash
git merge feature-dashboard
```

Output:

```
Fast-forward
```

---

# Three-Way Merge

## Definition

A three-way merge happens when both branches have new commits.

Example:

Before:

```
        C---D
       /
A---B
       \
        E---F
```

Git creates a new merge commit:

```
        C---D
       /     \
A---B          M
       \     /
        E---F
```

---

# Merge Commit

A merge commit combines two different development histories.

Example:

```bash
git commit -m "Merge feature branch"
```

The merge commit records when branches were combined.

---

# Checking Merge History

Command:

```bash
git log --oneline --graph
```

Example:

```
*   Merge feature-dashboard
|\
| * Add dashboard chart
| * Add KPI cards
|
* Initial project setup
```

---

# Resolving Merge Conflicts

A merge conflict occurs when Git cannot automatically decide which changes to keep.

Example:

Two developers modify the same line:

```
Developer A:
Total Sales Calculation


Developer B:
Sales Revenue Calculation
```

Git needs human decision.

---

# Merge Conflict Workflow

When conflict occurs:

1. Open conflicting file
2. Review changes
3. Choose correct version
4. Save file
5. Add changes

Command:

```bash
git add filename
```

Complete merge:

```bash
git commit -m "Resolve merge conflict"
```

---

# Abort a Merge

If you want to cancel a merge:

```bash
git merge --abort
```

This returns the repository to the previous state.

---

# Merge Best Practices

## Pull Latest Changes Before Merge

Before merging:

```bash
git pull
```

This reduces conflicts.

---

## Merge Small Changes

Small branches are easier to review and merge.

Good:

```
feature-add-sales-chart
```

Avoid:

```
complete-application-update
```

---

## Write Clear Commit Messages

Good:

```
Merge customer analysis feature
```

Avoid:

```
merge
```

---

# Merge Example in Data Analytics Projects

A data team may work with branches:

```
Sales Dashboard Project

main

 |
 |
 ├── feature-sales-analysis
 |
 ├── feature-profit-report
 |
 └── docs-update
```

After completion:

```
feature-sales-analysis

        ↓

Merge

        ↓

main
```

---

# Interview Questions

## 1. What is Git merge?

Git merge combines changes from one branch into another branch.

---

## 2. What is a fast-forward merge?

A fast-forward merge occurs when Git can move the branch pointer forward because no conflicting changes exist.

---

## 3. What is a merge conflict?

A merge conflict happens when Git cannot automatically combine changes from different branches.

---

## 4. How do you resolve a merge conflict?

Review conflicting files, select the correct changes, add the file, and commit the resolution.

---

## 5. Difference between branch and merge?

A branch creates an independent development path, while merge combines branch changes together.

---

# Key Takeaways

- Merge combines changes from different branches.
- Feature branches are merged into main after completion.
- Fast-forward merges happen when histories are linear.
- Three-way merges combine different development paths.
- Merge conflicts require manual resolution.

---

# Next Topic

➡️ Merge Conflicts