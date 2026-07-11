---
type: atomic
status: stable
domain: ai-models
created: 2026-07-11
updated: 2026-07-11
importance: medium
aliases: [Context Window]
---

## Concept

The context window is the maximum amount of text (measured in tokens) a model can attend to in a single request, spanning system prompt, conversation history, and tool output. It's the hard budget that [[Prompt Caching]] is designed to spend more efficiently, and the reason [[Model Routing (Big Model vs Small Model)]] often routes long-context tasks to specific models.

## Connects to

Part of [[Hub — AI Models]]. Directly related to [[Prompt Caching]], which reuses parts of the context window across requests instead of re-processing them, and to [[Hub — Prompt Engineering]], since prompt design has to fit inside this budget.
