---
type: principle
status: stable
domain: principles
created: 2026-07-11
updated: 2026-07-11
importance: high
aliases: []
---

## Principle

Fix the hard constraints of a system before adding features on top of it — the flat `03-Notes/` rule in this vault, or a [[VBV (Video Buffering Verifier)]] target in an encode, are constraints decided first, with everything else designed to fit inside them.

## Why

Constraints decided late force expensive rework, because features already assume the shape of the old, unconstrained system. Deciding them early — even if imperfectly — gives every later decision a fixed frame to fit into.

## Connects to

Part of [[Hub — Principles]]. This is the same discipline behind [[Document The Why]]: constraints are only durable if the reasoning behind them is written down, or the next pass will "fix" them away.
