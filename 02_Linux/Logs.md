---
title: Linux Logs
area: linux
difficulty: intermediate
status: draft
last_reviewed: 2026-07-04
sources:
  - "man journalctl"
tags:
  - linux
  - logs
---

# What It Is

Linux logs record what the system and its services have been doing. On systemd-based systems, most logs are collected by `journald` and viewed with `journalctl`; many services also write plain-text logs under `/var/log/`.

# Why It Matters

Logs are the primary evidence trail for troubleshooting and for security monitoring ([[Logging_Monitoring]]). An incident response process ([[Incident_Response]]) is only as good as the logs available to review.

# When To Use It

Any time something failed and you need to know why, or when reviewing a system's recent activity for signs of a problem or intrusion.

# How To Use It Safely

- Use `journalctl -u <service>` to scope to one service instead of scrolling the entire journal.
- Use `journalctl --since` / `--until` to bound a time window.
- Treat logs as sensitive data — they can contain IPs, usernames, and sometimes accidental secrets. Don't paste raw logs into public places without review.
- Preserve logs before troubleshooting steps that might overwrite or rotate them, if the log content itself might matter later (see [[Evidence to Capture|Log_Review_Lab]]).

# Common Mistakes

- Only checking one log source (e.g. `journalctl`) when the relevant information is in a service-specific log under `/var/log/`.
- Not noticing log rotation has already discarded the relevant window of time.
- Skimming logs without a time-bounded, targeted search, and missing the one relevant line in thousands.

# Related CORE Notes

- [[Services_Systemd]]
- [[Logging_Monitoring]]
- [[Log_Review_Lab]]
- [[Troubleshooting]]

# Sources

- `man journalctl` — standard on any systemd-based Linux system.
