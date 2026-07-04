---
title: VPS Basics
area: cloud-devops
difficulty: intermediate
status: draft
last_reviewed: 2026-07-04
sources:
tags:
  - cloud-devops
  - vps
---

# What It Is

A VPS (Virtual Private Server) is a virtual machine rented from a cloud provider, giving you root/administrator access to what behaves like a dedicated Linux (or Windows) server, without owning physical hardware.

# Why It Matters

A VPS is often the first "real" internet-facing system someone administers directly, which makes it the natural place to apply [[Hardening]], [[Logging_Monitoring]], and basic [[Troubleshooting]] in practice rather than theory.

# When To Use It

When you need a persistent, internet-reachable server for a project, and a fully managed platform doesn't fit your needs.

# How To Use It Safely

- Apply basic hardening immediately on provisioning — see [[New_Linux_Box_Checklist]] and [[Basic_Hardening_Checklist]].
- Use SSH key authentication instead of password authentication where possible.
- Keep the system patched and minimize exposed services/ports.
- Enable a firewall (e.g. `ufw`/`nftables`) with default-deny inbound rules, opening only what's needed.
- Set up basic monitoring/logging from day one, not after an incident.

# Common Mistakes

- Leaving default credentials or an open root SSH login with password authentication enabled.
- Exposing services (databases, admin panels) directly to the internet without a firewall or VPN in front of them.
- Never patching after initial setup.

# Related CORE Notes

- [[Hardening]]
- [[New_Linux_Box_Checklist]]
- [[Basic_Hardening_Checklist]]
- [[Network_Triage]]

# Sources

- Internal — general VPS/server administration practice; provider-specific documentation should be consulted for exact steps.
