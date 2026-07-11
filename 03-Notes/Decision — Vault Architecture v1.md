---
type: decision
status: stable
domain: principles
created: 2026-07-11
updated: 2026-07-11
importance: critical
aliases: []
---

## Decision

The vault stores all permanent notes in a single flat `03-Notes/` folder, forever — no topic sub-folders under any circumstance. Topic membership is expressed exclusively through a `domain` frontmatter field and through wikilinks to hub notes in `02-Hubs/`, never through file paths. Approved by Gabriel on 2026-07-11.

## Why

Two consumers read this vault besides Gabriel: Claude, note-by-note, and the JARVIS OS Vault Brain, which parses every Markdown file and resolves links by lowercase basename alone — paths carry no meaning to it. Since the graph reader can't see folders, any structure encoded in paths would be invisible to half the vault's consumers, while structure encoded in links is visible to all of them. A flat folder also enforces the one-title-one-note collision rule by construction, and it keeps [[Atomic Notes]] free to belong to several clusters at once, which folders cannot do. This follows [[Constraints Before Features]] — the reader's constraints were fixed first and the architecture designed inside them — and this note exists because of [[Document The Why]].

## Alternatives

**PARA** (Projects / Areas / Resources / Archive): rejected because it organizes by actionability, not by meaning; JARVIS OS needs a semantic memory, and PARA's categories say nothing about what a note is about. Its useful residue survives as the numbered pipeline folders (`00-Inbox` through `99-Archive`), which stage a note's lifecycle rather than its topic.

**Folders-per-domain** (one sub-folder per domain under `03-Notes/`): rejected because a note bridging two domains would need to live in one folder and lie about the other, duplicate titles across folders would silently collide in the link resolver, and every re-categorization would become a file move instead of a link edit. The [[Hub and Spoke Structure]] gives the same navigability with none of those costs.

## What would change this

The Vault Brain renders at most 1500 nodes (top 800 by degree plus neighbors) and scans at most 4000 files. Approaching the 1500-node render cap is the trigger to revisit this architecture. Growth short of that is handled inside the current design: a hub nearing ~150 notes gets split into sub-hubs — new hub notes, never new folders.
