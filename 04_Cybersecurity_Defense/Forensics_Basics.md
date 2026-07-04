---
title: Forensics Basics
area: defense
difficulty: advanced
status: draft
last_reviewed: 2026-07-04
sources:
  - "NIST SP 800-86, Guide to Integrating Forensic Techniques into Incident Response"
tags:
  - defense
  - forensics
---

# What It Is

Digital forensics is the practice of preserving, collecting, and analyzing digital evidence in a way that maintains its integrity — commonly summarized as maintaining a chain of custody and working from copies, never the original evidence, whenever possible.

# Why It Matters

Evidence handled carelessly during an incident can become unusable (or legally inadmissible) later. Basic forensic awareness protects your ability to fully understand and prove what happened, even if you never intend to pursue legal action.

# When To Use It

As part of [[Incident_Response]], whenever the scope of an incident is unclear and understanding "what actually happened" matters — before drawing conclusions from partial information.

# How To Use It Safely

- Work from a copy/image of evidence, not the original, whenever feasible.
- Record who accessed evidence, when, and why (chain of custody), even informally, for anything that might matter later.
- Note volatile evidence (running processes, network connections, memory contents) is lost on reboot — capture it first if it's relevant and safe to do so.
- This note is conceptual background only. CORE does not include real case files, real forensic evidence, or real-world investigation material — see [[CORE_Principles]].

# Common Mistakes

- Analyzing evidence directly on the original system/disk, altering timestamps or other artifacts in the process.
- Assuming a single artifact (one log line, one file) tells the whole story without corroboration.
- Treating forensics as something only needed for legal proceedings — it's equally valuable for internal root-cause understanding.

# Related CORE Notes

- [[Incident_Response]]
- [[Logging_Monitoring]]
- [[Log_Review_Lab]]

# Sources

- NIST SP 800-86, *Guide to Integrating Forensic Techniques into Incident Response* — https://csrc.nist.gov/pubs/sp/800/86/final
