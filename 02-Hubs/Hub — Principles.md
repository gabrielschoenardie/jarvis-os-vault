---
type: hub
status: active
domain: principles
created: 2026-07-11
updated: 2026-07-11
importance: critical
aliases: [Metodologia Gabriel]
---

## Definition

This hub, aliased "Metodologia Gabriel," collects the working principles that shape how Gabriel builds things — from vault architecture to video pipelines to agent workflows. These are rules learned from experience, not abstract advice.

## Contained clusters

The core loop is [[Iterative Refinement]] paired with [[Fail Fast, Fail Cheap]] and [[Show Don't Tell]] — get something real in front of yourself quickly. [[Constraints Before Features]] and [[Document The Why]] keep that speed from turning into chaos. [[Big Model Designs, Small Model Executes]] is how these principles scale to agent-driven work.

```dataview
LIST FROM "" WHERE domain = "principles" AND type != "hub" SORT file.mtime DESC
```

## Related hubs

Underpins nearly every other hub, most visibly [[Hub — Automation]] (via [[Big Model Designs, Small Model Executes]]) and [[Hub — Knowledge Base]] (via [[Document The Why]] and [[Decision — Vault Architecture v1]]), and reports up to [[Hub — JARVIS OS Core]].
