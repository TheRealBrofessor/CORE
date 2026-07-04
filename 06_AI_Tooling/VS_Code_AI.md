---
title: VS Code AI Features
area: ai-tooling
difficulty: beginner
status: draft
last_reviewed: 2026-07-04
sources:
  - "Visual Studio Code documentation, https://code.visualstudio.com/docs"
tags:
  - ai-tooling
  - vs-code
---

# What It Is

VS Code supports AI-assisted coding through built-in features and extensions (e.g. inline completions, chat panels, and agent integrations from multiple providers) layered on top of the standard editor.

# Why It Matters

Many developers' first exposure to AI coding tools is inline, inside the editor they already use daily, rather than through a separate CLI tool. Understanding what's happening (what's sent where, what gets auto-applied) matters for safe day-to-day use.

# When To Use It

For inline suggestions and quick in-editor AI assistance while writing code, as a complement to (not necessarily a replacement for) a dedicated agentic CLI tool like [[Claude_Code]] or [[Codex]] for larger multi-file tasks.

# How To Use It Safely

- Review inline suggestions before accepting them, especially for security-sensitive code (auth, input handling, permissions).
- Know which extension/provider you're using and what data-handling policy applies to your code.
- Keep extensions updated and only install AI extensions from verified publishers.

# Common Mistakes

- Auto-accepting suggestions without reading them, especially multi-line completions.
- Not realizing an installed AI extension may send code context to a third-party service — check the extension's documentation.
- Assuming inline suggestions are tested/correct rather than statistically likely completions.

# Related CORE Notes

- [[Prompting]]
- [[Claude_Code]]
- [[Codex]]

# Sources

- Visual Studio Code documentation — https://code.visualstudio.com/docs
