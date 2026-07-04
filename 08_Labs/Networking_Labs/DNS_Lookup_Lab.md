---
title: DNS Lookup Lab
area: labs
difficulty: beginner
status: draft
last_reviewed: 2026-07-04
sources:
tags:
  - lab
  - networking
  - dns
---

# Objective

Practice using `dig`/`nslookup` to inspect DNS records directly, reinforcing [[DNS]].

# Safety Scope

Fully passive, read-only public DNS lookups against domains you own or well-known public domains (e.g. a domain you control, or widely-used public sites for observation only). No active scanning or interaction beyond standard DNS queries.

# Requirements

- `dig` or `nslookup` installed (most Linux/macOS systems have one or both; Windows can use `nslookup` natively or install `dig` via WSL).

# Steps

1. Look up the A record (IPv4 address) of a domain: `dig example.com A +short`.
2. Look up the MX records (mail servers): `dig example.com MX +short`.
3. Look up the NS records (authoritative name servers): `dig example.com NS +short`.
4. Check the TTL (time-to-live) of the A record: `dig example.com A` (look at the number in the answer section, in seconds).
5. Query a specific DNS server directly instead of your default resolver: `dig @1.1.1.1 example.com A +short`.
6. Compare results from two different public resolvers (e.g. `1.1.1.1` and `8.8.8.8`) — they should normally match for a stable domain.

# Expected Result

You should be able to explain what each record type returned means, and explain why TTL affects how quickly a DNS change would be visible to you.

# Troubleshooting

- If `dig` isn't found, use `nslookup example.com` as a fallback (less detailed output).
- If results differ between resolvers, consider whether the domain uses geo-based or load-balanced DNS responses before assuming an error.

# Cleanup

None required — this lab makes no persistent changes.

# Related CORE Notes

- [[DNS]]
- [[TCP_IP]]
- [[Domain_OSINT]]

# Sources

- `man dig` — standard on most Linux/macOS systems with `bind-utils`/`dnsutils` installed.
