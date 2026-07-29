# Creating and Switching Branches

## Overview

Branch creation and branch switching are fundamental Git operations used in software development workflows.

Developers create separate branches for features, bug fixes, and experiments, then switch between branches depending on the task they are working on.

---

# Checking Current Branch

Before creating or switching branches, it is important to know the current branch.

Command:

```bash
git branch
```

Example output:

```text
* main
  feature-dashboard
```

The `*` symbol indicates the currently active branch.

---

# Creating a New Branch

## Purpose

The `git branch` command creates a new branch without switching to it.

## Syntax

```bash
git branch branch-name
```

## Example

```bash
git branch feature-dashboard
```

This creates:

```
main
 |
 └── feature-dashboard
```

The user is still on the original branch.

---

# Creating and Switching to a Branch

The modern Git command for creating and immediately moving to a new branch is:

```bash
git switch -c branch-name
```

Example:

```bash
git switch -c feature-dashboard
```

This performs two actions:

1. Creates the branch
2. Switches to the new branch

---

# Switching Between Existing Branches

## Command

```bash
git switch branch-name
```

Example:

```bash
git switch main
```

Now the active branch changes to:

```
main
```

---

# Older Command: git checkout

Before `git switch` was introduced, developers commonly used:

```bash
git checkout branch-name
```

Example:

```bash
git checkout feature-dashboard
```

`git checkout` can still be used, but `git switch` provides a clearer command specifically for branch movement.

---

# Branch Workflow Example

Imagine an Ecommerce Dashboard project.

Main branch:

```
main
```

A new dashboard feature is required.

Create branch:

```bash
git switch -c feature-dashboard
```

Work happens here:

```
main

 |

 └── feature-dashboard
        |
        |
     Add charts
     Update KPIs
     Improve visuals
```

After completion, the branch can be merged back into main.

---

# Listing All Branches

Command:

```bash
git branch
```

Example:

```
main
feature-dashboard
bug-fix-sales
```

---

# Deleting a Branch

After merging, unused branches can be removed.

## Safe Delete

```bash
git branch -d branch-name
```

Example:

```bash
git branch -d feature-dashboard
```

---

## Force Delete

```bash
git branch -D branch-name
```

Used when a branch contains unmerged changes.

---

# Renaming a Branch

Command:

```bash
git branch -m new-name
```

Example:

```bash
git branch -m main
```

---

# Branch Naming Best Practices

Professional examples:

```
feature-sales-dashboard

feature-customer-analysis

fix-calculation-error

docs-update-readme
```

Avoid:

```
newbranch

test1

changes
```

---

# Real-World Team Workflow

A typical development workflow:

```
Main Branch

      |
      |
Create Feature Branch

      |
      |
Develop Changes

      |
      |
Commit Changes

      |
      |
Create Pull Request

      |
      |
Merge Into Main
```

---

# Common Mistakes

## Working on the Wrong Branch

Always check:

```bash
git branch
```

before making changes.

---

## Creating Too Large Branches

A branch should focus on one task.

Good:

```
feature-add-sales-chart
```

Bad:

```
complete-project-update
```

---

# Interview Questions

## 1. Difference between git branch and git switch?

`git branch` creates or lists branches, while `git switch` changes the current working branch.

---

## 2. How do you create and switch to a branch?

Using:

```bash
git switch -c branch-name
```

---

## 3. What is the purpose of feature branches?

Feature branches allow developers to build new functionality separately without affecting stable code.

---

## 4. Difference between git switch and git checkout?

`git switch` is designed specifically for changing branches, while `git checkout` is an older command with multiple purposes.

---

# Key Takeaways

- Branches allow isolated development.
- `git branch` creates branches.
- `git switch` moves between branches.
- Feature branches are standard in professional workflows.
- Clean branch management improves collaboration.

---

# Next Topic

➡️ Merging Branches