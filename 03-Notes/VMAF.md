---
type: atomic
status: stable
domain: video-engineering
created: 2026-07-11
updated: 2026-07-11
importance: high
aliases: [Video Multimethod Assessment Fusion]
---

## Concept

VMAF is Netflix's perceptual video quality metric: it compares an encoded output against its source and produces a score correlated with how a human would rate the quality, which is far more reliable than PSNR for tuning real encodes. It's the standard way to answer "did this [[x264]] setting actually cost visible quality."

## Connects to

VMAF is the feedback loop for [[Hub — Video Engineering]] work: run it after any change to [[x264]] settings, [[VBV (Video Buffering Verifier)]] constraints, or a [[LUTs (Look-Up Tables)]] grade to confirm the change didn't quietly degrade the [[H.264]] output.
