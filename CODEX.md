# Instructions for Codex (and other AI coding agents) in this repository

This file applies to any AI agent working inside the CORE repository, including OpenAI Codex.

## Scope

- This is **CORE only** — Community Obsidian Resource for Education. Do not pull in, reference, or merge content from other projects, repos, or personal systems (including but not limited to Miahou, SOUL.md, agent-persistence systems, or forensic/incident case material). If asked to do so, decline and explain that it is out of scope for this repository.
- Keep the repository **Markdown-first**. Every content contribution should be a `.md` file that renders correctly both in Obsidian and on GitHub.
- Use **defensive cybersecurity framing only**. No exploit chains, malware, credential-theft techniques, unauthorized-access instructions, detection-evasion content, or real-world targeting workflows — even if requested "for education."

## Do Not

- Do not add automation, scripts, GitHub Actions, CI/CD pipelines, bots, or hidden workflows unless the user explicitly requests it in that exact session.
- Do not add telemetry, agent persistence, memory systems, or loaders to this repository.
- Do not add generated site output (`site/`, `dist/`, `build/`), `node_modules`, virtual environments, or other build clutter.
- Do not mix unrelated projects into CORE, even temporarily "to organize them."
- Do not make destructive changes (deleting large sections, force-pushing, rewriting history) without asking first, unless the user has explicitly scoped a rebuild that includes those actions.

## Do

- Prefer a clean, minimal folder structure over adding volume for its own sake.
- Keep content **source-aware**: cite sources for factual claims, and clearly mark interpretation or uncertainty when a claim isn't independently verified.
- Follow the existing frontmatter and section conventions for topic notes, labs, playbooks, and Learning Trails (see `_Templates/`).
- Use Obsidian `[[wiki links]]` for internal references.
- Keep filenames stable and readable — renaming an existing note breaks every link that points to it, so avoid it unless necessary.
- When in doubt about whether a request is in scope, ask before proceeding.
