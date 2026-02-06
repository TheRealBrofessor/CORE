# Web Reference Hub

## Core model
- **Browser/Client** sends requests to a **server**
- Requests are shaped by **URL + method + headers + body**
- Servers respond with **status + headers + body**
- **State** is typically carried via **cookies**, **tokens**, or server-side session stores

## Key concepts
- Methods: GET/POST/PUT/PATCH/DELETE
- Status codes: 2xx success, 3xx redirect, 4xx client error, 5xx server error
- Cookies: storage + session identifiers
- CORS: controls cross-origin reads in browsers
- Auth: sessions vs tokens (JWT) vs API keys

## Tools
- `curl` (raw HTTP)
- browser devtools (network tab)
- `openssl s_client` (TLS inspection)

## Links
- Intermediate notes: `../../notes/intermediate/web/index.md`
- Cheatsheet: `../../notes/cheatsheets/http.md`
- Lab: `../../notes/labs/http-basics.md`
