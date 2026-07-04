---
title: Domain OSINT
area: osint
difficulty: intermediate
status: draft
last_reviewed: 2026-07-04
sources:
  - "ICANN, WHOIS overview, https://www.icann.org/resources/pages/whois-2017-06-20-en"
tags:
  - osint
  - domain
---

# What It Is

Domain OSINT is researching a domain's public footprint using passive, publicly available sources: WHOIS/RDAP registration data, DNS records ([[DNS]]), TLS certificate transparency logs, and historical snapshots (e.g. web archives).

# Why It Matters

Domain infrastructure research is a core, purely passive verification technique — useful for judging whether a website is what it claims to be, without ever interacting with the site's actual application.

# When To Use It

When verifying claims about who operates a website, how long it has existed, or how its infrastructure has changed over time.

# How To Use It Safely

- Stick to passive, publicly published data sources (WHOIS/RDAP, public DNS, certificate transparency logs, web archives) — this requires no direct interaction with the target beyond ordinary DNS/WHOIS lookups.
- Understand privacy-protected WHOIS records are common and legitimate; absence of an owner's name is not itself suspicious.
- Do not use domain research as a pretext for probing, scanning, or attempting access to systems behind the domain — that is out of scope for CORE.

# Common Mistakes

- Treating WHOIS registrant data as always accurate or current — privacy services and inconsistent updates are common.
- Confusing domain age with legitimacy — new domains aren't automatically suspicious, and old domains aren't automatically trustworthy.
- Drawing conclusions from a single data point instead of corroborating across DNS history, certificate logs, and archived snapshots.

# Related CORE Notes

- [[DNS]]
- [[Source_Ranking]]
- [[Verification_Methods]]
- [[Source_Verification_Lab]]

# Sources

- ICANN, *WHOIS overview* — https://www.icann.org/resources/pages/whois-2017-06-20-en
