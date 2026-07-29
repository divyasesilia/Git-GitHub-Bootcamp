# Git Introduction

## Overview

Git is a distributed version control system used to track changes in source code and manage software development workflows.

It allows developers and teams to collaborate efficiently by maintaining a complete history of project changes, enabling version tracking, branching, merging, and rollback capabilities.

Git is one of the most widely adopted tools in modern software development and is an essential skill for developers, data professionals, and engineers working in collaborative environments.

---

# What is Version Control?

Version Control is a system that records changes made to files over time, allowing users to:

- Track modifications
- Restore previous versions
- Compare changes
- Collaborate with multiple contributors
- Maintain project history

### Real-World Example

Consider a data analytics project where multiple analysts update SQL scripts, Python notebooks, and dashboards.

Without version control:

- Changes may overwrite each other
- Previous versions can be lost
- Collaboration becomes difficult

With version control:

- Every change is recorded
- Previous versions can be restored
- Team members can work safely

---

# What is Git?

Git is an open-source distributed version control system created by Linus Torvalds in 2005.

Git manages changes in files by storing snapshots of the project at different points in time.

Unlike traditional centralized version control systems, Git provides every user with a complete copy of the repository history.

---

# Why Git is Used

Git helps teams and individuals:

## 1. Track Changes

Git records every modification made to project files.

Example:

```
Version 1 → Initial analysis notebook
Version 2 → Added data cleaning steps
Version 3 → Added visualization
```

---

## 2. Collaboration

Multiple developers can work on the same project using branches and merge workflows.

Example:

```
Main Project
     |
     |
Developer A → Feature Branch
Developer B → Bug Fix Branch
```

---

## 3. Maintain Project History

Git stores a complete timeline of changes.

Developers can view:

- Who made changes
- When changes were made
- What changes were introduced

---

## 4. Recover Previous Versions

If a new change introduces an issue, Git allows restoring earlier versions of the project.

---

# Git Features

## Distributed Architecture

Every developer has a complete copy of the repository, including its history.

Advantages:

- Works offline
- Faster operations
- Better reliability

---

## Branching

Branches allow developers to create independent versions of a project.

Example:

```
main
 |
 ├── feature-dashboard
 |
 └── bug-fix
```

---

## Merging

Git allows combining changes from different branches into a single project.

Example:

```
Feature Branch
       |
       ↓
     Merge
       |
       ↓
     Main Branch
```

---

## Commit History

A commit represents a saved snapshot of changes.

Example:

```
Commit 1: Created project structure

Commit 2: Added data cleaning script

Commit 3: Added dashboard analysis
```

---

# Git vs GitHub

| Git | GitHub |
|---|---|
| Version control software | Cloud-based hosting platform |
| Installed locally | Web-based service |
| Tracks file changes | Stores and shares repositories |
| Works offline | Enables collaboration |
| Created by Linus Torvalds | Owned by Microsoft |

---

# Git Workflow

The basic Git workflow consists of three main areas:

```
Working Directory
        |
        |
        ↓
Staging Area
        |
        |
        ↓
Local Repository
        |
        |
        ↓
Remote Repository
```

### Working Directory

The location where files are created and modified.

---

### Staging Area

A temporary area where changes are prepared before committing.

Command:

```bash
git add filename
```

---

### Local Repository

Stores committed changes on your computer.

Command:

```bash
git commit -m "message"
```

---

### Remote Repository

A hosted repository such as GitHub where projects are shared.

Command:

```bash
git push
```

---

# Basic Git Commands

| Command | Purpose |
|---|---|
| git init | Initialize a new repository |
| git status | Check repository status |
| git add | Add changes to staging area |
| git commit | Save changes |
| git log | View commit history |
| git clone | Copy repository locally |
| git push | Upload changes to remote repository |
| git pull | Download latest changes |

---

# Importance of Git for Data Professionals

Git is not limited to software developers.

Data professionals use Git for:

- SQL scripts
- Python projects
- Machine learning models
- Data pipelines
- Analytics dashboards
- Documentation

Example:

A Data Analyst project may contain:

```
Sales-Analysis-Project

├── SQL Queries
├── Python Notebooks
├── Data Cleaning Scripts
├── Reports
└── Documentation
```

Git helps maintain the complete project history.

---

# Key Takeaways

- Git is a distributed version control system.
- Git tracks and manages changes in projects.
- Git enables collaboration through branches and merging.
- GitHub provides online hosting and collaboration features.
- Git is an essential tool for modern technical professionals.

---

# Interview Questions

### 1. What is Git?

Git is a distributed version control system used to track changes and manage source code history.

---

### 2. What is the difference between Git and GitHub?

Git is a version control tool installed locally, while GitHub is a cloud platform used for hosting Git repositories.

---

### 3. What is a Git repository?

A Git repository is a storage location that contains project files and their complete version history.

---

### 4. What is a commit?

A commit is a snapshot of changes saved in the local Git repository.

---

## Next Topic

➡️ Git Installation and Configuration