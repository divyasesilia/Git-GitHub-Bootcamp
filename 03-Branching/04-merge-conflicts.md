# Git Merge Conflicts

## Overview

A merge conflict occurs when Git cannot automatically combine changes from different branches.

Conflicts usually happen when multiple developers modify the same part of a file or when Git cannot determine which version should be kept.

Merge conflicts are a normal part of collaborative development and require manual resolution.

---

# What is a Merge Conflict?

A merge conflict happens during a merge operation when Git finds conflicting changes.

Example:

Developer A changes:

```
Total Sales Calculation
```

Developer B changes the same line:

```
Revenue Calculation
```

Git cannot decide which version is correct.

Therefore, Git pauses the merge and asks the developer to resolve the conflict.

---

# Why Merge Conflicts Occur

Common reasons:

- Multiple developers edit the same lines
- Long-running branches become outdated
- Changes are made without pulling latest updates
- Files are renamed or deleted in different branches

---

# Example of a Merge Conflict

Two branches:

```
main

A---B---C


feature

A---B---D
```

Both branches changed the same location.

When merging:

```bash
git merge feature
```

Git reports:

```
CONFLICT (content): Merge conflict in file.txt
```

---

# Conflict Markers

Git marks conflicting sections in the file:

```
<<<<<<< HEAD

Current branch changes

=======

Incoming branch changes

>>>>>>> feature-branch
```

Meaning:

```
<<<<<<< HEAD
Your current branch
======= 
Incoming changes
>>>>>>> branch-name
```

---

# Resolving a Merge Conflict

The resolution process:

```
Merge Attempt

      ↓

Conflict Detected

      ↓

Open Conflicted File

      ↓

Choose Correct Changes

      ↓

Save File

      ↓

Stage Changes

      ↓

Complete Merge
```

---

# Step 1: Check Conflicted Files

Command:

```bash
git status
```

Example:

```
Unmerged paths:

modified: analysis.py
```

---

# Step 2: Open the File

Git shows the conflicting sections:

```
<<<<<<< HEAD

Your changes

=======

Other branch changes

>>>>>>> feature
```

Manually decide which changes should remain.

---

# Step 3: Remove Conflict Markers

Before:

```
<<<<<<< HEAD

Sales Analysis

=======

Revenue Analysis

>>>>>>> feature
```

After:

```
Sales and Revenue Analysis
```

Save the file.

---

# Step 4: Stage the Resolved File

Command:

```bash
git add filename
```

Example:

```bash
git add analysis.py
```

---

# Step 5: Complete the Merge

Command:

```bash
git commit -m "Resolve merge conflict"
```

The merge is now completed.

---

# Aborting a Merge

If you do not want to continue with the merge:

```bash
git merge --abort
```

This returns the repository to the state before the merge started.

---

# Checking Merge Status

Command:

```bash
git status
```

Useful for identifying:

- Conflicted files
- Merge progress
- Required actions

---

# Real-World Team Example

Imagine a data analytics team.

Branch 1:

```
feature-sales-dashboard
```

Developer adds:

- KPI cards
- Sales charts

Branch 2:

```
feature-sales-report
```

Another developer modifies the same dashboard configuration file.

When merging:

```
feature-sales-dashboard

        +

feature-sales-report

        ↓

Conflict
```

The team reviews both changes and decides the final version.

---

# Preventing Merge Conflicts

## 1. Pull Latest Changes Frequently

Before starting work:

```bash
git pull
```

This keeps your branch updated.

---

## 2. Keep Branches Small

Small branches are easier to merge.

Good:

```
feature-add-sales-chart
```

Avoid:

```
complete-dashboard-development
```

---

## 3. Communicate With Team Members

Avoid multiple people modifying the same files unnecessarily.

---

## 4. Commit Frequently

Small commits make changes easier to understand.

Good:

```
Add customer analysis query
```

Avoid:

```
large update
```

---

# Merge Conflict Best Practices

- Do not panic when conflicts occur
- Understand both changes before selecting a version
- Test after resolving conflicts
- Commit the resolution clearly

---

# Interview Questions

## 1. What is a merge conflict?

A merge conflict occurs when Git cannot automatically combine changes from different branches.

---

## 2. How do you resolve a merge conflict?

Open the conflicting file, choose the correct changes, remove conflict markers, stage the file, and commit.

---

## 3. How do you cancel a merge?

Using:

```bash
git merge --abort
```

---

## 4. Why do merge conflicts happen?

They happen when different branches modify the same part of a file or contain incompatible changes.

---

# Key Takeaways

- Merge conflicts are normal in team development.
- Git identifies conflicting changes automatically.
- Developers manually choose the correct version.
- Good communication and frequent updates reduce conflicts.

---

# Branching Module Completed

Topics Covered:

✅ Branch concepts  
✅ Creating branches  
✅ Switching branches  
✅ Merging branches  
✅ Merge conflicts  
