---
type: atomic
status: stable
domain: video-engineering
created: 2026-07-11
updated: 2026-07-11
importance: high
aliases: [GOP, Group of Pictures]
---

## Concept

The GOP defines how often an encode inserts a full I-frame, which trades compression efficiency against seek behavior and error propagation after a re-encode. Instagram enforces a hard cap of 60 frames (2s at 30fps). Rather than pick a fixed keyint from a scene-type preset, Metodologia Gabriel runs a lightweight `ffprobe` Pass-1 that measures the source's real cut rhythm and derives one of three strategies: `fixed` for regular cuts, `scenecut_only` for a single take, or `dual_coverage` for irregular cuts — the last pairing a calculated keyint with explicit forced-keyframe timestamps taken straight from the measured cut points.

## Connects to

Part of [[Hub — Video Engineering]], consumed by [[x264]] as the `keyint`/`scenecut` parameters (packed per [[x264-params Syntax]]), constrained the same way [[VBV (Video Buffering Verifier)]] is — as a hard Instagram ceiling, not a suggestion — and sharing its Pass-1 cut measurement with [[x264 Zones (Segment Bit Allocation)]].
