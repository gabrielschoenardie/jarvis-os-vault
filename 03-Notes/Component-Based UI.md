---
type: atomic
status: stable
domain: architecture
created: 2026-07-11
updated: 2026-07-11
importance: medium
aliases: []
---

## Concept

Building an interface out of small, self-contained components (React components in the jarvis-os app) that each own their own state and rendering, and compose into the full UI rather than one monolithic view.

## Connects to

Part of [[Hub — Architecture]], alongside [[State Management Boundaries]] — components are only clean if it's clear which state lives inside a component and which lives outside it. [[React Three Fiber Rendering]] is the specific component model the Vault Brain's 3D graph is built from.
