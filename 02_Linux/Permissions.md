---
title: Linux Permissions
area: linux
difficulty: beginner
status: draft
last_reviewed: 2026-07-04
sources:
  - "man chmod"
  - "man chown"
tags:
  - linux
  - permissions
---

# What It Is

Every file and directory on Linux has an owner (user), a group, and three permission sets (owner/group/others), each with read (`r`), write (`w`), and execute (`x`) bits. `ls -l` shows this as a string like `-rwxr-xr--`.

# Why It Matters

Permissions are the first line of defense on any multi-user or exposed system. Misconfigured permissions are a common root cause of both security incidents and "why won't this run" troubleshooting.

# When To Use It

Whenever a program can't read/write a file, or when hardening a system (removing unnecessary access) — see [[Hardening]].

# How To Use It Safely

- Use `chmod` with the minimum permission needed (e.g. `644` for a normal file, not `777`).
- Use `chown`/`chgrp` deliberately — changing ownership can lock you out of your own files if misapplied.
- Check permissions with `ls -l` or `stat` before changing them, so you know the starting state.
- Never chmod `777` as a troubleshooting shortcut on anything beyond a throwaway local test — it removes all access control.

# Common Mistakes

- Using `chmod 777` to "fix" a permission error without understanding why access was denied.
- Confusing execute permission on a directory (needed to enter/traverse it) with execute permission on a file (needed to run it).
- Forgetting that root bypasses standard permission checks entirely, which can mask a permissions bug during testing.

# Related CORE Notes

- [[Terminal]]
- [[Filesystems]]
- [[Hardening]]
- [[Linux_File_Permissions_Lab]]

# Sources

- `man chmod`, `man chown` — standard Linux manual pages.
