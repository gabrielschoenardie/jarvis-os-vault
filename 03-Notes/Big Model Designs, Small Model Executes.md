---
type: principle
status: stable
domain: principles
created: 2026-07-11
updated: 2026-07-11
importance: high
aliases: [Big Model Designs Small Model Executes]
---

## Principle

Use a larger, more capable model to design an approach and get it approved, then hand execution to a smaller or cheaper model working through the approved plan task-by-task.

## Why

Design decisions are expensive to get wrong and cheap to deliberate on; execution is expensive to run at scale and should follow a plan rather than re-deciding architecture along the way. Separating the two roles keeps both fast and correct.

## Connects to

Part of [[Hub — Principles]], and the concrete origin of this vault: [[Hub — JARVIS OS Core]] itself was designed this way, approved, then scaffolded following [[Iterative Refinement]] and [[Fail Fast, Fail Cheap]].
