---
type: atomic
status: stable
domain: video-engineering
created: 2026-07-11
updated: 2026-07-11
importance: high
aliases: []
---

## Concept

FFmpeg is the command-line engine behind almost all practical video engineering work: decoding, encoding, filtering, and muxing audio/video streams. It exposes libavcodec (which implements encoders like [[x264]]) and libavfilter (used to apply things like [[LUTs (Look-Up Tables)]]) through a single CLI, which is why it sits at the center of most encoding pipelines rather than any GUI tool.

## Connects to

FFmpeg is the practical entry point into [[Hub — Video Engineering]] — nearly every other note in this cluster describes a concept FFmpeg implements or controls, most directly [[x264]] as its default H.264 encoder and [[VBV (Video Buffering Verifier)]] as a rate-control constraint you pass to it.
