# Git Installation and Configuration

## Overview

Before using Git for version control, Git must be installed and configured on the local machine.

Git configuration connects the local Git environment with the user's identity and defines how Git manages projects.

---

# Installing Git

Git is available for major operating systems:

- Windows
- macOS
- Linux

After installation, Git can be accessed through:

- Command Prompt
- PowerShell
- Terminal
- VS Code Terminal

---

# Verify Git Installation

After installing Git, verify the installation using:

```bash
git --version
```

Example output:

```bash
git version 2.53.0.windows.1
```

This confirms that Git is successfully installed.

---

# Git Configuration

Git identifies users through configuration settings.

The two most important settings are:

- Username
- Email address

These details are attached to every commit created by the user.

---

# Configure Username

Command:

```bash
git config --global user.name "Your Name"
```

Example:

```bash
git config --global user.name "Divya Sesilia"
```

---

# Configure Email

Command:

```bash
git config --global user.email "your-email@example.com"
```

Example:

```bash
git config --global user.email "divyasesilia@gmail.com"
```

The email should match the email connected to the GitHub account.

---

# Global Configuration

The `--global` option applies the configuration to all repositories on the local machine.

Example:

```bash
git config --global user.name "Divya Sesilia"
```

This configuration will be used automatically for future Git projects.

---

# View Git Configuration

To view all Git configurations:

```bash
git config --list
```

Example output:

```text
user.name=Divya Sesilia
user.email=divyasesilia@gmail.com
```

---

# Local vs Global Configuration

| Configuration | Scope | Usage |
|---|---|---|
| Global | Entire computer | Applies to all repositories |
| Local | Single repository | Applies only to current project |

---

# Checking Current User Configuration

Commands:

```bash
git config user.name
```

```bash
git config user.email
```

Example:

```text
Divya Sesilia
divyasesilia@gmail.com
```

---

# Git Configuration File

Git stores global configuration information in:

```
.gitconfig
```

Location:

```
User Home Directory
```

---

# Why Configuration is Important

Proper Git configuration ensures:

- Commits are correctly attributed
- Team members can identify contributors
- GitHub links commits to the correct account
- Professional collaboration workflow

---

# Common Issues

## Incorrect Email Configuration

Problem:

Commits may not appear correctly on GitHub.

Solution:

Update the email:

```bash
git config --global user.email "correct-email@example.com"
```

---

## Missing Username

Problem:

Git cannot identify the commit author.

Solution:

Configure username:

```bash
git config --global user.name "Your Name"
```

---

# Interview Questions

## 1. Why do we configure username and email in Git?

Git uses these details to identify the author of each commit.

---

## 2. Difference between --global and local configuration?

`--global` applies settings to all repositories, while local configuration applies only to the current repository.

---

## 3. How do you check Git configuration?

Using:

```bash
git config --list
```

---

## Next Topic

➡️ Essential Git Commands