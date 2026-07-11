---
type: bridge
status: seed
domain: automation
created: 2026-07-11
updated: 2026-07-11
importance: high
aliases: []
---

## Domain A

[[Hub — AI Models]]: [[Model Routing (Big Model vs Small Model)]] decides which model handles which piece of work based on capability and cost.

## Domain B

[[Hub — Architecture]]: [[State Management Boundaries]] and [[Component-Based UI]] decide which piece of a system owns which responsibility.

## The connection

[[Agent Orchestration Basics]] applies the same question — who owns this piece of work — to agents instead of components or model tiers: which subtask should a big model design, which should a small model execute, and which state (plan, task list, results) is shared between them versus owned by one agent alone. This is [[Big Model Designs, Small Model Executes]] made concrete as a system design, not just a principle.
