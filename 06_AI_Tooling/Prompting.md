---
title: Prompting
area: ai-tooling
difficulty: beginner
status: draft
last_reviewed: 2026-07-04
sources:
  - "Anthropic, Prompt engineering overview, https://docs.anthropic.com/"
tags:
  - ai-tooling
  - prompting
---

# What It Is

Prompting is how you phrase input to an AI model to get useful output: providing clear context, explicit constraints, and enough specificity that the model doesn't have to guess your intent.

# Why It Matters

The same model can produce very different quality output depending on how a request is framed. This is the single highest-leverage skill for getting reliable results from any AI tool covered in this vault.

# When To Use It

Every time you interact with an AI model — a chat assistant, a coding agent ([[Claude_Code]], [[Codex]]), or an embedded tool ([[VS_Code_AI]]).

# How To Use It Safely

- State the goal and constraints explicitly rather than assuming the model shares your unstated context.
- Give the model relevant facts (file paths, error messages, exact requirements) instead of vague descriptions.
- Ask for the model's reasoning or sources when a claim matters, and verify anything you can't personally check — see [[AI_Safety_Workflows]].
- Iterate: treat the first response as a draft, not a final answer, especially for anything security- or fact-sensitive.

# Common Mistakes

- Assuming the model remembers context from a different, unconnected conversation.
- Accepting confident-sounding output as verified fact without checking it, especially for niche or fast-changing information.
- Writing vague prompts ("make it better") instead of specific, checkable requirements.

# Related CORE Notes

- [[AI_Safety_Workflows]]
- [[Claude_Code]]
- [[Codex]]
- [[Prompt_Audit_Lab]]

# Sources

- Anthropic, prompt engineering documentation — https://docs.anthropic.com/
