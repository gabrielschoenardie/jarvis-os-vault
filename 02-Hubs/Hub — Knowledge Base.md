---
type: hub
status: active
domain: knowledge-base
created: 2026-07-11
updated: 2026-07-11
importance: high
aliases: []
---

## Definition

This hub covers how this vault itself is organized as a knowledge base — the note-taking method behind the folder structure and linking rules.

## Contained clusters

The vault follows the [[Zettelkasten Method]]: small [[Atomic Notes]] linked densely rather than filed into topic folders, navigated through a [[Hub and Spoke Structure]] like this one. [[Decision — Vault Architecture v1]] records why this shape was chosen over folders-per-domain.

```dataview
LIST FROM "" WHERE domain = "knowledge-base" AND type != "hub" SORT file.mtime DESC
```

## Related hubs

Structurally underpins every hub in this vault, and connects to [[Hub — Memory System]] since the note graph this method produces is what [[Bridge — Vault as Mind]] renders. It also links back to [[Hub — JARVIS OS Core]] as the root hub for the vault.
