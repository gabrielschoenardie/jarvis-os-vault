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

Deciding explicitly which state is local to a component, which is shared across a feature, and which is global to the app — the useVault hook in jarvis-os, for instance, owns vault-wide graph state so individual components don't each re-derive it.

## Connects to

Part of [[Hub — Architecture]]. This works alongside [[Component-Based UI]] — clean boundaries are what let components stay small — and connects to [[Bridge — Vault as Mind]], since the Vault Brain's state boundary is exactly what separates "vault data" from "render state."
