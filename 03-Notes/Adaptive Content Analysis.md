---
type: atomic
status: stable
domain: video-engineering
created: 2026-07-11
updated: 2026-07-11
importance: high
aliases: [Metodologia Gabriel]
---

## Concept

Encoding parameters are derived from measured source features — noise profile, spatial and temporal complexity, highlight/shadow load, skin ratio, color temperature — rather than picked from a preset keyed to a scene "type." Two scenes of the same nominal type (a dim indoor ceremony versus a sunlit outdoor one) can have entirely different noise profiles, so a type-based preset is guessing where a measurement can know. Every parameter in this vault's video-engineering cluster derived "adaptively" — [[GOP (Group of Pictures)]]'s keyint, [[BM3D Denoise]]'s sigma, highlight rolloff — traces back to this same principle.

## Connects to

Part of [[Hub — Video Engineering]], and a concrete, domain-specific instance of [[Iterative Refinement]] and [[Fail Fast, Fail Cheap]] from [[Hub — Principles]] — measure the real source before deciding, the same discipline applied to encoding instead of software design.
