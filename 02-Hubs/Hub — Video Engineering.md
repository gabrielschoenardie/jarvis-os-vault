---
type: hub
status: active
domain: video-engineering
created: 2026-07-11
updated: 2026-07-11
importance: high
aliases: []
---

## Definition

This hub covers the practical pipeline for encoding and grading video for delivery, especially short-form platforms like Instagram Reels — the domain behind Gabriel's encoder work.

## Contained clusters

[[FFmpeg]] is the tool that ties everything together: it runs [[x264]] to produce [[H.264]] streams constrained by [[VBV (Video Buffering Verifier)]], applies [[LUTs (Look-Up Tables)]] for color, and the result is measured with [[VMAF]]. [[Bridge — Adaptive AI and VBV]] connects this pipeline to model-driven encoding decisions.

```dataview
LIST FROM "" WHERE domain = "video-engineering" AND type != "hub" SORT file.mtime DESC
```

## Related hubs

Bridges into [[Hub — AI Models]] via [[Bridge — Adaptive AI and VBV]], shares technique with [[Hub — Photography]] (color grading), and reports up to [[Hub — JARVIS OS Core]].
