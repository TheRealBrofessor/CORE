---
title: Search Operators
area: osint
difficulty: beginner
status: draft
last_reviewed: 2026-07-04
sources:
  - "Google Search Help, Refine web searches, https://support.google.com/websearch/answer/2466433"
tags:
  - osint
  - search
---

# What It Is

Search operators are special syntax that narrow a search engine query: `"exact phrase"`, `site:example.com`, `-excludeword`, `filetype:pdf`, `intitle:word`, and similar modifiers, supported (with variation) by most major search engines.

# Why It Matters

Precise queries are the difference between finding a specific, verifiable source in seconds and scrolling through irrelevant results. This is the foundation skill for effective, low-noise OSINT verification.

# When To Use It

Any time a plain-language search returns too many irrelevant results, or when you need to confirm whether specific information exists on a specific site.

# How To Use It Safely

- Use operators only against publicly indexed, publicly available content — this is passive research, not intrusion.
- Combine operators (`site:` + `"exact phrase"`) to narrow results without needing advanced tools.
- Cross-check results across more than one search engine — indexes differ and no single engine is complete.

# Common Mistakes

- Assuming search engine results are complete or unbiased — ranking algorithms and indexing gaps mean absence of a result isn't proof of absence of information.
- Relying on operator syntax that's engine-specific without checking it's still supported (search engines change supported operators over time).
- Treating a search result snippet as the full context — always open and read the actual source.

# Related CORE Notes

- [[Source_Ranking]]
- [[Verification_Methods]]
- [[Source_Verification_Lab]]

# Sources

- Google Search Help, *Refine web searches* — https://support.google.com/websearch/answer/2466433
