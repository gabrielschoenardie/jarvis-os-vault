---
type: hub
status: seed
domain:
created: <% tp.date.now("YYYY-MM-DD") %>
updated: <% tp.date.now("YYYY-MM-DD") %>
importance: high
aliases: []
---

## Definition

One paragraph describing what this domain covers.

## Contained clusters

Prose linking to the seed atomic notes that live under this hub (link your
atomic notes here — this is a load-bearing edge, not a bare list).

## Cluster query

```dataview
LIST FROM "" WHERE domain = "<slug>" AND type != "hub" SORT file.mtime DESC
```

## Related hubs

Link to sibling hubs and back to the Core hub (link related hubs here).
