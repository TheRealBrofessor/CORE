---
title: TCP/IP
area: networking
difficulty: beginner
status: draft
last_reviewed: 2026-07-04
sources:
  - "RFC 791, Internet Protocol"
  - "RFC 793, Transmission Control Protocol"
tags:
  - networking
  - tcp-ip
---

# What It Is

IP (Internet Protocol) gives every device an address and handles routing packets between networks. TCP (Transmission Control Protocol) runs on top of IP and adds reliability: ordered delivery, retransmission of lost packets, and connection setup/teardown (the three-way handshake). UDP is the simpler, connectionless alternative to TCP — faster, but no delivery guarantee.

# Why It Matters

TCP/IP is the addressing and transport layer underneath essentially all internet and local network traffic covered elsewhere in this vault (DNS, HTTP, VPNs). Understanding it turns "the network is broken" into a specific, diagnosable layer.

# When To Use It

When diagnosing connectivity issues, reading packet captures, or reasoning about firewall rules (which typically operate on IP addresses, ports, and protocol).

# How To Use It Safely

- Use `ping` and `traceroute`/`traceroute6` against systems you own or are authorized to test, to check basic reachability and routing.
- Understand that a port being closed/filtered is often intentional (firewall) — don't treat probing as a substitute for authorized testing.
- Only run active network scanning or probing tools against networks and hosts you have explicit permission to test — see [[Threat_Modeling]] and [[Network_Triage]].

# Common Mistakes

- Confusing IP address (network-layer identity, can change) with the actual device.
- Assuming TCP guarantees are also true of UDP (they aren't — UDP has no retransmission or ordering).
- Treating "ping works" as proof that a specific service/port is reachable — ICMP (ping) and the target service's port are different things.

# Related CORE Notes

- [[Networking_Basics]]
- [[DNS]]
- [[HTTP]]
- [[Packet_Capture]]

# Sources

- RFC 791, *Internet Protocol* — https://www.rfc-editor.org/rfc/rfc791
- RFC 793, *Transmission Control Protocol* — https://www.rfc-editor.org/rfc/rfc793
