---
type: atomic
status: stable
domain: video-engineering
created: 2026-07-11
updated: 2026-07-11
importance: medium
aliases: [x264-params]
---

## Concept

`-x264-params` packs many settings behind one flag, separated by colons — but three parameters (`deblock`, `psy-rd`, `zones`) carry sub-values separated by commas instead, and `zones` adds a slash on top to separate distinct zones. Mixing colon and comma inside one of those three doesn't error loudly; it silently breaks the parser's token boundaries, producing an encode with a parameter quietly dropped or misread.

## Connects to

Part of [[Hub — Video Engineering]], the serialization contract for every [[x264]] parameter discussed in this vault, including [[GOP (Group of Pictures)]]'s `keyint`/`scenecut` and the comma-and-slash exception used by [[x264 Zones (Segment Bit Allocation)]].
