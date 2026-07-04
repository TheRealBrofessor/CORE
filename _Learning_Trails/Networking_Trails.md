---
title: Networking Trails
area: learning-trails
question: My site works in a browser but "dig" shows a different IP than I expected — is something wrong?
difficulty: beginner
status: draft
created: 2026-07-04
last_reviewed: 2026-07-04
sources:
tags:
  - learning-trail
  - networking
  - dns
---

# Question

My site loads fine in a browser, but when I run `dig` I see a different IP than I expected. Is something wrong or compromised?

# Why It Matters

This is a very common source of unnecessary alarm — the mismatch is often completely normal, but it looks alarming without the right background.

# Path Followed

Started at [[DNS]] to understand how name resolution actually works, then did the [[DNS_Lookup_Lab]] to query the same domain against two different public resolvers directly. Cross-referenced [[TCP_IP]] for how a single domain can legitimately resolve to different IPs (load balancing, CDNs, geo-based routing).

# Source Path

RFC 1035 (via [[DNS]]'s Sources section) confirmed DNS answers aren't required to be identical across every resolver/location, especially for CDN-served or geo-distributed domains.

# Answer

A domain resolving to different IPs from different locations/resolvers is commonly normal behavior for sites behind a CDN or load balancer — not evidence of compromise. It becomes worth investigating only if the browser itself is also resolving unexpectedly (which would suggest a local DNS/hosts-file issue) or if the returned IP doesn't belong to any plausible, known infrastructure for that domain (a case for [[Domain_OSINT]] and [[Verification_Methods]]).

# What This Unlocks

A calibrated sense of "unusual but explainable" vs. "actually suspicious" — directly useful for [[Network_Triage]].

# Next Questions

How would I actually confirm which CDN/provider a domain's IP belongs to, passively?
