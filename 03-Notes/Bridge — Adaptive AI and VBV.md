---
type: bridge
status: seed
domain: video-engineering
created: 2026-07-11
updated: 2026-07-11
importance: medium
aliases: []
---

## Domain A

[[Hub — Video Engineering]]: encoding a clip against a fixed [[VBV (Video Buffering Verifier)]] target is a constrained optimization problem — hit the buffer limit while preserving as much [[VMAF]] quality as possible.

## Domain B

[[Hub — AI Models]]: a model can be used to choose encoder settings (CRF, preset, VBV bufsize) per-clip based on its content, rather than applying one fixed setting to every video.

## The connection

Using a model to adapt [[x264]] parameters per-clip against a VBV constraint is a small, concrete instance of [[Model Routing (Big Model vs Small Model)]] applied outside the chat context — the "model" here optimizes an encoding decision instead of a conversation, guided by the same [[Hub — Principles]] preference for measuring ([[VMAF]]) over guessing.
