---
title: Prompt Audit Lab
area: labs
difficulty: beginner
status: draft
last_reviewed: 2026-07-04
sources:
tags:
  - lab
  - ai-tooling
  - prompting
---

# Objective

Practice auditing your own prompts for ambiguity and unstated assumptions, reinforcing [[Prompting]] and [[AI_Safety_Workflows]].

# Safety Scope

Local exercise using any AI chat tool or coding agent you already have access to. No sensitive or production data — use a throwaway example task.

# Requirements

- Access to any AI assistant or coding agent (cloud or local, per [[Local_AI]]).
- A small, real task you want help with (e.g. "write a function that parses a date").

# Steps

1. Write your first-draft prompt for the task, exactly as you'd normally type it.
2. Before sending it, audit it against a checklist: Does it state the goal explicitly? Does it give necessary context (language, constraints, edge cases)? Does it leave anything for the model to guess?
3. Send the first-draft prompt and review the output.
4. Rewrite the prompt, filling in every gap you identified in step 2.
5. Send the revised prompt and compare the two outputs.
6. Note specifically what changed in the output quality, and which added detail mattered most.

# Expected Result

A concrete before/after comparison showing which specific missing detail (not just "more detail in general") most improved the output — turning [[Prompting]] from an abstract principle into an observed result.

# Troubleshooting

- If both outputs look similar, try a more ambiguous first-draft prompt — the exercise works best when the first draft genuinely under-specifies the task.
- If the model's output contains a factual/technical claim, verify it independently rather than accepting it — see [[Verification_Methods]].

# Cleanup

None required.

# Related CORE Notes

- [[Prompting]]
- [[AI_Safety_Workflows]]
- [[Claude_Code]]
- [[Codex]]

# Sources

- Internal — exercise structure only.
