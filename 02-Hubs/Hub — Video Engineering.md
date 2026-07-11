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

None of these parameters come from a fixed preset: [[Adaptive Content Analysis]] is the underlying method — measure the source, then derive. It feeds [[GOP (Group of Pictures)]] and its sibling [[x264 Zones (Segment Bit Allocation)]] (both from the same cut-structure measurement), and [[BM3D Denoise]]'s per-source strength. Getting the actual [[x264-params Syntax]] right when assembling these into one command is its own recurring gotcha. Before any of this runs, the [[Recompression Risk Score]] flags sources Instagram is likely to silently re-encode, and on the way out [[Audio Loudness (LUFS)]] and, for log or highlight-heavy footage, the [[DaVinci Wide Gamut (DWG)]] grading path round out the pipeline.

```dataview
LIST FROM "" WHERE domain = "video-engineering" AND type != "hub" SORT file.mtime DESC
```

## Related hubs

Bridges into [[Hub — AI Models]] via [[Bridge — Adaptive AI and VBV]], shares technique with [[Hub — Photography]] (color grading), and reports up to [[Hub — JARVIS OS Core]].
