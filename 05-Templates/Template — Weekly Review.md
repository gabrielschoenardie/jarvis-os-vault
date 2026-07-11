---
type: reference
status: seed
domain:
created: <% tp.date.now("YYYY-MM-DD") %>
updated: <% tp.date.now("YYYY-MM-DD") %>
importance: medium
aliases: []
---

## Created this week

```dataview
LIST FROM -"05-Templates" AND -"99-Archive"
WHERE date(created) >= date(today) - dur(7 days)
SORT created DESC
```

## Zero backlinks

```dataview
LIST FROM -"05-Templates" AND -"99-Archive"
WHERE type != "hub" AND length(file.inlinks) = 0
```

## Stale (30+ days untouched)

```dataview
TABLE updated, status FROM -"05-Templates" AND -"99-Archive"
WHERE status != "archived" AND date(updated) < date(today) - dur(30 days)
SORT updated ASC
```

## Notes

Work through each list above: process inbox captures, connect zero-backlink notes to a hub and a sibling (link your home hub here), and either refine or archive stale notes.
