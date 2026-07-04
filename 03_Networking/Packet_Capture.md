---
title: Packet Capture
area: networking
difficulty: intermediate
status: draft
last_reviewed: 2026-07-04
sources:
  - "Wireshark User's Guide, https://www.wireshark.org/docs/wsug_html_chunked/"
tags:
  - networking
  - packet-capture
---

# What It Is

Packet capture is recording raw network traffic as it crosses an interface, using tools like `tcpdump` (command line) or Wireshark (GUI), so it can be inspected protocol-by-protocol.

# Why It Matters

Packet capture is ground truth for network troubleshooting and defensive monitoring — it shows exactly what was sent, rather than what a log or application claims happened. It's a core blue-team skill for verifying incidents (see [[Incident_Response]]).

# When To Use It

When higher-level tools (logs, application errors) don't explain a network problem, or when you need to confirm exactly what traffic left or entered a system you own or administer.

# How To Use It Safely

- Only capture traffic on networks and interfaces you own or are explicitly authorized to monitor — packet capture on shared networks can expose other users' traffic.
- Use capture filters (e.g. by host/port) to limit scope to what's relevant, both for noise reduction and privacy.
- Treat captured traffic as sensitive data — it can contain credentials or personal information in cleartext protocols.
- Use read-only analysis (Wireshark's "Follow Stream", filters) rather than replaying or injecting traffic.

# Common Mistakes

- Capturing on the wrong interface and getting no relevant traffic.
- Capturing everything with no filter, producing an unmanageable amount of data.
- Forgetting that capturing on a switched network only sees traffic to/from/broadcast on your own port unless you've deliberately configured mirroring — you're not automatically seeing "everything" on the LAN.

# Related CORE Notes

- [[TCP_IP]]
- [[Logging_Monitoring]]
- [[Packet_Capture_Reading_Lab]]

# Sources

- Wireshark User's Guide — https://www.wireshark.org/docs/wsug_html_chunked/
