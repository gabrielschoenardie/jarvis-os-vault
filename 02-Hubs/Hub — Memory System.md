---
type: hub
status: active
domain: memory-system
created: 2026-07-11
updated: 2026-07-11
importance: high
aliases: []
---

## Definition

This hub covers how JARVIS OS remembers things — the models of memory available and which one this vault actually uses.

## Contained clusters

This vault stores memory as [[Graph-Based Memory]] rather than [[Semantic Retrieval]] over [[Vector Embeddings]], though the latter remains a natural extension as note count grows. [[Bridge — Vault as Mind]] explains why the graph model was chosen: it doubles as the literal render source for the Vault Brain.

```dataview
LIST FROM "" WHERE domain = "memory-system" AND type != "hub" SORT file.mtime DESC
```

## Related hubs

Connected to [[Hub — Architecture]] and [[Hub — JARVIS OS Core]] via [[Bridge — Vault as Mind]], and to [[Hub — Knowledge Base]] which shapes how the graph is authored.
