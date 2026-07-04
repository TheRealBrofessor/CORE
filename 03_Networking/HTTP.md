---
title: HTTP
area: networking
difficulty: beginner
status: draft
last_reviewed: 2026-07-04
sources:
  - "MDN Web Docs, HTTP overview, https://developer.mozilla.org/en-US/docs/Web/HTTP"
tags:
  - networking
  - http
---

# What It Is

HTTP (Hypertext Transfer Protocol) is the request/response protocol the web runs on. A client sends a request (method, e.g. `GET`/`POST`, plus headers and sometimes a body) to a server, which returns a response (a status code, headers, and a body). HTTPS is HTTP layered over TLS encryption.

# Why It Matters

Almost every web-facing tool, API, and OSINT technique in this vault depends on understanding an HTTP request/response cycle: status codes, headers, and the difference between HTTP and HTTPS.

# When To Use It

When debugging why a web request fails, reading network logs, or verifying claims about a website (e.g. checking response headers or certificate info) — see [[Verification_Methods]].

# How To Use It Safely

- Use `curl -I` for a quick, low-impact header check instead of downloading full content repeatedly.
- Always prefer HTTPS; treat a plain HTTP login form as a red flag.
- Respect a site's `robots.txt` and terms of service when scripting requests, even for read-only OSINT purposes.
- Avoid sending large volumes of requests to any service you don't own — that crosses into denial-of-service territory, which is out of scope for CORE.

# Common Mistakes

- Treating a `200 OK` status as proof of "success" in every case — some apps return 200 with an error message in the body.
- Confusing HTTP status code categories (2xx success, 3xx redirect, 4xx client error, 5xx server error).
- Assuming HTTPS alone means a site is trustworthy — it verifies encryption and the certificate's domain match, not the content's honesty (see [[Verification_Methods]]).

# Related CORE Notes

- [[TCP_IP]]
- [[DNS]]
- [[Verification_Methods]]

# Sources

- MDN Web Docs, *HTTP overview* — https://developer.mozilla.org/en-US/docs/Web/HTTP
