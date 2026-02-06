# Networking Reference Hub

## Mental model
- **IP** routes packets between hosts
- **TCP** is reliable, ordered, connection-oriented
- **UDP** is connectionless, faster, no delivery guarantees
- **DNS** maps names → IPs
- **HTTP** is an application protocol usually over TCP (HTTPS adds TLS)

## Common commands
- Interfaces/IP: `ip a`, `ip r`
- Sockets: `ss -tulpn`
- DNS: `dig A example.com`, `dig +short`
- HTTP: `curl -v https://example.com`
- Tracing: `traceroute`, `mtr`
- Packet capture: `tcpdump -i <iface>`

## Ports (quick)
- 22 SSH
- 53 DNS
- 80 HTTP
- 443 HTTPS

## Links
- Beginner notes: `../../notes/beginner/networking/index.md`
- Checklist: `../checklists/network-debug.md`
- Cheatsheet: `../../notes/cheatsheets/networking.md`
