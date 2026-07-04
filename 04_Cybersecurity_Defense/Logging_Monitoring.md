---
title: Logging and Monitoring
area: defense
difficulty: intermediate
status: draft
last_reviewed: 2026-07-04
sources:
  - "NIST SP 800-92, Guide to Computer Security Log Management"
tags:
  - defense
  - logging
  - monitoring
---

# What It Is

Logging is recording events as they happen (logins, errors, configuration changes, network connections). Monitoring is actively watching those logs (and other signals like resource usage) for patterns that indicate a problem, ideally with alerting rather than manual review alone.

# Why It Matters

You can't detect or investigate what you don't log. Logging and monitoring are what turn [[Incident_Response]] from guesswork into an evidence-based process, and are core to detecting the early signs of an incident before it escalates.

# When To Use It

Continuously, on any system you're responsible for securing — not just after something has already gone wrong.

# How To Use It Safely

- Log security-relevant events (authentication, permission changes, service start/stop) at minimum — see [[Logs]].
- Centralize logs where practical so they survive a compromised or wiped individual host.
- Set a retention period that balances storage cost against how far back you might need to investigate.
- Alert on high-signal events (repeated failed logins, new admin accounts) rather than trying to alert on everything, which trains people to ignore alerts.

# Common Mistakes

- Logging everything with no plan for reviewing it — logs that are never read provide no defensive value.
- Storing logs only locally on the system being monitored, where an attacker who compromises the system can also delete the evidence.
- Alert fatigue from over-broad alerting rules, causing real alerts to get ignored.

# Related CORE Notes

- [[Logs]]
- [[Incident_Response]]
- [[Log_Review_Lab]]
- [[Suspicious_Process_Check]]

# Sources

- NIST SP 800-92, *Guide to Computer Security Log Management* — https://csrc.nist.gov/pubs/sp/800/92/final
