---
title: Computer Science Basics
area: foundations
difficulty: beginner
status: draft
last_reviewed: 2026-07-04
sources:
  - "CS:APP (Bryant & O'Hallaron), Computer Systems: A Programmer's Perspective"
tags:
  - foundations
  - computer-science
---

# What It Is

A computer runs programs by repeatedly fetching an instruction from memory, decoding it, and executing it (the fetch-decode-execute cycle). Everything else — operating systems, applications, the internet — is layers built on top of that one basic loop.

# Why It Matters

Every other topic in CORE assumes some version of this model. Understanding that "a program" is just a sequence of simple instructions run very fast makes concepts like processes, memory, permissions, and even network packets much less mysterious.

# When To Use It

You don't "use" this note day-to-day — it's the mental model you fall back on when a higher-level concept (a crashing process, a permission error, a slow program) doesn't make sense any other way.

# How To Use It Safely

Not applicable in a hands-on sense — this is conceptual background, not a tool or technique.

# Common Mistakes

- Treating "the computer" as a black box instead of layers (hardware → OS → applications) — this makes troubleshooting feel like guesswork instead of narrowing down a layer.
- Assuming programming knowledge is required to understand computers at this level. It isn't — this is about mental models, not syntax.

# Related CORE Notes

- [[Command_Line]]
- [[Filesystems]]
- [[Linux_Index]]

# Sources

- Bryant, R. & O'Hallaron, D., *Computer Systems: A Programmer's Perspective* — general CS systems background (interpretation/summary, not a direct quote).
