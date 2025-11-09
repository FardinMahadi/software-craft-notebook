# HTML Images

## Why It Matters

- Images add context and emotion to content when described and sized correctly.
- Proper markup keeps pages accessible and prevents layout shifts.
- Performance-conscious loading helps pages feel fast on all devices.

## Core Ideas

- `<img>` requires `src` and should include meaningful `alt` text; use `alt=""` for purely decorative images.
- Set `width` and `height` attributes to reserve layout space and avoid cumulative layout shift.
- Apply responsive CSS (`max-width: 100%`) so images scale within flexible containers.
- Use `loading="lazy"` to defer offscreen images, and consider `decoding="async"` for large assets.
- Prefer modern formats (WebP, AVIF) with fallbacks when broader support is needed.

## Real-World Scenario

- A product marketing page features team photos and UI screenshots. With descriptive alt text, the accessibility review passes quickly. Width/height attributes keep the layout stable during load, and `loading="lazy"` ensures the hero copy appears immediately for visitors on slower connections.

## Examples

```html
<img
  src="/assets/team-photo.webp"
  alt="Customer success team collaborating around a whiteboard"
  width="800"
  height="533"
  loading="lazy"
  decoding="async"
/>
```

## Follow-up

- [ ] Audit existing images to ensure alt text communicates purpose without visuals.
- [ ] Add explicit dimensions and responsive CSS to prevent layout shifts.
- [ ] Test lazy loading performance by simulating slow network conditions in dev tools.
---
title: HTML Images
status: draft
last_reviewed: 09-11-2025
---

