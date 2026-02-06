# Playbook: Suspicious Login Investigation

## Trigger
- Unexpected login alert
- Impossible travel / new device
- Multiple failed attempts

## Triage (10 minutes)
- Identify account, timestamp, source IP, user agent
- Confirm whether user initiated the login
- Check MFA events

## Containment
- Reset password and revoke active sessions/tokens
- Rotate keys if any were exposed
- Temporarily lock account if needed

## Investigation
- Review recent privileged actions
- Check for new SSH keys / API tokens / OAuth grants
- Search logs for lateral movement or data access

## Recovery
- Restore access to user with clean device + MFA
- Remove malicious keys/tokens/apps
- Document and add detection rules

## Output
- Timeline
- Evidence (IPs, UAs, tokens)
- Root cause and prevention
