# Lab: HTTP Basics

## Objective
Build intuition for request/response anatomy, redirects, headers, and TLS.

## Tasks
1) Inspect headers:
- `curl -I https://example.com`

2) Follow redirects:
- `curl -IL https://example.com`

3) See full exchange:
- `curl -v https://example.com`

4) Inspect TLS:
- `echo | openssl s_client -connect example.com:443 -servername example.com 2>/dev/null | openssl x509 -noout -issuer -subject -dates`

## Success criteria
You can explain:
- why redirects happen
- which headers matter for caching/security
- what the certificate issuer/expiry means
