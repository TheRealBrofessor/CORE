# Networking Cheatsheet

## DNS
- `dig +short A example.com`
- `dig +trace example.com`

## HTTP
- `curl -I https://example.com`
- `curl -v https://example.com`

## Ports / sockets
- `ss -tulpn`
- `nc -vz host 443`
