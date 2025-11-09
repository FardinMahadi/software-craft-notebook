# CSS Colors

## Why It Matters

- Color choices impact branding, readability, and accessibility.
- Consistent color systems simplify theming and future updates.

## Core Ideas

- Supported formats: named keywords (`tomato`), hex (`#1d4ed8`, `#1d8`), RGB/RGBA (`rgb(29 78 216)`, `rgba(29 78 216 / 0.2)`), and HSL/HSLA (`hsl(221deg 83% 53%)`).
- CSS custom properties (`--color-primary`) centralize palettes for reuse.
- Maintain contrast ratios (4.5:1 for small text, 3:1 for large/bold text); test variants for color vision deficiencies.

## Real-World Scenario

- A product refresh introduces new brand colors. By defining variables in `:root`, engineers update buttons, alerts, and links across the UI with minimal changes while ensuring contrast guidelines are met.

## Examples

```css
:root {
  --color-primary: hsl(221deg 83% 53%);
  --color-primary-soft: hsl(221deg 83% 90%);
}

.button {
  background: var(--color-primary);
  color: white;
}

.button:hover {
  background: color-mix(in srgb, var(--color-primary) 90%, white 10%);
}
```

## Follow-up

- [ ] Define a color palette with custom properties and apply it to buttons and alerts.
- [ ] Convert a hex palette to HSL to tweak saturation and lightness precisely.
- [ ] Use a contrast checker to validate key UI components.

---

title: CSS Colors
status: draft
last_reviewed: 09-11-2025

---
