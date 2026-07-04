---
title: Network Triage
area: playbooks
difficulty: intermediate
status: draft
last_reviewed: 2026-07-04
sources:
tags:
  - playbook
  - networking
  - triage
---

# Purpose

A structured approach to diagnosing a network connectivity or unexpected-traffic problem on a system you administer.

# Use Case

Use when a service is unreachable, a connection is unexpectedly slow, or you suspect unusual outbound/inbound traffic.

# Checklist

- [ ] Confirm the exact symptom: which host, which port, which direction (inbound/outbound).
- [ ] Check basic reachability (see [[TCP_IP]]).
- [ ] Check DNS resolution is correct for any hostname involved (see [[DNS]]).
- [ ] Check the firewall rules for the relevant port/direction.
- [ ] Check what's actually listening on the relevant port locally.
- [ ] If needed, capture traffic directly to see ground truth (see [[Packet_Capture]]).
- [ ] Check logs for the relevant service/time window (see [[Logs]]).

# Commands or Actions

```
ping <host>                       # basic reachability (ICMP)
dig <hostname> A +short           # DNS resolution
ss -tulpn                         # what's listening locally
sudo ufw status verbose           # firewall rules (or iptables/nftables equivalent)
sudo tcpdump -i <interface> host <ip> -c 20   # targeted, short capture
```

# Evidence to Capture

- Exact error messages or symptoms as observed, with timestamps.
- Output of reachability/DNS checks at time of investigation.
- A short, targeted packet capture if the issue isn't resolved by the above (see [[Packet_Capture_Reading_Lab]] for capture technique).

# Mistakes to Avoid

- Assuming "ping works" means the actual service/port is reachable — see [[TCP_IP]].
- Changing firewall rules experimentally on a production system without a rollback plan.
- Capturing traffic broadly instead of filtering to the specific host/port in question.

# Related CORE Notes

- [[TCP_IP]]
- [[DNS]]
- [[Packet_Capture]]
- [[Troubleshooting]]

# Sources

- RFC 1180, *A TCP/IP Tutorial* — https://www.rfc-editor.org/rfc/rfc1180
