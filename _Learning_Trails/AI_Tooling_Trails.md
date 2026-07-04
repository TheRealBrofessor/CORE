---
title: AI Tooling Trails
area: learning-trails
question: My AI coding assistant confidently told me a function exists that doesn't — what happened?
difficulty: beginner
status: draft
created: 2026-07-04
last_reviewed: 2026-07-04
sources:
tags:
  - learning-trail
  - ai-tooling
  - prompting
---

# Question

My AI coding assistant confidently described a function/API that turned out not to exist. What happened, and how do I avoid getting burned by this again?

# Why It Matters

This is one of the most common frustrations with AI coding tools, and understanding it changes how you use every AI tool covered in this vault, not just one specific one.

# Path Followed

Started at [[AI_Terms]] to learn the term for this (hallucination), then [[Prompting]] to understand that models predict plausible-sounding text and can produce confident, wrong answers when the actual fact is outside their training or context. Went to [[AI_Safety_Workflows]] for the concrete practice: treat model claims about specific APIs/behavior as unverified until checked, the same way [[Verification_Methods]] treats any other unverified claim.

# Source Path

Anthropic's prompt engineering documentation (via [[Prompting]]'s Sources section) for general guidance on providing context to reduce ungrounded answers.

# Answer

The model wasn't "lying" — it produced the statistically plausible-sounding completion for the prompt given, without access to ground truth about that specific library/version. The fix isn't to stop using AI coding tools; it's to verify specific, checkable claims (an API's existence, a flag's behavior) against real documentation or by running the code, especially when the tool is operating in an area it might not have solid training data for (a new library version, an internal/private API).

# What This Unlocks

A working default of "verify specific technical claims, don't verify general reasoning" when using [[Claude_Code]], [[Codex]], or any other AI assistant.

# Next Questions

What's the fastest way to verify an AI-suggested API call actually exists before running it against a real system?
