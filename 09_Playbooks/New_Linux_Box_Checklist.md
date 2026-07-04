---
title: New Linux Box Checklist
area: playbooks
difficulty: beginner
status: draft
last_reviewed: 2026-07-04
sources:
tags:
  - playbook
  - linux
  - hardening
---

# Purpose

A first-hour checklist for any freshly provisioned Linux system (VPS, VM, or physical box) before it's used for anything real.

# Use Case

Run this immediately after provisioning a new system and before deploying any application or exposing it to a network.

# Checklist

- [ ] Update the system: install all available security patches.
- [ ] Create a non-root user with sudo access; confirm you can log in as that user.
- [ ] Disable direct root SSH login.
- [ ] Set up SSH key authentication; disable SSH password authentication once key login is confirmed working.
- [ ] Enable a firewall with default-deny inbound, allowing only needed ports.
- [ ] Set the system timezone/clock correctly (important for accurate logs — see [[Logs]]).
- [ ] Confirm `journald`/syslog is active and retaining logs (see [[Services_Systemd]]).
- [ ] Remove or disable any unnecessary pre-installed services.
- [ ] Set up automatic security updates if appropriate for the system's purpose.
- [ ] Document what the system is for and who administers it.

# Commands or Actions

```
sudo apt update && sudo apt upgrade -y   # or dnf/yum/pacman equivalent
sudo adduser <username> && sudo usermod -aG sudo <username>
sudo ufw default deny incoming && sudo ufw default allow outgoing
sudo ufw allow OpenSSH && sudo ufw enable
systemctl status systemd-journald
```

# Evidence to Capture

- Output of `systemctl list-units --type=service --state=running` at the end of setup, for your own baseline record.
- Firewall rule list (`ufw status verbose` or equivalent).
- Confirmation that password SSH login is disabled (attempt a password login and confirm it's rejected, from a session where key-based access is already confirmed working).

# Mistakes to Avoid

- Disabling password SSH login before confirming key-based login actually works — this can lock you out.
- Opening the firewall broadly "to make setup easier" and forgetting to close it afterward.
- Skipping the update step because the system "looks new" — provisioning images can be weeks or months out of date.

# Related CORE Notes

- [[Hardening]]
- [[Basic_Hardening_Checklist]]
- [[VPS_Basics]]
- [[Permissions]]

# Sources

- CIS Benchmarks — https://www.cisecurity.org/cis-benchmarks
