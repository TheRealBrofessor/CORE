---
title: Source Verification Checklist
area: playbooks
difficulty: beginner
status: draft
last_reviewed: 2026-07-04
sources:
tags:
  - playbook
  - osint
  - verification
---

# Purpose

A quick checklist to run before trusting, citing, or repeating any claim — the operational form of [[Verification_Methods]].

# Use Case

Use before adding a source to a CORE note, before repeating a claim publicly, or whenever a claim seems important enough to double-check.

# Checklist

- [ ] Have I traced this to its original/primary source, not just a re-share?
- [ ] Is there at least one independent corroborating source?
- [ ] Is the date current, and does the context still apply?
- [ ] Have I ranked the source type (primary/secondary/unverified) per [[Source_Ranking]]?
- [ ] Am I clearly separating verified fact from my own interpretation?
- [ ] If it's an image or media claim, have I checked it per [[Image_OSINT]]?
- [ ] If it's a domain/site claim, have I checked it per [[Domain_OSINT]]?

# Commands or Actions

- Use [[Search_Operators]] to trace the original source (`"exact phrase"`, `site:`).
- Use reverse image search for any image claim.
- Use `dig`/WHOIS for any domain claim.

# Evidence to Capture

- The original source URL/reference, not just the secondary one you first encountered.
- Your ranking of the source and reasoning for it.

# Mistakes to Avoid

- Treating repetition (many people sharing the same claim) as independent corroboration.
- Skipping this checklist for claims that "feel obviously true" — that's exactly when confirmation bias is strongest.
- Citing a source you haven't actually opened and read yourself.

# Related CORE Notes

- [[Verification_Methods]]
- [[Source_Ranking]]
- [[Search_Operators]]
- [[Source_Verification_Lab]]

# Sources

- IFLA, *How To Spot Fake News* — https://www.ifla.org/
