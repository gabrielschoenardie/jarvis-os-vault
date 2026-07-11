---
type: hub
status: active
domain: prompt-engineering
created: 2026-07-11
updated: 2026-07-11
importance: high
aliases: []
---

## Definition

This hub covers how prompts are structured to get reliable behavior out of a model — the practical craft that sits on top of whatever model you've chosen.

## Contained clusters

[[System Prompt Design]] sets the persistent frame for a session, often combined with [[Few-Shot Examples]] to demonstrate rather than describe the desired output, and with [[Chain of Thought Prompting]] when the task benefits from visible intermediate reasoning.

```dataview
LIST FROM "" WHERE domain = "prompt-engineering" AND type != "hub" SORT file.mtime DESC
```

## Related hubs

Directly downstream of [[Hub — AI Models]] and the [[Model Context Window]] it operates within, and relevant to [[Hub — JARVIS OS Core]]'s voice interface.
