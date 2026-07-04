---
title: Docker
area: cloud-devops
difficulty: intermediate
status: draft
last_reviewed: 2026-07-04
sources:
  - "Docker Docs, https://docs.docker.com/"
tags:
  - cloud-devops
  - docker
---

# What It Is

Docker packages an application with its dependencies into a container — an isolated, portable unit that runs consistently across environments. Containers are built from images defined by a `Dockerfile` and are lighter-weight than full virtual machines because they share the host's kernel.

# Why It Matters

Containers solve "it works on my machine" by packaging the runtime environment alongside the code, and are foundational to most modern deployment and CI/CD workflows ([[CI_CD]]).

# When To Use It

When you need a consistent, reproducible runtime environment across development, testing, and production, or want to isolate an application's dependencies from the host system.

# How To Use It Safely

- Use official or well-maintained base images, and check for known vulnerabilities before deploying.
- Don't run containers as root unless the workload genuinely requires it.
- Keep images updated — an outdated base image can carry known, patched vulnerabilities forward.
- Avoid baking secrets into an image layer — use environment variables or a secrets manager instead.

# Common Mistakes

- Treating container isolation as equivalent to full security isolation — containers share the host kernel and are not a hard security boundary against a determined attacker.
- Using `latest` tags in production, which can silently pull an unexpected new version.
- Leaving unused containers/images/volumes running, wasting resources and expanding attack surface.

# Related CORE Notes

- [[CI_CD]]
- [[Hardening]]
- [[VPS_Basics]]

# Sources

- Docker Docs — https://docs.docker.com/
