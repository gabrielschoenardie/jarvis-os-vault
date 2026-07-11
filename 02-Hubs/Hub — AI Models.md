---
type: hub
status: active
domain: ai-models
created: 2026-07-11
updated: 2026-07-11
importance: high
aliases: []
---

## Definition

This hub covers the models JARVIS OS runs on: their constraints, tradeoffs, and how to use different tiers of model for different jobs.

## Contained clusters

Every model's basic constraint is its [[Model Context Window]], which [[Prompt Caching]] helps use more efficiently across requests. Choosing which model handles a task is [[Model Routing (Big Model vs Small Model)]], the same idea behind [[Big Model Designs, Small Model Executes]].

```dataview
LIST FROM "" WHERE domain = "ai-models" AND type != "hub" SORT file.mtime DESC
```

## Related hubs

Connected to [[Hub — Prompt Engineering]] (prompting is how you actually use a model), [[Hub — Automation]] via [[Bridge — Agent Orchestration]], and [[Hub — JARVIS OS Core]].
