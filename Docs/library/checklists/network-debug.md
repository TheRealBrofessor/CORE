# Network Debug Checklist

## Layer 3/4
- [ ] `ip a` (correct IP?)
- [ ] `ip r` (default route present?)
- [ ] `ping -c 1 1.1.1.1` (raw connectivity)
- [ ] `ss -tulpn` (service actually listening)

## DNS
- [ ] `dig +short example.com`
- [ ] Check resolver config: `/etc/resolv.conf`

## HTTP
- [ ] `curl -v https://host`
- [ ] Check TLS errors and redirects

## Tracing
- [ ] `traceroute host` or `mtr host`
