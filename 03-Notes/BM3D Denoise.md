---
type: atomic
status: stable
domain: video-engineering
created: 2026-07-11
updated: 2026-07-11
importance: medium
aliases: [BM3D, Block-Matching 3D]
---

## Concept

BM3D is the gold-standard denoiser for coarse or chromatic noise, run inside a float32 pipeline rather than as a plain FFmpeg filter. Its sigma_spatial and sigma_chroma strength parameters are derived from measured noise rather than chosen from a preset, and are clamped tighter whenever skin is detected in-frame — pushed too hard, it produces "waxy skin," a plastic, texture-less look that is the visible symptom of over-denoising.

## Connects to

Part of [[Hub — Video Engineering]], validated against [[VMAF]] — denoised output must score ≥ the un-denoised source, or the filter is destroying real detail rather than noise — and one of the pipelines whose strength [[Adaptive Content Analysis]] derives from measured source features instead of a fixed preset.
