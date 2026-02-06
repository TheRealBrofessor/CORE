# Linux Reference Hub

## Core concepts
- **Everything is a file**: devices, sockets, and config are exposed as filesystem objects.
- **Users/Groups**: permissions are evaluated via UID/GID and file mode bits.
- **Processes**: each process has PID, owner, environment, open files, and network sockets.

## Common tasks
- Inspect files/dirs: `ls -la`, `stat`
- Search: `find`, `grep -R`, `ripgrep (rg)`
- Processes: `ps aux`, `top`, `htop`, `pgrep`, `kill`
- Services (systemd): `systemctl status|start|stop <svc>`
- Logs: `journalctl -u <svc> -e`, `/var/log/*`
- Networking: `ip a`, `ss -tulpn`, `curl`, `dig`

## Permission model (quick)
- Mode bits: `rwxrwxrwx` for user/group/other
- Ownership: `chown user:group file`
- Special bits: SUID/SGID/sticky

## Links
- Beginner notes: `../../notes/beginner/linux/index.md`
- Checklist: `../checklists/linux-baseline.md`
- Cheatsheet: `../../notes/cheatsheets/linux-cli.md`
