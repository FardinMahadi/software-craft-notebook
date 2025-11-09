# CSS Backgrounds

## Why It Matters

- Backgrounds add depth and branding through color, imagery, and gradients.
- Understanding layering prevents readability or performance issues.

## Core Ideas

- Key properties: `background-color`, `background-image`, `background-repeat`, `background-position`, `background-size`, and `background-attachment`.
- Shorthand syntax lets you define multiple values at once: `background: color image position/size repeat attachment`.
- Layers are comma-separated; the first layer renders on top.
- Use gradients as overlays to improve contrast, especially when text sits on images.

## Real-World Scenario

- A marketing hero section needs a photo with readable text on top. Designers combine a background image with a semi-transparent gradient overlay so the copy remains legible while the brand photo stays visible.

## Examples

```css
.hero {
  background:
    linear-gradient(135deg, rgba(29, 78, 216, 0.75), rgba(34, 211, 238, 0.75)),
    url('/img/hero.jpg') center/cover no-repeat fixed;
  color: white;
}

.logo-wall {
  background: white url('/img/pattern.svg') repeat 0 0 / 120px 120px;
}
```

## Follow-up

- [ ] Create a banner with a gradient overlay on top of a background image.
- [ ] Experiment with `background-size: contain` versus `cover` to understand cropping.
- [ ] Audit large background images and consider lazy-loading or responsive sources to improve performance.
---
title: CSS Backgrounds
status: draft
last_reviewed: 09-11-2025
---

