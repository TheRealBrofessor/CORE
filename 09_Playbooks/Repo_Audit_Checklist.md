---
title: Repo Audit Checklist
area: playbooks
difficulty: beginner
status: draft
last_reviewed: 2026-07-04
sources:
tags:
  - playbook
  - github
  - audit
---

# Purpose

A checklist for auditing a Git repository's structure, history, and content before treating it as clean/trustworthy — the same kind of check used to prepare this vault's rebuild.

# Use Case

Use before adopting, publishing, or continuing work on a repository whose full history or contents you haven't reviewed, or periodically on a repository you maintain.

# Checklist

- [ ] Review the full commit history (`git log --oneline --all`) for unexpected content or resets.
- [ ] Check for committed secrets (API keys, credentials, tokens) — including in old history, not just the current tree.
- [ ] Check for unwanted build clutter (`node_modules`, `.venv`, `dist`, `build`, large binaries) and confirm `.gitignore` covers them.
- [ ] Check for content clearly out of scope for the repository's stated mission.
- [ ] Confirm the license, contributing guidelines, and code of conduct are present and accurate.
- [ ] Confirm README accurately describes current (not aspirational or outdated) repository state.
- [ ] Confirm no personal/sensitive data is present that shouldn't be public.

# Commands or Actions

```
git log --oneline --all | head -100
git log --diff-filter=A --name-only --all | sort -u   # every filename ever added
du -sh .git                                            # repo size sanity check
git status
```

# Evidence to Capture

- List of any concerning files/commits found, with commit hashes.
- Confirmation `.gitignore` was checked against actual tracked files (not just present but unused).

# Mistakes to Avoid

- Only checking the current working tree and ignoring history — secrets or clutter can persist in old commits even after later removal.
- Assuming a `.gitignore` file retroactively removes already-tracked files — it only prevents new files from being added.
- Rewriting history to scrub secrets without understanding the consequences (force-push required, breaks other clones) — treat this as a deliberate, separate decision, not a routine audit step.

# Related CORE Notes

- [[Git]]
- [[GitHub]]
- [[Threat_Modeling]]

# Sources

- GitHub Docs, secret scanning — https://docs.github.com/code-security/secret-scanning
