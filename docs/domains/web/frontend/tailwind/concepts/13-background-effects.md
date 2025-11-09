---
title: Backgrounds & Effects
status: draft
last_reviewed: 09-11-2025
---

# Backgrounds & Effects

## Why It Matters

- Tailwind provides background, border, and effect utilities to add depth without custom CSS.

## Core Ideas

- Backgrounds: colors (`bg-slate-900`), gradients (`bg-gradient-to-r`, `from-indigo-500`, `via-purple-500`, `to-pink-500`), positioning (`bg-cover`, `bg-center`).
- Borders & radius: `border`, `border-2`, `border-dashed`, rounded utilities (`rounded`, `rounded-lg`, `rounded-full`, corner-specific variants).
- Effects: shadows (`shadow-sm` → `shadow-2xl`), filters (`filter`, `blur`, `backdrop-blur`), blend modes (`mix-blend-multiply`, `bg-blend-overlay`).

## Real-World Scenario

- A landing page hero uses gradient backgrounds (`bg-gradient-to-r`), card shadows, and backdrop blur on overlay text to maintain contrast while showcasing imagery.

## Follow-up

- [ ] Design a hero section combining gradient background, soft shadow, and backdrop blur.
- [ ] Compare border utilities to outline variants to keep focus states accessible.
- [ ] Document preferred shadow intensities to maintain consistent depth cues.
