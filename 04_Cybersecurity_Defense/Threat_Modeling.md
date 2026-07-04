---
title: Threat Modeling
area: defense
difficulty: intermediate
status: draft
last_reviewed: 2026-07-04
sources:
  - "OWASP Threat Modeling, https://owasp.org/www-community/Threat_Modeling"
tags:
  - defense
  - threat-modeling
---

# What It Is

Threat modeling is systematically asking: what am I protecting, who might want to compromise it, how could they do it, and what's the impact if they succeed. A common simple frame is STRIDE (Spoofing, Tampering, Repudiation, Information disclosure, Denial of service, Elevation of privilege).

# Why It Matters

Without a threat model, security effort gets spread evenly (or randomly) instead of focused on what actually matters. It turns "make this secure" into a specific, prioritized list of risks to address.

# When To Use It

Before hardening a system ([[Hardening]]), when designing a new service, or when deciding what to monitor ([[Logging_Monitoring]]) and what a lab or playbook should actually check.

# How To Use It Safely

- Start by listing assets (data, systems) and their value/sensitivity, not attack techniques.
- Identify realistic threat actors for your context — a personal server and a bank have very different realistic threats.
- Rank risks by likelihood × impact, not by how interesting the attack sounds.
- Keep the output actionable: each identified risk should map to a concrete mitigation or accepted risk decision.

# Common Mistakes

- Jumping straight to "attacks" without first defining what's being protected and why.
- Treating threat modeling as a one-time exercise instead of revisiting it as the system changes.
- Over-indexing on exotic threats while ignoring mundane, high-likelihood ones (weak passwords, unpatched software).

# Related CORE Notes

- [[Security_Basics]]
- [[Hardening]]
- [[Repo_Audit_Checklist]]

# Sources

- OWASP, *Threat Modeling* — https://owasp.org/www-community/Threat_Modeling
