---
title: Blue Team Trails
area: learning-trails
question: I saw repeated failed SSH logins in my logs — is this an actual attack?
difficulty: beginner
status: draft
created: 2026-07-04
last_reviewed: 2026-07-04
sources:
tags:
  - learning-trail
  - defense
  - logs
---

# Question

I saw a lot of repeated failed SSH login attempts in my server's logs. Is this an actual attack, and what should I do?

# Why It Matters

This is one of the most common first "is this a real incident" moments for anyone running an internet-facing server, and it's a good test case for applying a calm, structured process instead of panicking.

# Path Followed

Started at [[Logs]] to confirm where SSH login attempts are actually recorded, then used the [[Log_Review_Lab]] approach to scope a time window and count failed attempts by source IP. Cross-referenced [[Threat_Modeling]] to reason about realistic risk (broad internet scanning vs. targeted attack), then [[Hardening]] and [[Basic_Hardening_Checklist]] for the actual fix.

# Source Path

NIST SP 800-61 Rev. 2 (via [[Incident_Response]]'s Sources section) for the general principle of triage-before-panic.

# Answer

Continuous low-volume failed SSH logins from many different IPs is extremely common background internet scanning, not a targeted attack — nearly every internet-facing SSH server sees this constantly. It becomes a real incident-response concern ([[Incident_Response]]) only if a login actually succeeds unexpectedly, or if failures are concentrated and persistent from a single source in a way that suggests targeting. The actual fix for the background noise is hardening (disable password auth, use SSH keys, consider rate-limiting or moving off the default port) rather than incident response.

# What This Unlocks

The judgment to distinguish "normal background noise" from "needs the full [[Incident_Response]] process" — a core blue-team skill.

# Next Questions

What specific hardening step reduces SSH brute-force noise the most, and how would I verify it worked?
