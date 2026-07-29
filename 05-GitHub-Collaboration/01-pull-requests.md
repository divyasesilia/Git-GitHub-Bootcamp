# GitHub Pull Requests

## Overview

A Pull Request (PR) is a GitHub feature used to propose changes from one branch into another branch.

It allows developers to:

- Share completed work
- Request code review
- Discuss changes
- Run automated checks
- Merge approved updates

Pull Requests are a central part of professional software development workflows.

---

# What is a Pull Request?

A Pull Request is a request to merge changes from a source branch into a target branch.

Example:

```
feature-dashboard

        |
        |
        ↓

Pull Request

        |
        |
        ↓

main
```

The developer is asking:

"Please review my changes and merge them into the main project."

---

# Why Use Pull Requests?

Pull Requests help teams:

- Review code before merging
- Identify mistakes early
- Maintain code quality
- Discuss implementation decisions
- Track project changes
- Collaborate effectively

---

# Pull Request Workflow

Professional workflow:

```
Create Feature Branch

        ↓

Develop Changes

        ↓

Commit Changes

        ↓

Push Branch to GitHub

        ↓

Create Pull Request

        ↓

Code Review

        ↓

Approval

        ↓

Merge into Main
```

---

# Creating a Pull Request

## Step 1: Create a Branch

Example:

```bash
git switch -c feature-dashboard
```

---

## Step 2: Make Changes

Example:

```
Add sales dashboard
Update documentation
Improve analysis
```

---

## Step 3: Commit Changes

```bash
git add .
```

```bash
git commit -m "Add sales dashboard feature"
```

---

## Step 4: Push Branch

```bash
git push origin feature-dashboard
```

---

## Step 5: Open Pull Request

On GitHub:

1. Open repository
2. Select Pull Requests
3. Click New Pull Request
4. Select branches
5. Add description
6. Submit PR

---

# Pull Request Components

A professional PR contains:

## Title

Should clearly describe the change.

Good:

```
Add customer analysis dashboard
```

Avoid:

```
Update files
```

---

## Description

Explain:

- What changed
- Why it was changed
- How it was tested

Example:

```
Added customer segmentation analysis.

Changes:
- Added SQL queries
- Updated dashboard visuals
- Added documentation
```

---

## Reviewers

Team members who check the changes.

---

## Comments

Reviewers can discuss:

- Improvements
- Questions
- Suggestions

---

# Reviewing a Pull Request

A reviewer checks:

## Code Quality

Questions:

- Is the code readable?
- Are naming conventions followed?
- Is the logic correct?

---

## Functionality

Questions:

- Does the feature work?
- Are requirements completed?

---

## Documentation

Questions:

- Are instructions updated?
- Are changes explained?

---

# Pull Request Approval

After review:

Options:

```
Approve

Request Changes

Comment
```

---

# Merge Options

GitHub provides different merge strategies.

---

# 1. Merge Commit

Creates a merge commit.

Example:

```
A---B---C
     \   \
      D---M
```

Preserves complete branch history.

---

# 2. Squash and Merge

Combines multiple commits into one.

Before:

```
Fix typo

Update chart

Improve query
```

After:

```
Complete dashboard update
```

Creates cleaner history.

---

# 3. Rebase and Merge

Places commits directly on top of the target branch.

Creates a linear history.

---

# Pull Request Best Practices

## Keep PRs Small

Good:

```
Add sales chart
```

Avoid:

```
Complete application redesign
```

Small PRs are easier to review.

---

## Write Clear Descriptions

Explain:

- Purpose
- Changes
- Testing

---

## Review Before Creating PR

Check:

```bash
git status
```

and:

```bash
git diff
```

before submitting.

---

# Real-World Company Example

A developer works on:

```
feature-payment-system
```

After completion:

```
Push Branch

      ↓

Create Pull Request

      ↓

Developer Review

      ↓

Testing

      ↓

Approval

      ↓

Merge to Main
```

The main branch remains protected and stable.

---

# Data Analytics Project Example

For an Ecommerce Dashboard project:

Branches:

```
main

 |
 |
 ├── feature-sales-analysis
 |
 ├── feature-sql-queries
 |
 ├── feature-powerbi-dashboard
```

Example Pull Request:

Title:

```
Add SQL sales analysis
```

Description:

```
Changes:
- Added sales queries
- Added customer analysis
- Updated documentation

Testing:
SQL queries validated successfully.
```

After approval:

```
feature-sql-queries

        ↓

main
```

---

# Pull Request vs Push

| Push | Pull Request |
|---|---|
| Sends changes to remote repository | Requests review and merging |
| No review required | Requires collaboration |
| Developer action | Team workflow |

---

# Interview Questions

## 1. What is a Pull Request?

A Pull Request is a request to merge changes from one branch into another after review.

---

## 2. Why are Pull Requests important?

They enable collaboration, code review, and quality control.

---

## 3. What happens after creating a Pull Request?

Team members review changes, request modifications if needed, approve, and merge the PR.

---

## 4. Difference between merge and pull request?

Merge is a Git operation that combines branches. A Pull Request is a GitHub collaboration process used before merging.

---

# Key Takeaways

- Pull Requests enable team collaboration.
- PRs allow code review before merging.
- Good PRs have clear descriptions.
- Small PRs are easier to review.
- Pull Requests are standard in professional GitHub workflows.

---

# Next Topic

➡️ GitHub Issues