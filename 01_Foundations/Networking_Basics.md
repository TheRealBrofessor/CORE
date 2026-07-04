---
title: Networking Basics
area: foundations
difficulty: beginner
status: draft
last_reviewed: 2026-07-04
sources:
  - "RFC 1180, A TCP/IP Tutorial"
tags:
  - foundations
  - networking
---

# What It Is

A network is a set of devices that can exchange data using agreed-upon rules (protocols). The internet is a network of networks, held together by a common addressing scheme (IP) and common transport rules (TCP/UDP).

# Why It Matters

Every service you use — a website, an app, a game — depends on devices finding each other and exchanging data reliably. Understanding the basic model (addresses, ports, packets) makes the deeper topics in [[Networking_Index]] much easier to absorb.

# When To Use It

Whenever you need to reason about why two devices can or can't communicate — the starting point for almost all network troubleshooting.

# How To Use It Safely

This is conceptual background; the safety consideration is in how you apply it — only test connectivity or probe systems you own or are explicitly authorized to test. See [[Threat_Modeling]] and [[Network_Triage]] for safe, defensive application.

# Common Mistakes

- Treating "the internet" as one thing instead of a stack of separate concerns (addressing, routing, transport, application protocols).
- Confusing a device's IP address with its identity — addresses can change, be shared (NAT), or be spoofed.

# Related CORE Notes

- [[TCP_IP]]
- [[DNS]]
- [[HTTP]]
- [[Networking_Index]]

# Sources

- RFC 1180, *A TCP/IP Tutorial* — https://www.rfc-editor.org/rfc/rfc1180
