---
type: principle
status: stable
domain: principles
created: 2026-07-11
updated: 2026-07-11
importance: high
aliases: [Fail Fast Fail Cheap]
---

## Principle

Find out a decision is wrong as early and as inexpensively as possible — a quick VMAF check on one clip before batch-encoding a thousand, a small scaffolding pass before writing the full vault.

## Why

The cost of a mistake grows with how much has been built on top of it. Catching an error before it compounds is always cheaper than catching it after.

## Connects to

Part of [[Hub — Principles]], and the direct motivation for [[Iterative Refinement]] and [[Show Don't Tell]] — both are strategies for surfacing failure early rather than late.
