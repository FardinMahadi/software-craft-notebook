---
title: Transitions & Animations
status: draft
last_reviewed: 09-11-2025
---

# Transitions & Animations

## Why It Matters

- Tailwind utilities bring motion to interfaces without manual CSS.

## Core Ideas

- Transition helpers: `transition`, `transition-colors`, `transition-opacity`, durations (`duration-150`), timing (`ease-in-out`).
- Animation helpers: prebuilt `animate-spin`, `animate-ping`, `animate-bounce`, `animate-pulse`; extend `animation` with custom keyframes in `tailwind.config.js`.
- Transform utilities (`scale-95`, `rotate-3`, `translate-y-4`) combine with `origin-*` for pivot control.

## Real-World Scenario

- Hovering a CTA button uses `transition` and `transform` to create a gentle lift, while a custom keyframe animates skeleton loaders during data fetches.

## Follow-up

- [ ] Add subtle hover transitions to buttons while respecting reduced-motion settings.
- [ ] Extend Tailwind with a custom keyframe animation for skeleton loaders.
- [ ] Document motion guidelines so transitions stay consistent across the product.
