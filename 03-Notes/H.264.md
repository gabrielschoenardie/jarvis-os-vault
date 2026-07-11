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

H.264 (AVC) is the video compression standard that dominates streaming and mobile delivery, including Instagram Reels and similar short-form platforms. It works by predicting each frame from neighboring frames and encoding only the difference, with quality and bitrate tradeoffs controlled by an encoder implementation such as [[x264]].

## Connects to

H.264 is the deliverable format most of [[Hub — Video Engineering]] is organized around: [[x264]] is the reference encoder that implements it, [[VBV (Video Buffering Verifier)]] is the rate-control model H.264 streams must satisfy for smooth playback, and [[VMAF]] is how you measure whether an H.264 encode actually preserved visual quality.
