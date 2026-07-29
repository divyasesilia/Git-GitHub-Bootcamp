# GitHub Code Review

## Overview

Code review is the process of examining code changes before they are merged into the main project.

It helps teams:

- Improve code quality
- Find mistakes early
- Share knowledge
- Maintain coding standards
- Prevent bugs

Code review is an essential practice in professional software development teams.

---

# What is Code Review?

Code review is a structured evaluation of changes made by a developer.

The reviewer checks:

- Code correctness
- Readability
- Performance
- Security
- Documentation
- Testing

Example:

```
Developer creates Pull Request

        ↓

Reviewer examines changes

        ↓

Feedback provided

        ↓

Developer updates code

        ↓

Approval

        ↓

Merge
```

---

# Why is Code Review Important?

Code review helps teams:

## Improve Quality

Another person can identify problems that the original developer may miss.

---

## Share Knowledge

Team members understand different parts of the project.

---

## Maintain Standards

Teams follow consistent:

- Coding style
- Naming conventions
- Documentation practices

---

## Reduce Bugs

Problems are found before reaching production.

---

# Code Review Workflow

Professional workflow:

```
Developer

   ↓

Create Feature Branch

   ↓

Write Code

   ↓

Create Pull Request

   ↓

Assign Reviewer

   ↓

Review Changes

   ↓

Request Changes / Approve

   ↓

Merge
```

---

# Reviewer Responsibilities

A reviewer should check:

## 1. Functionality

Questions:

- Does the code solve the required problem?
- Does it work as expected?

---

## 2. Code Quality

Check:

- Is the code readable?
- Are names meaningful?
- Is the structure understandable?

---

## 3. Performance

Consider:

- Is the solution efficient?
- Are there unnecessary operations?

---

## 4. Security

Check:

- Sensitive information exposure
- Unsafe practices
- Poor validation

---

## 5. Documentation

Verify:

- Comments where needed
- Updated README
- Clear explanations

---

# Types of Review Comments

## Suggestion

Used for improvement.

Example:

```
Consider using a function here to improve readability.
```

---

## Question

Used to understand logic.

Example:

```
Could you explain why this approach was chosen?
```

---

## Issue

Used when something must be fixed.

Example:

```
This calculation produces incorrect results.
```

---

# Approval Process

After review, reviewers can:

## Approve

Meaning:

```
Changes look good.
```

The Pull Request can be merged.

---

## Request Changes

Meaning:

```
Updates are required before merging.
```

The developer makes corrections.

---

## Comment

Used for discussion without blocking the merge.

---

# Code Review Checklist

## Code

☐ Does the code work correctly?  
☐ Is the logic clear?  
☐ Are variables and functions named properly?  
☐ Are there unnecessary changes?  

---

## Testing

☐ Has the code been tested?  
☐ Are edge cases considered?  

---

## Documentation

☐ Are instructions updated?  
☐ Are important decisions explained?  

---

## Security

☐ Are credentials protected?  
☐ Is sensitive information avoided?  

---

# Good Code Review Practices

## Be Constructive

Good:

```
Could we simplify this function to make it easier to maintain?
```

Avoid:

```
This code is bad.
```

---

## Focus on the Code

Review the implementation, not the person.

---

## Explain Suggestions

Instead of only saying what to change, explain why.

Example:

```
Using a dictionary here improves lookup speed from O(n) to O(1).
```

---

# Common Code Review Mistakes

## Reviewing Too Many Changes

Large Pull Requests are difficult to review.

Better:

```
Small focused Pull Requests
```

---

## Ignoring Documentation

Code without explanation becomes difficult to maintain.

---

## Only Looking for Errors

Good reviews also recognize:

- Good design
- Improvements
- Best practices

---

# Real-World Company Example

A developer creates a payment feature.

Pull Request:

```
Feature:
Add payment processing
```

Reviewer checks:

```
✓ Code structure
✓ Error handling
✓ Security
✓ Tests
✓ Documentation
```

Feedback:

```
Please add validation before processing payment.
```

Developer updates code.

Reviewer approves.

Feature is merged.

---

# Data Analytics Project Example

For an Ecommerce Sales Dashboard:

Pull Request:

```
Add customer analysis notebook
```

Reviewer checks:

## SQL

- Are queries correct?
- Are joins accurate?

## Python

- Is data cleaning logic clear?
- Are calculations correct?

## Dashboard

- Are KPIs accurate?
- Are visuals meaningful?

## Documentation

- Are insights explained?

After approval:

```
feature-customer-analysis

          ↓

main
```

---

# Code Review and Data Analysts

Code review is also important for analysts.

Examples:

- Reviewing SQL queries
- Checking Python notebooks
- Validating dashboard calculations
- Reviewing documentation

Quality checks improve trust in analytics results.

---

# Interview Questions

## 1. What is code review?

Code review is the process of evaluating code changes before merging them into a project.

---

## 2. Why is code review important?

It improves quality, finds bugs, shares knowledge, and maintains standards.

---

## 3. What happens when changes are requested?

The developer updates the code and submits it for another review.

---

## 4. What makes a good code review?

A good review is constructive, specific, and focused on improving the code.

---

# Key Takeaways

- Code review improves software quality.
- Pull Requests enable the review process.
- Reviewers check functionality, quality, and security.
- Feedback should be constructive.
- Professional teams review changes before merging.

---

# Next Topic

➡️ Forks and Open Source Contribution