# Contributing to CORE

CORE accepts contributions that strengthen its mission: a clean, honest, defensive-only technical education vault. Read this file before opening a pull request.

## Scope: Defensive-Only

CORE covers computer science, Linux, networking, defensive cybersecurity, OSINT verification, cloud/DevOps, Git/GitHub, and AI tooling. It does **not** accept:

- Exploit code, exploit chains, or weaponized proof-of-concepts.
- Malware, credential-theft techniques, or unauthorized-access instructions.
- Detection-evasion or anti-forensics content.
- Real-world targeting workflows against specific people, organizations, or systems.
- Forensic case material, incident data, or anything tied to a real investigation.
- Personal agent-persistence systems, unrelated side projects, or content belonging to other repositories.

If you are unsure whether something fits, open an issue and ask before submitting a pull request.

## How To Add a Note

1. Pick the correct subject folder (`01_Foundations` through `10_Glossary`) — one concept per note.
2. Copy [[_Templates/Topic_Template]] (`_Templates/Topic_Template.md`) as your starting point.
3. Fill in the frontmatter completely, including `area`, `difficulty`, and `tags`. Leave `status: draft` until the note has been reviewed.
4. Write all seven required sections: What It Is, Why It Matters, When To Use It, How To Use It Safely, Common Mistakes, Related CORE Notes, Sources.
5. Add the note to its folder's `*_Index.md` file and link it from at least one other related note.
6. Use `[[Wiki_Links]]` for internal references, not raw file paths.

## How To Add Sources

- Every factual claim that isn't common, easily-verified knowledge should have a source in the `Sources` section.
- Prefer primary documentation (man pages, RFCs, vendor docs) over blog posts or secondary summaries.
- If a claim is your own interpretation or an unverified inference, say so explicitly in the note body — do not present interpretation as fact.
- Dead or paywalled links should be flagged in the pull request description, not silently left in.

## How To Add a Lab

1. Copy [[_Templates/Lab_Template]] into the correct subfolder under `08_Labs/`.
2. Write all nine required sections, especially **Safety Scope** — state clearly what systems the lab may be run against (your own local/lab environment only, unless explicitly a read-only public-source lookup).
3. Labs must be reproducible with commonly available tools and must not require bypassing security controls you don't own.
4. Add the lab to `08_Labs/Labs_Index.md`.

## How To Add a Learning Trail

1. Copy [[_Templates/Learning_Trail_Template]] into `_Learning_Trails/`.
2. Learning Trails document a real question, the actual path taken through CORE notes to answer it, where the answer was found, and what to ask next — not a hypothetical or idealized path.
3. Use the Learning Trail frontmatter (includes `question` and `created` fields, not the standard topic frontmatter).
4. Add the trail to the relevant `_Learning_Trails/*_Trails.md` file and to `_Learning_Trails/Learning_Trails_Index.md`.

## Pull Request Quality Rules

- One concept, note, lab, or trail per PR where practical — keep reviews small.
- No unsupported claims. If you can't source it, mark it as interpretation or open uncertainty.
- No unsafe offensive content, even framed as "educational."
- Frontmatter must be complete and correctly formatted.
- Internal links must resolve to real note names.
- No automation, scripts, GitHub Actions, or hidden workflows — CORE is Markdown-first and stays that way unless a maintainer explicitly changes that decision.
- No generated site output, `node_modules`, virtual environments, or other build clutter — check `.gitignore` before committing.
- Write in direct, practical, beginner-accessible language. No hype, no filler, no exaggerated claims.

## Questions

Open a GitHub issue for anything not covered here.
