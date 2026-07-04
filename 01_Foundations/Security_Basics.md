---
title: Security Basics
area: foundations
difficulty: beginner
status: draft
last_reviewed: 2026-07-04
sources:
  - "NIST SP 800-12, An Introduction to Information Security"
tags:
  - foundations
  - security
---

# What It Is

Information security is the practice of protecting the confidentiality, integrity, and availability (the "CIA triad") of data and systems. Confidentiality means only authorized parties can read data; integrity means data isn't altered without authorization; availability means systems work when needed.

# Why It Matters

Every defensive topic in CORE ([[Hardening]], [[Logging_Monitoring]], [[Incident_Response]], [[Threat_Modeling]]) is really a different angle on protecting one or more parts of the CIA triad. Having this frame makes it easy to categorize any new security concept you encounter.

# When To Use It

Whenever you're evaluating a security control or incident and want to know what it's actually protecting — ask which part of the CIA triad is at risk.

# How To Use It Safely

- Security learning in CORE is defensive-only: hardening your own systems, detecting and responding to threats, and verifying information (OSINT). See [[CORE_Principles]].
- Never test security controls against systems you don't own or don't have explicit written authorization to test.

# Common Mistakes

- Treating "security" as one undifferentiated thing instead of specific properties (confidentiality/integrity/availability) that can be improved independently.
- Assuming more security controls always mean better security — controls have usability and maintenance costs, and threat modeling ([[Threat_Modeling]]) exists to target effort where it matters.

# Related CORE Notes

- [[Threat_Modeling]]
- [[Hardening]]
- [[Defense_Index]]

# Sources

- NIST SP 800-12 Rev. 1, *An Introduction to Information Security* — https://csrc.nist.gov/pubs/sp/800/12/r1/final
