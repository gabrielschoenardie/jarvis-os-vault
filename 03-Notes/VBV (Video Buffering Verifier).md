---
type: atomic
status: stable
domain: video-engineering
created: 2026-07-11
updated: 2026-07-11
importance: high
aliases: [VBV]
---

## Concept

VBV models a decoder's input buffer as a leaky bucket: bits arrive at a capped rate and drain as frames decode, and the encoder must never let that virtual buffer overflow or underflow. Platforms like Instagram enforce their own VBV constraints (maxrate/bufsize) on top of H.264, so an encode that looks fine locally can still fail platform ingest if VBV isn't respected.

## Connects to

VBV is a rate-control constraint layered on top of [[H.264]], enforced in practice by passing maxrate/bufsize flags to [[x264]] through [[FFmpeg]]. It belongs to [[Hub — Video Engineering]] alongside [[VMAF]], which is how you verify a VBV-constrained encode didn't sacrifice too much quality to hit its buffer target.
