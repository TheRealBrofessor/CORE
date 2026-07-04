---
title: Services and systemd
area: linux
difficulty: intermediate
status: draft
last_reviewed: 2026-07-04
sources:
  - "systemd.io documentation, https://systemd.io/"
tags:
  - linux
  - systemd
  - services
---

# What It Is

systemd is the init system and service manager used by most modern Linux distributions. It starts, stops, restarts, and monitors background services ("units"), and is controlled primarily via the `systemctl` command.

# Why It Matters

Almost everything running in the background on a modern Linux box — web servers, SSH, logging daemons, security agents — is managed as a systemd service. Knowing how to check and control service state is essential for both operations and defense (e.g. confirming a monitoring agent is actually running).

# When To Use It

When you need to check if a service is running, start/stop/restart it, view its recent logs, or configure it to start on boot.

# How To Use It Safely

- Check status before changing anything: `systemctl status <service>`.
- Use `systemctl restart` instead of `stop` + `start` where a clean restart is what you actually want.
- Review `journalctl -u <service>` (see [[Logs]]) when a service fails, before making configuration changes blindly.
- Be cautious disabling services you don't recognize — confirm what they do first, especially on a shared or production system.

# Common Mistakes

- Assuming a service is running because its process exists, without checking systemd's own status (a process can be running but the unit itself reports "failed").
- Editing a unit file directly without running `systemctl daemon-reload` afterward, so changes don't take effect.
- Disabling or masking a security-relevant service (e.g. a firewall or logging agent) while troubleshooting, and forgetting to re-enable it.

# Related CORE Notes

- [[Terminal]]
- [[Logs]]
- [[Systemd_Service_Check_Lab]]
- [[Hardening]]

# Sources

- systemd project documentation — https://systemd.io/
