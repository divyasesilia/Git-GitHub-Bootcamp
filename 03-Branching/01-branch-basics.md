# Git Branch Basics

## Overview

A Git branch is an independent line of development that allows developers to work on features, fixes, or experiments without affecting the main project.

Branches are one of Git's most powerful features because they enable parallel development and safe collaboration.

---

# What is a Git Branch?

A branch is a movable pointer to a specific commit in Git history.

Instead of modifying the main project directly, developers create a separate branch where they can make changes safely.

Example:

```
main
 |
 A---B---C
          \
           D---E
           feature-branch
```

The feature branch contains new changes while the main branch remains stable.

---

# Why Branches are Used

Branches help teams:

- Develop new features safely
- Fix bugs without affecting production code
- Test changes independently
- Work on multiple tasks simultaneously
- Maintain a clean development workflow

---

# Main Branch

The main branch is the primary branch of a repository.

Common names:

- `main`
- `master` (older projects)

The main branch usually contains:

- Stable code
- Production-ready changes
- Completed features

Example:

```
main

|
|--- Version 1
|--- Version 2
|--- Version 3
```

---

# Feature Branches

A feature branch is created to develop a specific feature separately.

Example:

A data analytics project needs a new dashboard.

Instead of changing `main`:

```
main
 |
 |
 └── feature-dashboard
```

The dashboard development happens inside the feature branch.

After completion, the branch is merged into main.

---

# Common Branch Types

## Main Branch

Purpose:

- Production-ready code
- Stable releases

Example:

```
main
```

---

## Feature Branch

Purpose:

- New functionality development

Examples:

```
feature-sales-dashboard

feature-login-page
```

---

## Bug Fix Branch

Purpose:

- Fix existing issues

Examples:

```
fix-calculation-error

fix-dashboard-filter
```

---

## Documentation Branch

Purpose:

- Update documentation separately

Example:

```
docs-update-readme
```

---

# Branch Workflow

Professional Git workflow:

```
Main Branch

      |
      |
Create Branch

      |
      |
Develop Feature

      |
      |
Commit Changes

      |
      |
Review Changes

      |
      |
Merge Back to Main
```

---

# Branch Naming Conventions

Good branch names are descriptive.

Examples:

```
feature-sales-analysis

feature-powerbi-dashboard

fix-data-cleaning-error

docs-update-readme
```

Avoid:

```
test
new
branch1
changes
```

---

# Creating a Branch

Command:

```bash
git branch branch-name
```

Example:

```bash
git branch feature-dashboard
```

This creates a new branch.

---

# Viewing Branches

Command:

```bash
git branch
```

Example output:

```
* main
  feature-dashboard
```

The `*` indicates the current branch.

---

# Why Not Work Directly on Main?

Directly changing the main branch can create problems:

- Unstable code
- Difficult rollback
- Collaboration conflicts
- Risk of breaking production

Professional teams protect the main branch and use feature branches.

---

# Branch Example in Data Analytics

A Data Analyst project may use branches like:

```
Sales-Analysis-Project

main

 |
 |
 ├── feature-sales-dashboard
 |
 ├── feature-customer-analysis
 |
 └── docs-update-readme
```

Each branch handles a specific improvement.

---

# Best Practices

## Create Small Focused Branches

Good:

```
feature-monthly-sales-report
```

Avoid:

```
complete-project-update
```

---

## Use Meaningful Names

Branch names should explain the purpose.

---

## Merge Only Completed Work

Before merging:

- Test changes
- Review updates
- Confirm functionality

---

# Interview Questions

## 1. What is a Git branch?

A Git branch is an independent line of development that allows changes to be made without affecting the main codebase.

---

## 2. Why are branches important?

Branches allow parallel development, safer changes, and better collaboration.

---

## 3. What is the main branch?

The main branch is the primary stable branch containing production-ready code.

---

## 4. Why should developers avoid working directly on main?

Because unfinished or incorrect changes can affect the stable project.

---

# Key Takeaways

- Branches allow isolated development.
- Main branch contains stable code.
- Feature branches support collaboration.
- Branching is essential for professional Git workflows.

---

# Next Topic

➡️ Creating and Switching Branches