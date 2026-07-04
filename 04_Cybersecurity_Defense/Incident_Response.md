---
title: Incident Response
area: defense
difficulty: intermediate
status: draft
last_reviewed: 2026-07-04
sources:
  - "NIST SP 800-61 Rev. 2, Computer Security Incident Handling Guide"
tags:
  - defense
  - incident-response
---

# What It Is

Incident response is the structured process for handling a suspected or confirmed security incident, commonly broken into phases: preparation, detection & analysis, containment, eradication, recovery, and post-incident review.

# Why It Matters

Reacting to an incident without a process leads to lost evidence, incomplete containment, and repeat incidents from the same root cause. A defined process keeps a stressful situation methodical.

# When To Use It

The moment you suspect (not just confirm) unauthorized access, malware, data exposure, or anomalous system behavior.

# How To Use It Safely

- Preserve evidence before making changes where possible — see [[Forensics_Basics]] and don't reboot/wipe a system as a first reaction unless containment requires it.
- Contain first (isolate the affected system from the network) before fully eradicating, so you don't destroy evidence of scope.
- Document a timeline as you go — what was observed, when, and what actions were taken.
- Do a post-incident review focused on root cause and process improvement, not blame.
- Stay within your own systems and authorization — CORE's incident response guidance is for defending systems you own or administer, not investigating third parties.

# Common Mistakes

- Immediately reimaging/rebooting a compromised system before capturing volatile evidence (running processes, network connections, memory) if that evidence might be needed.
- Treating containment as the end of the process and skipping root-cause eradication, leading to reinfection.
- Skipping the post-incident review, so the same gap gets exploited again.

# Related CORE Notes

- [[Logging_Monitoring]]
- [[Forensics_Basics]]
- [[Suspicious_Process_Check]]
- [[Network_Triage]]

# Sources

- NIST SP 800-61 Rev. 2, *Computer Security Incident Handling Guide* — https://csrc.nist.gov/pubs/sp/800/61/r2/final
