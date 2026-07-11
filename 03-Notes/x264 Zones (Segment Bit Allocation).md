---
type: atomic
status: stable
domain: video-engineering
created: 2026-07-11
updated: 2026-07-11
importance: medium
aliases: [x264 Zones]
---

## Concept

x264 zones bias bitrate allocation per shot — more bits to complex segments, fewer to static ones — reusing the same cut structure already measured for [[GOP (Group of Pictures)]], so it costs no extra encoding pass. Multipliers are clamped to [0.70, 1.40] and frame-weighted so the average stays near 1.0, meaning the global `-b:v`/VBV budget stays valid: zones move bits *within* the budget, they never raise the ceiling.

## Connects to

Part of [[Hub — Video Engineering]], a sibling of [[GOP (Group of Pictures)]] since both are derived from the same source-cut Pass-1, bounded by the same [[VBV (Video Buffering Verifier)]] ceiling it's built to never exceed, and serialized into [[x264]]'s `-x264-params` following the comma-and-slash exception documented in [[x264-params Syntax]].
