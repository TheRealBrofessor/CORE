---
title: CORE Roadmap
area: start-here
difficulty: beginner
status: draft
last_reviewed: 2026-07-04
sources:
tags:
  - start-here
  - roadmap
---

# Roadmap

CORE grows incrementally. This roadmap tracks the current state and planned direction — it is not a promise of a delivery date.

## Current State (2026-07-04)

- Full folder structure in place across all ten subject areas plus Labs, Playbooks, Glossary, Indexes, Templates, and Learning Trails.
- Starter content exists in every required file. Most notes are `status: draft` and need source review and expansion over time.
- No automation, CI/CD, or site generation is configured — the vault is Markdown-only by design at this stage.

## Near-Term

- Expand each subject area beyond its starter notes as contributors add depth.
- Grow the Learning Trails collection with real questions and real paths, not hypothetical ones.
- Review and promote notes from `status: draft` to `status: reviewed` as sources are verified.

## Deliberately Not Planned Right Now

- GitHub Actions, CI/CD, or automated publishing — out of scope until explicitly decided otherwise.
- A generated static site (e.g. MkDocs) — CORE previously carried MkDocs tooling and was reset specifically to return to a clean Markdown-first vault. Re-adding a site generator would need a deliberate, separate decision.
- Offensive-security content of any kind — permanently out of scope, not just "not yet."

## How To Propose Roadmap Changes

Open a GitHub issue describing the proposed addition and how it fits CORE's defensive-only, Markdown-first mission. See [CONTRIBUTING.md](../CONTRIBUTING.md).

## Related CORE Notes

- [[Welcome]]
- [[CORE_Principles]]
- [[Master_Index]]

## Sources

- Internal — repository history (`git log`) shows the prior MkDocs-based structure and its reset.
