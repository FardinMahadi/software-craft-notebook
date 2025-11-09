# Inline-Block & Alignment

## Why It Matters

- `inline-block` bridges inline flow and block sizing, useful for menus or tag clouds without floats.
- Knowing alignment quirks helps when cleaning up legacy layouts.

## Core Ideas

- Inline-block elements sit on the same line but respect width/height.
- Whitespace between inline-block elements creates gaps; control with font-size adjustments, comments, or flexbox.
- `vertical-align` (`middle`, `top`, `bottom`) aligns inline and inline-block elements on the baseline.
- `text-align: center` on the parent centers inline-block children; flexbox offers more control.

## Real-World Scenario

- A badge list on a profile page uses inline-block elements. Designers align icons and labels without floats, and later migrate to flexbox knowing the trade-offs.

## Examples

```css
.badge {
  display: inline-block;
  padding: 0.5rem 1rem;
  background: #eef2ff;
  margin: 0 0.5rem 0.5rem 0;
  vertical-align: middle;
}

.badge-group {
  text-align: center;
}
```

## Follow-up

- [ ] Create a multi-column feature list using inline-blocks and adjust spacing.
- [ ] Experiment with `vertical-align` values to align icons and text.
- [ ] Refactor inline-block layouts into flexbox to compare maintainability.
---
title: Inline-Block & Alignment
status: draft
last_reviewed: 09-11-2025
---

