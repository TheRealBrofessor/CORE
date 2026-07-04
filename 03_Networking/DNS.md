---
title: DNS
area: networking
difficulty: beginner
status: draft
last_reviewed: 2026-07-04
sources:
  - "RFC 1035, Domain Names - Implementation and Specification"
tags:
  - networking
  - dns
---

# What It Is

DNS (Domain Name System) translates human-readable domain names (`example.com`) into IP addresses. It works as a distributed, hierarchical lookup: your resolver asks a chain of servers (root → TLD → authoritative) until it gets an answer, then caches it for a time-to-live (TTL) period.

# Why It Matters

DNS underlies nearly everything on the internet — browsing, email delivery, API calls. It's also a common point of both misconfiguration (site "down" because of DNS, not the server) and OSINT value (domain history, ownership, infrastructure) — see [[Domain_OSINT]].

# When To Use It

When a site or service is unreachable and you need to rule DNS in or out, or when investigating a domain's infrastructure for verification purposes.

# How To Use It Safely

- Use `dig` or `nslookup` for direct, read-only lookups — these are passive and safe against any public domain.
- Understand TTL/caching before concluding a DNS change "didn't work" — it may just not have propagated yet.
- When looking up domains for OSINT purposes, stick to passive lookups; don't send authenticated or intrusive requests to infrastructure you don't own.

# Common Mistakes

- Assuming a DNS change is instant — caching and TTLs mean propagation can take minutes to days.
- Confusing a domain registrar (where you register the name) with a DNS host/provider (where records actually live) — they're often, but not always, the same company.
- Treating WHOIS/DNS data as proof of who currently controls a domain — ownership and control can be more complex than a single record suggests (see [[Verification_Methods]]).

# Related CORE Notes

- [[TCP_IP]]
- [[HTTP]]
- [[Domain_OSINT]]
- [[DNS_Lookup_Lab]]

# Sources

- RFC 1035, *Domain Names - Implementation and Specification* — https://www.rfc-editor.org/rfc/rfc1035
