---
title: Log Review Lab
area: labs
difficulty: intermediate
status: draft
last_reviewed: 2026-07-04
sources:
tags:
  - lab
  - defense
  - logs
---

# Objective

Practice a structured log review — scoping a time window, searching for specific event patterns, and documenting findings — reinforcing [[Logs]] and [[Logging_Monitoring]].

# Safety Scope

Local machine or personal VM only. This lab reviews your own system's authentication logs — no external systems, no third-party data.

# Requirements

- A Linux system with `journalctl` (systemd) or `/var/log/auth.log` (Debian/Ubuntu) / `/var/log/secure` (RHEL-based).

# Steps

1. Scope a time window for review, e.g. the last 24 hours: `journalctl --since "24 hours ago" -u ssh` (or the equivalent auth log for your distribution).
2. Search specifically for failed authentication attempts: `journalctl --since "24 hours ago" | grep -i "failed password"` (adjust grep pattern to your system's actual log format).
3. Count occurrences to look for patterns: pipe the above through `wc -l`, and separately group by source IP if present (e.g. `grep "Failed password" auth.log | awk '{print $(NF-3)}' | sort | uniq -c | sort -rn`, adjusting field position to your log format).
4. Note any repeated-source-IP failed attempts — this is the kind of signal [[Suspicious_Process_Check]] and [[Network_Triage]] build on.
5. Document your findings in a simple format: time window reviewed, what you searched for, what you found, and your conclusion (e.g. "normal background noise" vs. "warrants follow-up").

# Expected Result

A short written summary of what you searched, what you found, and whether it warrants further investigation — practicing the documentation habit described in [[Incident_Response]].

# Troubleshooting

- If `grep` patterns return nothing, confirm the actual log format on your distribution first — messages vary by distro and by SSH version.
- If log volume is too large to review manually, narrow the time window further before adding more complex filtering.

# Cleanup

None required — this lab is read-only against existing logs.

# Related CORE Notes

- [[Logs]]
- [[Logging_Monitoring]]
- [[Incident_Response]]
- [[Suspicious_Process_Check]]

# Sources

- `man journalctl` — standard systemd manual page.
