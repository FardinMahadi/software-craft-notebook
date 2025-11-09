# CSS Icons

## Why It Matters

- Icons provide quick visual cues but must remain accessible and consistent.
- Choosing the right technique (font, SVG, background image) affects styling flexibility and performance.

## Core Ideas

- **Icon fonts** load glyphs via `@font-face` or CDN; pseudo-elements inject icons (`.btn::before { content: "\e001"; }`). Always pair with text or hidden labels.
- **SVG icons** offer full styling control. Inline SVG supports `fill`/`stroke` changes; external sprites reuse markup with `<use>`.
- **Background images** work for purely decorative icons; adjust padding to leave space for text.
- Mark decorative icons with `aria-hidden="true"` and provide screen-reader text elsewhere.

## Real-World Scenario

- A navigation bar uses inline SVGs for icons so designers can change stroke colors on hover. For legacy email templates, the team falls back to icon fonts but ensures each link has text labels for accessibility.

## Examples

```css
.btn::before {
  content: '';
  display: inline-block;
  width: 1em;
  height: 1em;
  margin-right: 0.5em;
  background: url('/icons/check.svg') no-repeat center/contain;
  aria-hidden: true;
}
```

## Follow-up

- [ ] Compare icon font and SVG approaches for the same navigation menu.
- [ ] Add `aria-hidden="true"` to purely decorative icons and provide hidden text for screen readers.
- [ ] Evaluate icon loading strategy to minimize duplicate requests.
---
title: CSS Icons
status: draft
last_reviewed: 09-11-2025
---

