# CSS Fonts

## Why It Matters

- Fonts set tone and improve readability across devices.
- Thoughtful fallback stacks prevent awkward jumps when custom fonts fail.

## Core Ideas

- Define font stacks with fallbacks: `font-family: "Inter", system-ui, sans-serif;`
- Control `font-size`, `font-weight`, `font-style`, `font-variant`, and `font-stretch`; shorthand `font: 600 1rem/1.5 "Inter", sans-serif;`
- Load web fonts via `@font-face` or hosted services; preload critical weights to reduce flashes of unstyled text.
- Use responsive sizing with relative units and `clamp()`.

## Real-World Scenario

- A blog introduces a new brand font. By preloading the regular and bold weights and defining a solid fallback stack, readers see consistent typography without layout shifts, even on slower connections.

## Examples

```css
@font-face {
  font-family: 'Acme Sans';
  src: url('/fonts/acme-sans.woff2') format('woff2');
  font-weight: 400;
  font-display: swap;
}

body {
  font-family: 'Acme Sans', system-ui, sans-serif;
  font-size: clamp(1rem, 1.5vw, 1.125rem);
}
```

## Follow-up

- [ ] Integrate a variable font and adjust its axes via CSS custom properties.
- [ ] Audit font loading strategy to minimize layout shift and blocking time.
- [ ] Review fallback stacks to ensure they match the intended tone.
---
title: CSS Fonts
status: draft
last_reviewed: 09-11-2025
---

