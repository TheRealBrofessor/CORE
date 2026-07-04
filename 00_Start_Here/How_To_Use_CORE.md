---
title: How To Use CORE
area: start-here
difficulty: beginner
status: draft
last_reviewed: 2026-07-04
sources:
tags:
  - start-here
  - navigation
---

# How To Use CORE

## In Obsidian

1. Clone the repository to your machine.
2. Open Obsidian → `Open folder as vault` → select the cloned `CORE` folder.
3. Use `Ctrl/Cmd+O` (Quick Switcher) to open any note by name.
4. Use `Ctrl/Cmd+Shift+F` (or the search panel) to search all note content.
5. Click any `[[wiki link]]` to jump to the linked note. Unresolved links (shown differently by Obsidian) usually mean a note hasn't been written yet — that's expected in an evolving vault.
6. Use the Graph View if you want a visual map of how notes connect, though it is not required to use CORE effectively.

## On GitHub

`[[wiki links]]` do not render as clickable links on GitHub — this is a known, accepted tradeoff for staying plugin-free in Obsidian. On GitHub, navigate using:

- The folder structure itself (numbered folders = subject areas).
- Each folder's `*_Index.md` file, which lists every note in that folder with a plain relative link.
- [[Master_Index]] in `_Indexes/`, which links every subject area.

## Reading Order

CORE does not require reading folders in numeric order, but the numbering reflects a rough dependency order: Foundations before Linux, Linux before Networking-heavy topics, and so on. If you want a specific goal-oriented order, use a curated path in `_Indexes/` instead of reading folders top to bottom.

## Frontmatter Fields

Every topic note carries frontmatter (`title`, `area`, `difficulty`, `status`, `last_reviewed`, `sources`, `tags`). Use `difficulty` to judge if a note fits your current level, and `status` to see if a note is still a draft. `status: draft` does not mean incorrect — it means not yet fully reviewed against sources.

## Related CORE Notes

- [[Welcome]]
- [[CORE_Principles]]
- [[Master_Index]]
- [[Topic_Template]]

## Sources

- Internal — Obsidian usage patterns are standard Obsidian behavior, not CORE-specific.
