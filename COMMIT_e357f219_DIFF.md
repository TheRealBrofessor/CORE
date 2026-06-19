# Commit: e357f2192da65ae0692b485c60d3100447ae8dc3

**Message:** Reset repository contents

**Author:** TheRealBrofessor <66forde36@gmail.com>

**Date:** 2026-06-13T01:02:17Z

**URL:** https://github.com/TheRealBrofessor/CORE/commit/e357f2192da65ae0692b485c60d3100447ae8dc3

---

## Summary

This commit deleted 632,944 lines across the repository (632,941 deletions, 3 additions).

---

## Deleted Files

### Configuration & Templates

#### .github/ISSUE_TEMPLATE/bug.yml
**Status:** Removed (28 lines deleted)
```yaml
name: Bug report
description: Report a problem with the site or content.
title: "[Bug]: "
labels: ["bug"]

body:
  - type: textarea
    id: what
    attributes:
      label: What happened?
      description: What did you expect vs what happened?
    validations:
      required: true

  - type: input
    id: page
    attributes:
      label: Page / file path
      placeholder: "e.g., notes/beginner/cs/what-is-a-computer.md"
    validations:
      required: false

  - type: textarea
    id: steps
    attributes:
      label: Steps to reproduce
    validations:
      required: false
```

#### .github/ISSUE_TEMPLATE/content-request.yml
**Status:** Removed (32 lines deleted)
```yaml
name: Content request
description: Request a new note, lab, or cheatsheet.
title: "[Content]: "
labels: ["content"]

body:
  - type: dropdown
    id: type
    attributes:
      label: Content type
      options:
        - Note
        - Lab
        - Cheatsheet
    validations:
      required: true

  - type: input
    id: topic
    attributes:
      label: Topic / title
      placeholder: "e.g., Beginner Git: Branching basics"
    validations:
      required: true

  - type: textarea
    id: outline
    attributes:
      label: What should it cover?
      description: Bullet points are fine.
    validations:
      required: true
```

#### .github/ISSUE_TEMPLATE/new-note-proposal.yml
**Status:** Removed (29 lines deleted)
```yaml
name: New note proposal
description: Propose a new note with scope and placement in CORE.
title: "[Note]: "
labels: ["note"]

body:
  - type: input
    id: path
    attributes:
      label: Proposed file path
      placeholder: "e.g., notes/beginner/git/git-branches.md"
    validations:
      required: true

  - type: textarea
    id: summary
    attributes:
      label: Summary
      description: 2–5 sentences explaining what the note teaches and prerequisites.
    validations:
      required: true

  - type: textarea
    id: refs
    attributes:
      label: Sources / references
      description: Links, books, or specs backing this note.
    validations:
      required: false
```

#### .github/PULL_REQUEST_TEMPLATE.md
**Status:** Removed (30 lines deleted)
```markdown
## Summary
Briefly explain what this pull request does.

## Type of Change
(Check all that apply)

- [ ] New note
- [ ] Update to existing content
- [ ] Lab
- [ ] Cheatsheet
- [ ] Documentation / Meta
- [ ] Bug fix

## Location
Where does this change live?

Example:
- notes/beginner/cs/
- notes/intermediate/web/
- templates/

## Checklist
- [ ] Content follows project structure
- [ ] Markdown formatting is clean
- [ ] Links are valid (if applicable)
- [ ] Fits CORE scope and level
- [ ] No duplicate content

## Additional Context
Anything reviewers should know?
```

#### .github/workflows/deploy.yml
**Status:** Removed (48 lines deleted)
```yaml
name: Deploy MkDocs site to GitHub Pages

on:
  push:
    branches:
      - main
  workflow_dispatch:

permissions:
  contents: read
  pages: write
  id-token: write

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout repository
        uses: actions/checkout@v4

      - name: Set up Python
        uses: actions/setup-python@v5
        with:
          python-version: "3.x"

      - name: Install dependencies
        run: pip install -r requirements.txt

      - name: Build MkDocs site
        run: mkdocs build --strict

      - name: Upload site artifact
        uses: actions/upload-pages-artifact@v3
        with:
          path: ./site


  deploy:
    needs: build
    runs-on: ubuntu-latest
    environment:
      name: github-pages
      url: ${{ steps.deployment.outputs.page_url }}
    steps:
      - name: Deploy to GitHub Pages
        id: deployment
        uses: actions/deploy-pages@v4
```

#### .gitignore
**Status:** Removed (2 lines deleted)
```
site/
.venv/
```

---

### Virtual Environment Files (.venv/)

**Status:** All removed (632,000+ lines deleted)

#### Binary/Script Files Deleted:
- `.venv/bin/Activate.ps1` (247 lines) - PowerShell activation script
- `.venv/bin/activate` (70 lines) - Bash activation script
- `.venv/bin/activate.csh` (27 lines) - C-shell activation script
- `.venv/bin/activate.fish` (69 lines) - Fish shell activation script
- `.venv/bin/ghp-import` (6 lines) - GHP Import utility
- `.venv/bin/markdown_py` (6 lines) - Markdown processor
- `.venv/bin/mkdocs` (6 lines) - MkDocs CLI
- `.venv/bin/mkdocs-get-deps` (6 lines) - MkDocs dependency tool
- `.venv/bin/normalizer` (6 lines) - Charset normalizer
- `.venv/bin/pip` (8 lines) - Pip package manager
- `.venv/bin/pip3` (8 lines) - Pip3 package manager
- `.venv/bin/pip3.12` (8 lines) - Pip3.12 package manager
- `.venv/bin/pybabel` (6 lines) - Babel tool
- `.venv/bin/pygmentize` (6 lines) - Pygments highlighter
- `.venv/bin/python` (1 line) - Python symlink
- `.venv/bin/python3` (1 line) - Python3 symlink
- `.venv/bin/python3.12` (1 line) - Python3.12 symlink
- `.venv/bin/watchmedo` (6 lines) - Watchdog monitor

#### Package Cache Files Deleted:
- `.venv/lib/python3.12/site-packages/__pycache__/ghp_import.cpython-312.pyc`
- `.venv/lib/python3.12/site-packages/__pycache__/six.cpython-312.pyc`
- `.venv/lib/python3.12/site-packages/__pycache__/yaml_env_tag.cpython-312.pyc`

#### Package Files Deleted:
- `.venv/lib/python3.12/site-packages/_yaml/__init__.py` (33 lines)
- `.venv/lib/python3.12/site-packages/_yaml/__pycache__/__init__.cpython-312.pyc`
- `.venv/lib/python3.12/site-packages/babel-2.18.0.dist-info/INSTALLER` (1 line)

---

## Repository State After Commit

After this reset, the repository contains only:

```
CORE/
└── README.md (185 bytes)
```

### README.md Contents:
```markdown
# CORE

Community Obsidian Resource Exchange.

This repository was reset after unexpected Python/virtual-environment contents were found. Rebuild cleanly from trusted local files only.
```

---

## Parent Commit

**SHA:** `5652ab4335ca27c77f0687be7c46bfa05173be30`

---

## Statistics

- **Total Changes:** 632,944 lines
- **Additions:** 3 lines
- **Deletions:** 632,941 lines
- **Files Modified:** 40+ files

---

## Notes

The commit message and README note indicate this reset was intentional due to "unexpected Python/virtual-environment contents" being discovered in the repository. The virtual environment directory should typically be excluded via `.gitignore` rather than committed to the repository.
