# Security Baseline Checklist

## Accounts & access
- [ ] MFA enabled on critical accounts
- [ ] Least privilege roles/policies
- [ ] No shared admin accounts

## Secrets
- [ ] No secrets committed to git
- [ ] Secrets stored in a vault / GitHub Secrets
- [ ] Rotation plan exists

## Dependencies
- [ ] Pin versions where possible
- [ ] Audit high-risk deps
- [ ] Remove unused deps

## Logging & detection
- [ ] Auth logs enabled and retained
- [ ] Alerts for suspicious login patterns
- [ ] Time sync enabled (NTP)

## Backup & recovery
- [ ] Backups exist
- [ ] Restore tested
