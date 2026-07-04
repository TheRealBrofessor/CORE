---
title: Linux File Permissions Lab
area: labs
difficulty: beginner
status: draft
last_reviewed: 2026-07-04
sources:
tags:
  - lab
  - linux
  - permissions
---

# Objective

Practice reading and changing Linux file permissions until the permission model in [[Permissions]] is intuitive, not just theoretical.

# Safety Scope

Local machine or personal VM/container only. This lab creates and modifies test files in a scratch directory — it does not touch system files or require root privileges beyond your own user account.

# Requirements

- A Linux system (or WSL/VM) with a standard shell.
- Basic familiarity with [[Terminal]] and [[Command_Line]].

# Steps

1. Create a scratch directory: `mkdir -p ~/core-lab/perm-lab && cd ~/core-lab/perm-lab`.
2. Create a test file: `touch secret.txt` and run `ls -l secret.txt` — note the default permission string.
3. Remove all permissions for group and others: `chmod 600 secret.txt`. Confirm with `ls -l`.
4. Try to read the file as intended (`cat secret.txt`) — it should still work as the owner.
5. Add execute permission for yourself only: `chmod u+x secret.txt`. Note this makes little sense for a text file — execute matters for scripts/binaries, not general readability.
6. Create a directory `mkdir locked_dir`, remove execute permission (`chmod u-x locked_dir`), then try `cd locked_dir` or `ls locked_dir/somefile` — observe the "permission denied" even though you own it, illustrating that directory execute permission is required to traverse it.
7. Restore sane permissions: `chmod 755 locked_dir` and `chmod 644 secret.txt`.

# Expected Result

You should be able to explain, from direct observation, why removing execute permission on a directory blocks traversal even for the owner, and why `600` vs `644` vs `755` mean different things for files vs. directories.

# Troubleshooting

- If `chmod` reports "operation not permitted," confirm you own the file (`ls -l`) — you can't `chmod` a file you don't own without elevated privileges.
- If commands behave unexpectedly, run `id` to confirm which user/groups you're actually operating as.

# Cleanup

`rm -rf ~/core-lab/perm-lab` when finished.

# Related CORE Notes

- [[Permissions]]
- [[Filesystems]]
- [[Basic_Hardening_Checklist]]

# Sources

- `man chmod` — standard Linux manual page.
