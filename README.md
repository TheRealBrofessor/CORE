# CORE — Community Obsidian Resource for Education

CORE is a public, Markdown-first, Obsidian-compatible technical education vault. It organizes practical learning paths, notes, labs, playbooks, and references across computer science, Linux, networking, defensive cybersecurity, OSINT verification, cloud/DevOps, Git/GitHub, and AI coding tools.

Start here: [Welcome.md](00_Start_Here/Welcome.md)

## What CORE Is

- A structured knowledge base you can clone and open directly as an Obsidian vault.
- A set of beginner-to-intermediate learning paths across foundational and applied technical topics.
- A collection of hands-on, safe, defensive-only labs and playbooks.
- A living reference that marks what is verified fact, what is interpretation, and what is still uncertain.
- A place where every note explains *what* something is, *why it matters*, and *how to use it safely*.

## What CORE Is Not

- Not an offensive hacking manual. No exploit chains, malware, credential theft, unauthorized access techniques, or real-world targeting workflows.
- Not a personal notebook, journal, or agent-persistence system. CORE contains no private data, no case files, and no forensic incident material tied to real investigations.
- Not an automation platform. CORE is Markdown content — it does not run scripts, agents, or hidden workflows.
- Not a finished product. Content is versioned, reviewed, and improved over time — see the `status` field in each note's frontmatter.

## Who CORE Is For

- Beginners who want a structured, honest on-ramp to Linux, networking, and security concepts.
- Self-learners who want a defensive-security and OSINT-verification focus without offensive framing.
- People evaluating or learning AI coding tools (Claude Code, Codex, local models) for technical work.
- Anyone who wants to contribute a well-sourced note, lab, or learning trail back to a shared public vault.

## How To Use CORE In Obsidian

1. Clone this repository.
2. Open the cloned folder in Obsidian as a vault (`Open folder as vault`).
3. Use the Quick Switcher (`Ctrl/Cmd+O`) to jump to any note by name.
4. Follow `[[wiki links]]` between notes — every note links to related notes, its parent index, and relevant learning trails.
5. Start from [[Master_Index]] or [[Welcome]] if you are new.
6. No community plugins are required. CORE relies only on Obsidian's built-in linking and search.

## How To Read CORE On GitHub

Every note is plain Markdown and renders cleanly on GitHub. Wiki-style `[[links]]` do not render as clickable links on GitHub (this is expected — they work in Obsidian). When browsing on GitHub, use the folder structure and the index files (`*_Index.md`, `_Indexes/Master_Index.md`) as your navigation map.

## How The Learning Paths Work

Each numbered folder (`01_Foundations` through `10_Glossary`) is a subject area with its own `*_Index.md` file listing every note in that area. The Master Index (`_Indexes/Master_Index.md`) links every subject area together. The `_Indexes` folder also contains curated **paths** — ordered reading lists for a specific goal (e.g. Beginner Path, Blue Team Path) that pull notes, labs, and playbooks from across the vault into a single sequence.

## How Learning Trails Work

A Learning Trail is a record of a real question a learner had, the path they took through CORE to answer it, where the answer was actually found, and what question naturally comes next. Trails live in `_Learning_Trails/` and are meant to be added to over time — see `_Learning_Trails/Learning_Trails_Index.md` and `_Templates/Learning_Trail_Template.md`.

## How To Contribute

See [CONTRIBUTING.md](CONTRIBUTING.md) for the full process, including how to add notes, sources, labs, and Learning Trails, and the pull request quality rules. All contributions must stay within CORE's defensive-only, education-first scope.

## License

See [LICENSE](LICENSE).
