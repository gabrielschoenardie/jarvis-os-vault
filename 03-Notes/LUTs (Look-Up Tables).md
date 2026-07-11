---
type: atomic
status: stable
domain: video-engineering
created: 2026-07-11
updated: 2026-07-11
importance: medium
aliases: [LUTs, LUT]
---

## Concept

A LUT is a precomputed color transform, mapping input RGB values to output RGB values, used to apply a consistent grade (log-to-rec709 conversion, a stylized look) across many clips without hand-tuning each one. In an encoding pipeline it is typically applied as an [[FFmpeg]] filter before the frame ever reaches the encoder.

## Connects to

LUTs sit early in the [[Hub — Video Engineering]] pipeline, upstream of [[x264]] encoding — get the color right first, since [[VMAF]] scores and [[VBV (Video Buffering Verifier)]] constraints only judge what happens after the LUT has already shaped the image.
