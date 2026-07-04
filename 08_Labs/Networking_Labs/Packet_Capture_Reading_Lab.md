---
title: Packet Capture Reading Lab
area: labs
difficulty: intermediate
status: draft
last_reviewed: 2026-07-04
sources:
tags:
  - lab
  - networking
  - packet-capture
---

# Objective

Capture and read a short slice of your own machine's network traffic to reinforce [[Packet_Capture]] and [[TCP_IP]].

# Safety Scope

Capture only on an interface and network you own/administer (e.g. your own laptop's loopback or local Wi-Fi interface). Do not capture on shared/enterprise networks without explicit authorization, and do not capture on any interface where doing so would expose other people's traffic without their knowledge and consent.

# Requirements

- `tcpdump` (command line) or Wireshark installed.
- Sudo/administrator privileges (packet capture requires elevated access).

# Steps

1. Identify your network interfaces: `ip link show` (Linux) or `ifconfig` (macOS/older tools).
2. Start a short, filtered capture on your primary interface, limited to DNS traffic: `sudo tcpdump -i <interface> udp port 53 -c 10` (captures 10 packets and stops).
3. In another terminal, generate some DNS traffic: `dig example.com`.
4. Observe the captured packets in the first terminal — note source/destination IP and port.
5. Repeat with an HTTP-related filter if useful: `sudo tcpdump -i <interface> tcp port 443 -c 10`, then visit any HTTPS site in a browser.
6. If using Wireshark instead, apply a display filter like `dns` or `tcp.port == 443` on a similarly short capture.

# Expected Result

You should be able to point to a captured packet and correctly identify its source IP, destination IP, and port, and connect that back to the specific action (the `dig` command or the browser request) that generated it.

# Troubleshooting

- "Permission denied" on capture usually means you need `sudo` (Linux/macOS) or to run as Administrator (Windows/Npcap for Wireshark).
- No packets captured: confirm you selected the correct active interface (`ip link show` shows interface state).

# Cleanup

Delete any capture files (`.pcap`) you saved, if they aren't needed — they can contain more traffic detail than you intended to keep.

# Related CORE Notes

- [[Packet_Capture]]
- [[TCP_IP]]
- [[DNS]]

# Sources

- `man tcpdump` — standard on most Linux/macOS systems.
