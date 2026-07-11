---
type: hub
status: active
domain: architecture
created: 2026-07-11
updated: 2026-07-11
importance: high
aliases: []
---

## Definition

This hub covers the software architecture behind the jarvis-os app: how the React/Vite frontend and the 3D Vault Brain are structured, and the patterns that keep them maintainable as the app grows.

## Contained clusters

The core pattern here is [[Component-Based UI]], made workable by clear [[State Management Boundaries]] between local, feature-level, and app-wide state. The Vault Brain specifically is built with [[React Three Fiber Rendering]], the React binding for Three.js used across [[Three.js Visualization]].

```dataview
LIST FROM "" WHERE domain = "architecture" AND type != "hub" SORT file.mtime DESC
```

## Related hubs

Closely tied to [[Hub — JARVIS OS Core]], which this architecture serves, and to [[Hub — Memory System]] via [[Bridge — Vault as Mind]] and [[Hub — Automation]] via [[Bridge — Agent Orchestration]].
