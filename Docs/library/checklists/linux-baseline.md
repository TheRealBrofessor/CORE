# Linux Baseline Checklist

## Identity & access
- [ ] Create non-root user; disable password SSH if possible
- [ ] Confirm sudoers minimal
- [ ] Disable unused accounts/services

## Patch state
- [ ] `sudo apt update && sudo apt upgrade`
- [ ] Reboot if kernel upgraded

## Services
- [ ] `systemctl --type=service --state=running`
- [ ] Disable anything not needed

## Network exposure
- [ ] `ss -tulpn` review listeners
- [ ] Firewall enabled (ufw/nftables)

## Logging
- [ ] `journalctl -p warning -b`
- [ ] Verify logs stored and rotated
