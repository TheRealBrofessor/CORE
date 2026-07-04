---
title: Claude Code
area: ai-tooling
difficulty: intermediate
status: draft
last_reviewed: 2026-07-04
sources:
  - "Anthropic, Claude Code documentation, https://docs.anthropic.com/en/docs/claude-code"
tags:
  - ai-tooling
  - claude-code
---

# What It Is

Claude Code is Anthropic's agentic command-line coding tool. It runs in a terminal (or IDE integration), can read/write files, run shell commands, and use additional tools, operating under a permission model that can prompt for approval on riskier actions.

# Why It Matters

Agentic coding tools like Claude Code can meaningfully speed up real engineering work, but because they can execute commands and modify files directly, using them safely requires understanding their permission model — not just their chat interface.

# When To Use It

For hands-on coding tasks — exploring a codebase, implementing a feature, debugging, or repository maintenance — where having the tool read/run/edit directly is more efficient than copy-pasting into a chat window.

# How To Use It Safely

- Review permission prompts before approving actions, especially destructive ones (deleting files, force-pushing, rewriting history).
- Keep project-specific guidance in a `CLAUDE.md` file (as this repository does) so the tool has explicit, durable scope boundaries.
- Use version control (Git) so any unwanted change is easy to review and revert.
- Don't grant broader permissions than a task needs "to save time" — scope matches risk.

# Common Mistakes

- Approving destructive actions (like force-push or history rewrite) without understanding the consequence.
- Not keeping the repository under version control, so there's no easy way to review or undo agent changes.
- Assuming the tool has context it wasn't actually given — be explicit about constraints in your prompt or in `CLAUDE.md`.

# Related CORE Notes

- [[Prompting]]
- [[AI_Safety_Workflows]]
- [[Codex]]
- [[Git]]

# Sources

- Anthropic, Claude Code documentation — https://docs.anthropic.com/en/docs/claude-code
