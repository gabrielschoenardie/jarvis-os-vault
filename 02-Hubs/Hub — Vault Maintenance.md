---
type: hub
status: active
domain: principles
created: 2026-07-11
updated: 2026-07-11
importance: high
aliases: []
---

## Definition

This hub covers the operational discipline that keeps the vault healthy as it grows: which plugins to run, how often to review, and the rule that nothing is ever deleted.

## Contained clusters

This hub operationalizes the last two stages of the [[Principle — Knowledge Lifecycle]] — Review and Archive — as a concrete cadence, run using [[Template — Weekly Review]].

```dataview
LIST FROM "" WHERE domain = "principles" AND type != "hub" SORT file.mtime DESC
```

## Plugins

Dataview, Templater, and QuickAdd are already installed. The one remaining recommendation is **Graph Analysis** (install via the Obsidian community plugins UI) — it surfaces node degree and clustering directly in Obsidian, which is useful for spotting the same high-degree hubs the Vault Brain renders largest before they need splitting.

## Canonical queries

```dataview
LIST FROM "" WHERE domain = "<slug>" AND type != "hub" SORT file.mtime DESC
```

```dataview
LIST FROM -"05-Templates" AND -"99-Archive"
WHERE type != "hub" AND length(file.inlinks) = 0
```

```dataview
TABLE updated, status FROM -"05-Templates" AND -"99-Archive"
WHERE status != "archived" AND date(updated) < date(today) - dur(30 days)
SORT updated ASC
```

## Maintenance cadence

- **Weekly**: run [[Template — Weekly Review]] — process new captures, connect zero-backlink notes, refine or archive stale ones.
- **Monthly**: check hub size. A hub nearing ~150 notes should be split into a new sub-hub, never a new folder — see [[Decision — Vault Architecture v1]] for why folders aren't the escape valve.
- **Quarterly**: review the three bridge notes ([[Bridge — Adaptive AI and VBV]], [[Bridge — Agent Orchestration]], [[Bridge — Vault as Mind]]) — are they still the right seams, or has a new one formed?
- **Always**: never delete. Retire a note to `99-Archive/` with `status: archived` and leave its links intact, per [[Principle — Knowledge Lifecycle]].

## Related hubs

Part of the same domain as [[Hub — Principles]], relevant to [[Hub — Knowledge Base]] since maintenance is what keeps that structure legible, and reports up to [[Hub — JARVIS OS Core]].
