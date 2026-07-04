---
title: Systemd Service Check Lab
area: labs
difficulty: beginner
status: draft
last_reviewed: 2026-07-04
sources:
tags:
  - lab
  - linux
  - systemd
---

# Objective

Practice checking, starting/stopping, and reading logs for a systemd service, applying [[Services_Systemd]] and [[Logs]] hands-on.

# Safety Scope

Local machine or personal VM/container with systemd (most modern Linux distributions). Use a low-risk, already-installed service (e.g. `cron`, `ssh`, or `systemd-timesyncd`) — do not disable a service you rely on without understanding the impact first.

# Requirements

- A systemd-based Linux system with sudo access.
- At least one running service to inspect (check with `systemctl list-units --type=service --state=running`).

# Steps

1. List running services: `systemctl list-units --type=service --state=running`.
2. Pick one low-risk service and check its detailed status: `systemctl status <service>`.
3. Note the fields: `Loaded`, `Active`, `Main PID`, and the recent log lines shown inline.
4. View its full recent logs: `journalctl -u <service> --since "1 hour ago"`.
5. Restart the service: `sudo systemctl restart <service>`, then immediately re-check `systemctl status <service>` to confirm it came back up cleanly.
6. Check if the service is enabled to start on boot: `systemctl is-enabled <service>`.

# Expected Result

You should be able to state, for your chosen service: whether it's currently active, whether it starts on boot, and what its most recent log entries say — all without needing to search the internet mid-task.

# Troubleshooting

- If `systemctl status` shows "failed" after a restart, run `journalctl -u <service> -n 50` to see the failure detail before assuming the lab is broken.
- If you don't have sudo access, this lab can still be done read-only (skip the restart step) using `systemctl status` and `journalctl` alone.

# Cleanup

No cleanup required if you only restarted an already-running service. If you changed `enabled`/`disabled` state during the lab, restore it to its original value.

# Related CORE Notes

- [[Services_Systemd]]
- [[Logs]]
- [[Troubleshooting]]

# Sources

- `man systemctl`, `man journalctl` — standard systemd manual pages.
