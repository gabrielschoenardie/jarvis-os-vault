---
type: atomic
status: stable
domain: video-engineering
created: 2026-07-11
updated: 2026-07-11
importance: low
aliases: [LUFS]
---

## Concept

Instagram normalizes uploaded audio to -14 LUFS integrated automatically; delivering audio already at that target — rather than louder — avoids Instagram's own gain reduction introducing pumping or peak distortion on top of the original mix. Measured with FFmpeg's `ebur128`/`loudnorm` filters: a 2-pass `loudnorm` suits dynamic material (live ceremony audio, music with silence and applause), while a simpler volume-plus-limiter pass suits already-consistent studio tracks.

## Connects to

Part of [[Hub — Video Engineering]], applied through [[FFmpeg]]'s audio filter chain alongside the video pipeline in the same encode command.
