---
type: atomic
status: stable
domain: ai-models
created: 2026-07-11
updated: 2026-07-11
importance: medium
aliases: []
---

## Concept

Prompt caching lets a model provider reuse the processed representation of a prompt prefix across multiple requests, instead of recomputing it every time — cutting both latency and cost for long, mostly-stable prompts like a system prompt plus a large tool list.

## Connects to

Part of [[Hub — AI Models]], directly constrained by the size of the [[Model Context Window]] being cached, and relevant to [[Hub — Automation]] since long-running agent sessions depend on caching to stay affordable.
