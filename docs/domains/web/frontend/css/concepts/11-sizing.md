# CSS Sizing

## Why It Matters

- Controlling width and height keeps layouts balanced across screens.
- Relative sizing improves responsiveness without manual breakpoints.

## Core Ideas

- Use `width`, `height`, and their min/max counterparts to define limits.
- Absolute units (`px`) offer precision; relative units (`%`, `em`, `rem`, `vw`, `vh`) adapt to context—prefer relatives for responsive designs.
- `min-width`/`min-height` prevent components from collapsing; `max-width` keeps text and images readable.
- `aspect-ratio` maintains proportions for media without padding hacks.

## Real-World Scenario

- A video gallery must stay 16:9 across devices. By setting `aspect-ratio: 16 / 9` and limiting width with `clamp()`, designers keep thumbnails consistent from mobile to desktop without extra wrappers.

## Examples

```css
.video {
  width: clamp(200px, 50vw, 640px);
  aspect-ratio: 16 / 9;
}

img {
  max-width: 100%;
  height: auto;
}
```

## Follow-up

- [ ] Constrain images with `max-width: 100%` to prevent overflow on small screens.
- [ ] Use `clamp()` to set responsive widths with safe minimum and maximum values.
- [ ] Audit components for fixed pixel widths and replace them with relative units where possible.
---
title: CSS Sizing
status: draft
last_reviewed: 09-11-2025
---

