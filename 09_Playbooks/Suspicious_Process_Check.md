---
title: Suspicious Process Check
area: playbooks
difficulty: intermediate
status: draft
last_reviewed: 2026-07-04
sources:
tags:
  - playbook
  - defense
  - triage
---

# Purpose

A structured first response for when a process on a system you own looks unexpected or suspicious — before deciding whether it's a real incident.

# Use Case

Use when you notice an unfamiliar process, unusually high resource usage, or a process you didn't start, on a system you administer.

# Checklist

- [ ] Identify the process: name, PID, parent process, user it's running as.
- [ ] Check when it started and what launched it.
- [ ] Check what it has open: network connections, open files.
- [ ] Check if the binary is where you'd expect it and matches a known-good package, if applicable.
- [ ] Check recent logs around the time the process started (see [[Logs]]).
- [ ] Decide: known-good, needs more investigation, or escalate to full [[Incident_Response]].

# Commands or Actions

```
ps -ef | grep <name-or-pid>
ps -o ppid= -p <pid>            # parent process ID
ss -tulpn | grep <pid>          # network connections owned by the process
lsof -p <pid>                   # open files/sockets for the process
journalctl --since "1 hour ago" | grep -i <relevant term>
```

# Evidence to Capture

- Full `ps`/`lsof`/`ss` output for the process at time of discovery, before taking any remediation action.
- Timestamp of when it was first noticed and by whom.
- Relevant log excerpts covering the process's start time.

# Mistakes to Avoid

- Killing the process immediately without capturing evidence first, if there's a chance this is a real incident (see [[Forensics_Basics]]).
- Assuming a process is safe just because its name looks familiar — malicious processes sometimes use names similar to legitimate ones.
- Treating high CPU/memory usage alone as proof of compromise — check context before concluding.

# Related CORE Notes

- [[Logging_Monitoring]]
- [[Incident_Response]]
- [[Forensics_Basics]]
- [[Log_Review_Lab]]

# Sources

- NIST SP 800-61 Rev. 2 — https://csrc.nist.gov/pubs/sp/800/61/r2/final
