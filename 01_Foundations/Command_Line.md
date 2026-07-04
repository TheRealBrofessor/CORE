---
title: The Command Line
area: foundations
difficulty: beginner
status: draft
last_reviewed: 2026-07-04
sources:
  - "GNU Bash Reference Manual, https://www.gnu.org/software/bash/manual/"
tags:
  - foundations
  - command-line
---

# What It Is

The command line (a shell, e.g. Bash, Zsh) is a text-based interface where you type commands directly instead of clicking through a graphical interface. A shell reads a line of text, interprets the first word as a command, and passes the rest as arguments.

# Why It Matters

Most servers, containers, and remote systems have no graphical interface at all. Nearly every tool covered elsewhere in CORE (Linux administration, networking diagnostics, Git, Docker, cloud CLIs) is operated through a shell.

# When To Use It

Any time you need to inspect, configure, or automate a system that doesn't have (or shouldn't need) a graphical interface — which in practice is most of technical work covered in this vault.

# How To Use It Safely

- Read a command before running it, especially anything copied from the internet — know what each flag does.
- Use `--dry-run` or equivalent flags when a tool offers one, before running the real command.
- Be deliberate with destructive commands (deleting, overwriting, permission changes) — there is often no confirmation prompt.
- Keep a command history (`history` in Bash) so you can review what you actually ran.

# Common Mistakes

- Running commands found online without understanding what they do.
- Confusing `rm` (delete) with `mv` (move) — `rm` has no undo.
- Not knowing the difference between your current directory and an absolute path, and running a command in the wrong place.

# Related CORE Notes

- [[Terminal]]
- [[Filesystems]]
- [[Permissions]]

# Sources

- GNU Bash Reference Manual — https://www.gnu.org/software/bash/manual/
