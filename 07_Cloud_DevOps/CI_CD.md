---
title: CI/CD
area: cloud-devops
difficulty: intermediate
status: draft
last_reviewed: 2026-07-04
sources:
  - "GitHub Docs, About continuous integration, https://docs.github.com/actions"
tags:
  - cloud-devops
  - ci-cd
---

# What It Is

CI/CD (Continuous Integration / Continuous Delivery or Deployment) is automation that runs tests and checks on every change (CI), and optionally deploys changes automatically once they pass (CD), typically triggered by commits or pull requests.

# Why It Matters

CI/CD catches problems (failing tests, broken builds) before they reach production, and removes manual, error-prone deployment steps. Understanding it conceptually matters even for projects — like this vault currently — that deliberately don't use it yet.

# When To Use It

For codebases where automated testing and repeatable deployment provide real value — typically application code rather than a documentation-only vault (see [[Roadmap]] for why CORE doesn't have CI/CD yet).

# How To Use It Safely

- Keep pipeline definitions in version control alongside the code they test/deploy.
- Limit what credentials/secrets a pipeline has access to — a compromised pipeline shouldn't have more access than necessary.
- Require passing checks before merge on important branches, rather than treating CI as advisory.
- Review third-party actions/plugins used in a pipeline the same way you'd review any other dependency.

# Common Mistakes

- Granting a CI pipeline broad credentials "to make things easier," expanding the blast radius of a pipeline compromise.
- Treating a green CI check as proof of correctness rather than proof that the specific tests it runs passed.
- Adding automation before it's needed, adding maintenance burden without corresponding value — CORE deliberately avoids this at its current stage (see [[CLAUDE.md|CLAUDE]] / [[CODEX.md|CODEX]] guidance in the repository root).

# Related CORE Notes

- [[GitHub]]
- [[Docker]]
- [[AI_Safety_Workflows]]

# Sources

- GitHub Docs, *About continuous integration* — https://docs.github.com/actions
