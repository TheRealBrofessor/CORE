---
title: Filesystems
area: foundations
difficulty: beginner
status: draft
last_reviewed: 2026-07-04
sources:
  - "The Linux Documentation Project, https://tldp.org/"
tags:
  - foundations
  - filesystems
---

# What It Is

A filesystem is the system an operating system uses to organize data into files and directories on storage. On Linux/Unix systems, everything is arranged into a single tree starting at the root (`/`); on Windows, each drive gets its own letter (`C:\`).

# Why It Matters

Nearly every task — reading logs, configuring services, running programs, using Git — involves navigating and referencing paths. Misunderstanding relative vs. absolute paths is one of the most common sources of "it's not working" for beginners.

# When To Use It

Any time you're navigating a system from the command line, writing a script that reads/writes files, or trying to understand where a program's config or logs live.

# How To Use It Safely

- Know the difference between an absolute path (`/etc/passwd`, starts at root) and a relative path (`../config`, starts from your current directory).
- Use `pwd` to confirm your current directory before running a path-sensitive command.
- Be cautious with wildcards (`*`) in destructive commands — they expand to every match, which can be more than you expect.

# Common Mistakes

- Assuming a relative path will always point to the same thing regardless of current directory.
- Confusing a symlink for the real file it points to.
- Not checking file permissions before assuming a "file not found" error is actually about existence rather than access — see [[Permissions]].

# Related CORE Notes

- [[Command_Line]]
- [[Permissions]]
- [[Terminal]]

# Sources

- The Linux Documentation Project — https://tldp.org/
