# CSS Units

## Why It Matters

- Choosing the right units keeps layouts flexible and accessible.
- Responsive design relies on relative measurements instead of fixed pixels.

## Core Ideas

- Absolute units (`px`, `cm`, `pt`) suit print or icons but lack flexibility on the web.
- Relative units adapt to context: `em` (current element size), `rem` (root size), `vw`/`vh` (viewport), `vmin`/`vmax`, modern variants (`svh`, `lvh`, `dvh`), and `ch` (character width).
- Mix units with `calc()` and guide fluid values with `clamp(min, preferred, max)`.
- Respect user font settings by basing spacing and typography on `rem`.

## Real-World Scenario

- A hero section uses `clamp()` with `vw` and `rem` so headings scale up on large screens but never shrink below readable sizes on mobile.

## Examples

```css
body {
  font-size: 1rem; /* respect user settings */
}

.hero {
  padding-block: clamp(3rem, 10vh, 6rem);
}

.sidebar {
  width: min(22rem, 90vw);
}
```

## Follow-up

- [ ] Convert fixed pixel values to `rem` to respect user font settings.
- [ ] Use viewport units for hero sections and combine with `min()` or `clamp()` to constrain extremes.
- [ ] Explore `dvh`/`svh` for mobile browsers that adjust viewport height when toolbars appear.
---
title: CSS Units
status: draft
last_reviewed: 09-11-2025
---

