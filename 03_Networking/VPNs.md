---
title: VPNs
area: networking
difficulty: beginner
status: draft
last_reviewed: 2026-07-04
sources:
  - "NIST SP 800-77 Rev. 1, Guide to IPsec VPNs"
tags:
  - networking
  - vpn
---

# What It Is

A VPN (Virtual Private Network) creates an encrypted tunnel between your device and a VPN server, routing your traffic through that server. It hides traffic contents and your IP address from networks between you and the VPN server, and from destination sites (which see the VPN server's IP instead of yours).

# Why It Matters

VPNs are widely marketed with claims that go beyond what they technically do. Understanding the real boundary of what's protected (and what isn't) matters both for personal use and for evaluating security claims in general — a good example of applying [[Verification_Methods]] to a product claim.

# When To Use It

When you want to encrypt traffic on an untrusted network (e.g. public Wi-Fi) or mask your IP address from the destination site — not as a general-purpose "security fix."

# How To Use It Safely

- Understand a VPN moves trust from your local network/ISP to the VPN provider — the provider can see your traffic unless it's separately encrypted (e.g. HTTPS).
- Verify a provider's logging policy and jurisdiction claims independently rather than taking marketing copy at face value.
- A VPN does not make you anonymous by itself, does not stop malware, and does not verify the legitimacy of sites you visit.

# Common Mistakes

- Believing a VPN provides full anonymity — DNS leaks, browser fingerprinting, and account logins can still identify you.
- Assuming all VPN protocols are equally secure — protocol and implementation matter (e.g. modern WireGuard vs. legacy PPTP).
- Using a free VPN without understanding its business model — free services often monetize traffic/data in some way.

# Related CORE Notes

- [[TCP_IP]]
- [[Verification_Methods]]
- [[Security_Basics]]

# Sources

- NIST SP 800-77 Rev. 1, *Guide to IPsec VPNs* — https://csrc.nist.gov/pubs/sp/800/77/r1/final
