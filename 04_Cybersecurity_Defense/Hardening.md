---
title: System Hardening
area: defense
difficulty: intermediate
status: draft
last_reviewed: 2026-07-04
sources:
  - "CIS Benchmarks, https://www.cisecurity.org/cis-benchmarks"
tags:
  - defense
  - hardening
---

# What It Is

Hardening is reducing a system's attack surface: removing unnecessary software and services, applying least-privilege permissions, enabling firewalls, keeping software patched, and disabling default/weak configurations.

# Why It Matters

Most successful attacks exploit basic, known weaknesses (unpatched software, default credentials, unnecessary open services) rather than novel techniques. Hardening addresses the highest-likelihood risks identified in [[Threat_Modeling]].

# When To Use It

When setting up any new system exposed to a network, and periodically thereafter — see [[New_Linux_Box_Checklist]] and [[Basic_Hardening_Checklist]].

# How To Use It Safely

- Disable or remove services you don't actively use, rather than leaving them running "just in case."
- Apply the principle of least privilege to users, permissions ([[Permissions]]), and network access.
- Keep the OS and installed packages patched on a regular cadence.
- Change default credentials on any service before exposing it to a network.
- Test hardening changes in a non-production environment first when possible — some changes (e.g. disabling a service) can break functionality.

# Common Mistakes

- Hardening once at setup and never revisiting it as new software is installed.
- Disabling logging or monitoring agents "to reduce noise" — this removes visibility exactly where it matters (see [[Logging_Monitoring]]).
- Treating a firewall as sufficient on its own without also patching and minimizing running services.

# Related CORE Notes

- [[Permissions]]
- [[Threat_Modeling]]
- [[New_Linux_Box_Checklist]]
- [[Basic_Hardening_Checklist]]

# Sources

- CIS Benchmarks — https://www.cisecurity.org/cis-benchmarks
