# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repository is

This is **not a software project** — it is a personal knowledge vault ("jarvis-os-vault") of Markdown notes, organized in an Obsidian/PKM style. There are no build, lint, or test commands; there is no package manager or code tooling.

It is also the long-term memory source for the JARVIS OS app (a separate repo): that app's 3D "Vault Brain" reads this vault's files directly and renders every note as a node and every wikilink as an edge. That reader has real parsing constraints (below), and every note in this vault must be written with them in mind.

## Vault structure

Content is organized into numbered top-level folders that define a processing pipeline for notes:

- `00-Inbox/` — unprocessed captures; notes land here first before being triaged
- `01-Daily/` — daily notes
- `02-Hubs/` — hub/index notes that link related notes together (maps of content)
- `03-Notes/` — the main body of processed, permanent notes
- `04-Projects/` — notes tied to active projects
- `05-Templates/` — note templates
- `99-Archive/` — inactive/retired material

**`03-Notes/` is flat, permanently.** No topic sub-folders under it, ever. A note's topic is expressed through its `domain` frontmatter field and its wikilinks, never through its path.

## Naming and collision rule

Links resolve by lowercase basename, so one title is one note across the entire vault. Never create two notes with the same basename in different folders. Naming conventions:

- Atomic/principle/decision/etc. notes: `Title Case.md` — no IDs, no dates.
- Hub notes: `Hub — <Name>.md` (em dash).
- Bridge notes: `Bridge — <Name>.md` (em dash).
- Daily notes: `YYYY-MM-DD.md`.

## YAML frontmatter schema

Every note carries this frontmatter (frontmatter is parsed for wikilinks too, so aliases and any bracketed values in it become graph edges):

```yaml
---
type: atomic | hub | bridge | principle | decision | learning | project | reference | glossary | daily
status: seed | draft | active | review | stable | archived
domain: jarvis-os-core | architecture | ai-models | prompt-engineering | automation | memory-system | principles | knowledge-base | video-engineering | photography
created: YYYY-MM-DD
updated: YYYY-MM-DD
importance: critical | high | medium | low
aliases: []
---
```

## Linking rules

- Every atomic-type note links to at least one hub and at least one sibling note, in prose (not a bare list).
- Every hub links back to `Hub — JARVIS OS Core`.
- Bridges are deliberate: a bridge note names one primary domain in its frontmatter, and its body links out to both hubs it connects.
- Prefer links inside sentences over bare bullet lists of links — this is what keeps the note graph legible in the 3D Vault Brain, not just in Obsidian.

## Vault Brain reader constraints (do not violate)

The JARVIS OS app's vault reader has specific behavior that shapes how notes must be written:

- Markdown fenced code blocks (triple backtick) are stripped **before** link parsing, so a wikilink inside a fenced code block (e.g. inside a Dataview query) creates **zero** graph edges. Dataview blocks are invisible to the graph — real structure must live in body prose links, not query blocks.
- Inline code (single backticks) is **not** stripped, so a wikilink inside inline code still resolves.
- An unresolved link (pointing to a note that doesn't exist) renders as a "ghost" node. Any bracketed example that is not meant to be a real link — in documentation like this file — must be placed inside a fenced code block (not just inline single backticks, which are *not* stripped) so it is excluded from parsing and never becomes a ghost:
  ```
  [[link]]
  ```
- All `.md` files outside dot-folders are scanned and become graph nodes, including files in `05-Templates/`, `99-Archive/`, and root-level `README.md`/`CLAUDE.md`. Template files deliberately contain no literal double-bracket links (they use plain-text cues like "link your home hub here") so they don't pollute the graph with dangling edges.
- Scan cap is 4000 files; the render prunes to the top 800 nodes by degree plus their neighbors, capped at 1500 nodes total. Hubs are meant to be the highest-degree nodes so they render largest and brightest.

## Working in this vault

- All content is Markdown. Notes may use Obsidian conventions such as wikilinks and YAML frontmatter.
- When creating a note, place it in the folder matching its role above; use `00-Inbox/` when the destination is unclear.
- Git tracks only files, so empty folders are invisible in git — the structure above is the source of truth for the vault layout.
