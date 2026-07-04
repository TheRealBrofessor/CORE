---
title: Basic Hardening Checklist
area: playbooks
difficulty: intermediate
status: draft
last_reviewed: 2026-07-04
sources:
tags:
  - playbook
  - hardening
---

# Purpose

A periodic hardening review checklist for a system you already administer, beyond the initial setup covered in [[New_Linux_Box_Checklist]].

# Use Case

Run this on a recurring schedule (e.g. quarterly) or after any significant change to a system's role or exposed services.

# Checklist

- [ ] Review all running services — is each one still needed? (see [[Services_Systemd]])
- [ ] Review all open ports against the firewall's allow list — remove anything no longer needed.
- [ ] Review user accounts — remove/disable any that are no longer needed.
- [ ] Review sudo/admin group membership — confirm it matches who actually needs elevated access.
- [ ] Confirm all software is patched to current supported versions.
- [ ] Review file permissions on sensitive files/directories (see [[Permissions]]).
- [ ] Confirm logging/monitoring is still active and retaining an adequate window (see [[Logging_Monitoring]]).
- [ ] Rotate or review credentials/keys that haven't been rotated recently.

# Commands or Actions

```
ss -tulpn                              # listening ports and owning processes
systemctl list-units --type=service --state=running
sudo cat /etc/group | grep sudo        # sudo group membership (Debian/Ubuntu)
journalctl --disk-usage                # confirm journal retention/size
```

# Evidence to Capture

- Before/after list of running services and open ports, so changes are auditable.
- List of accounts removed/disabled and why.
- Date of last successful patch run.

# Mistakes to Avoid

- Treating this as a one-time task instead of a recurring review — systems drift as software is installed and users change over time.
- Removing a service or account without confirming nothing depends on it first.
- Hardening in a way that breaks legitimate functionality without testing afterward.

# Related CORE Notes

- [[Hardening]]
- [[New_Linux_Box_Checklist]]
- [[Threat_Modeling]]

# Sources

- CIS Benchmarks — https://www.cisecurity.org/cis-benchmarks
