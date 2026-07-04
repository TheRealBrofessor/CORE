---
title: Codex
area: ai-tooling
difficulty: intermediate
status: draft
last_reviewed: 2026-07-04
sources:
  - "OpenAI, Codex documentation, https://developers.openai.com/codex"
tags:
  - ai-tooling
  - codex
---

# What It Is

Codex is OpenAI's agentic coding tool/agent, available via CLI and IDE integrations, that can read a codebase, propose or make changes, and run commands to help complete engineering tasks — conceptually similar in role to [[Claude_Code]], from a different provider.

# Why It Matters

Codex is one of the mainstream options for agentic AI coding work. Understanding its permission and execution model matters just as much as with any other agent that can touch real files and run real commands.

# When To Use It

For hands-on coding tasks where an agent operating directly in your repository (rather than a plain chat window) is the more efficient workflow.

# How To Use It Safely

- Review proposed changes and command executions before approving them, especially anything destructive or affecting shared/remote state.
- Keep repository-specific scope and constraints written down (as this repository's `CODEX.md` does) so the agent has explicit boundaries.
- Use version control so agent-made changes are always reviewable and revertible.
- Treat output as a draft to review, not an authoritative final answer, particularly for security-sensitive changes.

# Common Mistakes

- Granting broad, standing permissions instead of scoping them to the task at hand.
- Not maintaining a clear repository-level instructions file, leaving the agent to guess scope boundaries.
- Assuming agent-proposed code is correct and secure without review — see [[AI_Safety_Workflows]].

# Related CORE Notes

- [[Claude_Code]]
- [[Prompting]]
- [[AI_Safety_Workflows]]
- [[Git]]

# Sources

- OpenAI, Codex documentation — https://developers.openai.com/codex
