---
type: hub
status: active
domain: automation
created: 2026-07-11
updated: 2026-07-11
importance: high
aliases: []
---

## Definition

This hub covers running work without a human driving each step — from a single scheduled job to coordinated multi-agent systems.

## Contained clusters

[[Agent Orchestration Basics]] is the central concept, usually feeding on a [[Task Queues]] of pending work and triggered on a schedule via [[Cron Scheduling]]. [[Bridge — Agent Orchestration]] connects this cluster to model and architecture decisions.

```dataview
LIST FROM "" WHERE domain = "automation" AND type != "hub" SORT file.mtime DESC
```

## Related hubs

Bridges into [[Hub — AI Models]] and [[Hub — Architecture]] via [[Bridge — Agent Orchestration]], and supports [[Hub — JARVIS OS Core]].
