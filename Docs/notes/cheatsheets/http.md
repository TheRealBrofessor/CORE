# HTTP Cheatsheet

## Quick curl
- Headers only: `curl -I https://example.com`
- Verbose: `curl -v https://example.com`
- POST JSON:
  - `curl -X POST https://host/api -H 'Content-Type: application/json' -d '{"a":1}'`

## Common status codes
- 200 OK
- 301/302 Redirect
- 400 Bad Request
- 401 Unauthorized
- 403 Forbidden
- 404 Not Found
- 429 Too Many Requests
- 500 Internal Server Error
- 502/503 Gateway/Service issues

## Cookies
- View: `curl -I https://host`
- Send: `curl -H 'Cookie: name=value' https://host`
