---
title: GitHub
area: cloud-devops
difficulty: beginner
status: draft
last_reviewed: 2026-07-04
sources:
  - "GitHub Docs, https://docs.github.com/"
tags:
  - cloud-devops
  - github
---

# What It Is

GitHub is a hosting platform for Git repositories that adds collaboration features on top of Git itself: pull requests (proposed changes with review/discussion), issues (tracked tasks/bugs), and (optionally) automation via GitHub Actions.

# Why It Matters

GitHub is the collaboration layer that makes a Git repository like CORE usable by multiple contributors — pull requests are how changes get proposed and reviewed before merging (see [[CONTRIBUTING]] rules referenced from the repository root).

# When To Use It

Whenever a project needs public hosting, external contribution, issue tracking, or a review process around changes — as this repository itself uses.

# How To Use It Safely

- Review pull requests for scope and quality before merging — don't merge unreviewed changes into a shared branch.
- Use repository settings (branch protection, required reviews) to prevent accidental direct pushes to important branches.
- Be deliberate about what becomes public — a public repo's full history, including old commits, is visible unless explicitly rewritten.
- Never commit credentials; use GitHub's secret scanning and `.gitignore` (see repository root) as a backstop, not a substitute for care.

# Common Mistakes

- Merging a pull request without reading the actual diff.
- Assuming a private repository stays private forever, or forgetting a fork can retain history after a repo is made private.
- Treating GitHub Issues/PRs as a substitute for real documentation instead of a complement to it.

# Related CORE Notes

- [[Git]]
- [[CI_CD]]
- [[Repo_Audit_Checklist]]

# Sources

- GitHub Docs — https://docs.github.com/
