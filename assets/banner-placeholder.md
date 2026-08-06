# Banner — Design Brief (v1.0 shipped)

**Status: done.** The final banner is `assets/banner.png` (1983×793px), embedded at the top of `profile/README.md`. This file is kept as the original design brief for reference and for the next banner iteration (see "Deviations" below).

## Spec

| Property | Value |
|---|---|
| Dimensions | 1280×640px (GitHub social preview ratio) |
| Safe area | ~1200×600px centered |
| Background | Graphite / near-black |
| Accent | `#0F6E63` |
| Text color | White |
| Content | "NextMind" wordmark, optionally a thin accent rule or minimal mark — nothing else |
| Typography | Single geometric sans-serif (e.g. Inter, Geist), generous tracking |
| Style | Flat, precise, no gradients, no illustration, no stock texture |
| Source format | SVG, exported to PNG for upload |

## What to avoid

- No mesh gradients or glow effects.
- No stock photography or abstract 3D renders.
- No taglines or marketing copy on the banner itself — the wordmark carries it.
- No emoji or icon clutter.

## Where it's used

- Embedded at the top of `profile/README.md`.
- Recommended for GitHub organization social preview too (Settings → General → Social preview) — see manual settings list in the implementation notes.

## Deviations from the original spec (v1.0 → v2.0 note)

The shipped banner (1983×793, ~2.5:1) differs from this brief in a few ways worth tracking for the next revision, not fixing now:

- Uses a night-sky/mountain photographic scene instead of a flat background — more atmospheric than the original "flat, no illustration" spec.
- Bakes the tagline and four pillar icons (Software, Automations, Intelligent Systems, Human First) directly into the image, whereas the brief assumed wordmark-only.
- Dimensions are wider (2.5:1) than the original 2:1 (1280×640) social-preview ratio.

None of these are problems — the banner was designed and approved outside this brief — but they're noted so a v2.0 banner revision (if one happens) starts from what shipped, not from this original spec.

## Status

**Shipped in GitHub Branding v1.0.**
