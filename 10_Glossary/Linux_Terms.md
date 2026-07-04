---
title: Linux Terms
area: glossary
difficulty: beginner
status: draft
last_reviewed: 2026-07-04
sources:
  - "man pages (various)"
tags:
  - glossary
  - linux
---

# Linux Terms

- **Shell** — a program that reads and executes commands (e.g. Bash, Zsh). See [[Terminal]].
- **Root** — the superuser account with unrestricted system access; also the name of the top-level directory (`/`). See [[Filesystems]].
- **Permissions** — read/write/execute rights on files and directories, defined per owner/group/others. See [[Permissions]].
- **Process** — a running instance of a program, identified by a PID (process ID).
- **Daemon** — a background process/service with no direct user interaction, typically managed by systemd. See [[Services_Systemd]].
- **systemd** — the init system and service manager used by most modern Linux distributions. See [[Services_Systemd]].
- **journalctl** — the command used to read systemd's centralized log (the journal). See [[Logs]].
- **Symlink** — a symbolic link: a file that points to another file/path rather than containing data itself.
- **Package manager** — a tool (`apt`, `dnf`, `pacman`, etc.) for installing, updating, and removing software.

# Related CORE Notes

- [[Linux_Index]]
- [[Terminal]]
- [[Permissions]]

# Sources

- Standard Linux manual pages (`man`).
