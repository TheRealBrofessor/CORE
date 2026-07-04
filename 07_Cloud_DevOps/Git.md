---
title: Git
area: cloud-devops
difficulty: beginner
status: draft
last_reviewed: 2026-07-04
sources:
  - "Pro Git Book, https://git-scm.com/book/en/v2"
tags:
  - cloud-devops
  - git
---

# What It Is

Git is a distributed version control system: it tracks changes to files over time as a series of commits, allows branching to work on parallel lines of change, and can synchronize history between repositories (e.g. your local copy and GitHub).

# Why It Matters

Version control is what makes it safe to experiment, collaborate, and recover from mistakes in code (and, as in this vault, in Markdown content). It's also what makes AI coding agent changes ([[Claude_Code]], [[Codex]]) reviewable and reversible — see [[AI_Safety_Workflows]].

# When To Use It

For any project — code or otherwise — where you want a history of changes, the ability to collaborate, or the ability to undo a mistake.

# How To Use It Safely

- Commit in small, logical units with clear messages, not one giant commit for unrelated changes.
- Use branches for in-progress work instead of committing directly to a shared main branch.
- Understand the difference between `git reset --hard` (discards changes) and safer alternatives before using it.
- Never force-push (`git push --force`) to a shared branch without team agreement — it can overwrite others' work.

# Common Mistakes

- Committing secrets (API keys, passwords) into history — removing them later requires rewriting history, which is disruptive.
- Using `git add -A`/`git add .` reflexively and accidentally committing unintended files.
- Force-pushing to a shared branch and silently discarding a collaborator's commits.

# Related CORE Notes

- [[GitHub]]
- [[AI_Safety_Workflows]]
- [[Command_Line]]

# Sources

- Chacon, S. & Straub, B., *Pro Git* — https://git-scm.com/book/en/v2
