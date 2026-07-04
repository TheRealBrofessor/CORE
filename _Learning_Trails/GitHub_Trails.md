---
title: GitHub Trails
area: learning-trails
question: I accidentally committed a secret to a public GitHub repo — what now?
difficulty: beginner
status: draft
created: 2026-07-04
last_reviewed: 2026-07-04
sources:
tags:
  - learning-trail
  - github
  - git
---

# Question

I accidentally committed an API key/secret to a public GitHub repo. Deleting the file in a new commit removed it from the current view — is that enough?

# Why It Matters

This is a extremely common real mistake, and the intuitive fix (delete the file, commit again) is not actually sufficient — understanding why matters for anyone using Git/GitHub at all.

# Path Followed

Started at [[Git]] to understand that commit history is additive — a new commit deleting a file doesn't remove it from earlier commits, which are still fully accessible. Went to [[GitHub]] for how a public repo's full history (including old commits) is visible to anyone unless explicitly rewritten. Cross-referenced the [[Repo_Audit_Checklist]], which explicitly calls out checking history (not just the current tree) for secrets.

# Source Path

GitHub Docs on secret scanning (via [[GitHub]]'s Sources section) for how GitHub itself treats this class of problem.

# Answer

Deleting a file in a later commit does not remove it from history — anyone can still find it in an earlier commit via `git log`. The actual fix requires treating the secret as already compromised (rotate/revoke it immediately at the source, e.g. the API provider) regardless of what's done to the repo, and separately deciding whether to rewrite history (`git filter-repo`/BFG or similar) to scrub it from the repo itself — a deliberate, disruptive action, not a routine one (see [[Repo_Audit_Checklist]]'s "Mistakes to Avoid" section).

# What This Unlocks

Understanding that in Git, "delete" and "remove from history" are different operations — directly useful the next time a [[Repo_Audit_Checklist]] pass turns up something unexpected in old history.

# Next Questions

What's the safest, least-disruptive way to rewrite Git history to remove a secret from every commit, given that it requires a force-push?
