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

A weighted checklist — bit depth, source codec, chroma subsampling, bitrate, color space tagging, fps, resolution, audio codec — scored before encoding to predict whether Instagram will silently re-encode the upload, destroying quality a second time in a pass nobody controls. A score of 5 or higher flags the source for correction before it ever reaches the encoder, rather than discovering the problem after upload.

## Connects to

Part of [[Hub — Video Engineering]], protecting the [[H.264]] delivery format's actual arrival quality, and reduced by the same bitrate discipline [[VBV (Video Buffering Verifier)]] already enforces during encoding.
