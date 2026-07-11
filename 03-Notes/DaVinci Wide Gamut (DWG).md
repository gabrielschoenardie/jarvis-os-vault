---
type: atomic
status: stable
domain: video-engineering
created: 2026-07-11
updated: 2026-07-11
importance: low
aliases: [DWG, DaVinci Wide Gamut]
---

## Concept

DWG is the wide-gamut working color space used mid-pipeline in Cineon-style grading (not ACEScg): Rec.709 gamma is decoded to linear, matrixed into DWG, graded there in log space, then tone-mapped and matrixed back to Rec.709 before a film-look LUT is applied. Working in this intermediate log space lets exposure and saturation adjustments happen without clipping highlights the way operating directly in 8-bit YUV would.

## Connects to

Part of [[Hub — Video Engineering]], the color space feeding into whichever [[LUTs (Look-Up Tables)]] is applied last, and the reason a float32 grading path can score higher on [[VMAF]] than an 8-bit pipeline specifically on high-highlight-load or high-noise source material.
