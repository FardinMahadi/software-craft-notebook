# Opacity & Transparency

## Why It Matters

- Opacity affects element visibility and can create stacking contexts.
- Smooth fade animations rely on opacity changes.

## Core Ideas

- `opacity: 0` hides the element visually; `opacity: 1` is fully opaque.
- Opacity affects the element and all descendants. Use semi-transparent colors (`rgba`, `hsla`) when only the background should fade.
- `backdrop-filter` pairs with translucent backgrounds for frosted glass effects (include fallbacks).
- Animate opacity alongside `visibility` or `pointer-events` to keep hidden content accessible.

## Real-World Scenario

- A modal overlay fades in/out with transitions on `opacity`. Coupled with `visibility: hidden` and `pointer-events: none`, it stays accessible and doesn’t block interaction when hidden.

## Examples

```css
.overlay {
  opacity: 0;
  visibility: hidden;
  transition: opacity 200ms ease;
}

.overlay.is-open {
  opacity: 1;
  visibility: visible;
}

.glass-card {
  background: rgb(255 255 255 / 0.7);
  backdrop-filter: blur(12px);
}
```

## Follow-up

- [ ] Build a modal overlay that fades in using opacity transitions.
- [ ] Compare using `opacity` vs. semi-transparent background colors when only the backdrop should change.
- [ ] Test components for stacking context side effects when opacity < 1.
---
title: Opacity & Transparency
status: draft
last_reviewed: 09-11-2025
---

