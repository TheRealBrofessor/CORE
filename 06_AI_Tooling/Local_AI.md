---
title: Local AI
area: ai-tooling
difficulty: intermediate
status: draft
last_reviewed: 2026-07-04
sources:
  - "Ollama documentation, https://github.com/ollama/ollama"
tags:
  - ai-tooling
  - local-ai
---

# What It Is

Local AI means running a language model directly on your own hardware (via tools like Ollama or llama.cpp) instead of calling a cloud provider's API. Model weights and inference run locally; no prompt data leaves your machine by default.

# Why It Matters

Local models trade some capability (smaller models are generally less capable than the largest cloud models) for privacy, offline availability, and no per-request cost. Understanding this tradeoff matters when choosing a tool for a given task.

# When To Use It

When working with sensitive data that shouldn't leave your machine, when you need offline availability, or when experimenting with model behavior without ongoing API costs.

# How To Use It Safely

- Verify the model source (official model registry/repository) before downloading weights, similar to vetting any other software dependency.
- Keep local AI tooling updated — like any other locally-run software, it can have vulnerabilities.
- Understand that a smaller local model may produce less accurate or less nuanced output than a large cloud model — verify important claims regardless of which you use.

# Common Mistakes

- Assuming "local" automatically means "private" if the tool itself still phones home telemetry — check the specific tool's actual behavior.
- Expecting a small local model to match the reasoning quality of the largest cloud-hosted models.
- Downloading model weights from unofficial/unverified mirrors.

# Related CORE Notes

- [[Prompting]]
- [[AI_Safety_Workflows]]

# Sources

- Ollama project documentation — https://github.com/ollama/ollama
