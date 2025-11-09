# Z-Index & Stacking Order

## Why It Matters

- Overlays, tooltips, and modals rely on predictable stacking order.
- Mismanaged `z-index` leads to hidden UI or accessibility issues.

## Core Ideas

- `z-index` works only on positioned elements (`position` not `static`).
- Higher `z-index` values sit in front of lower ones within the same stacking context.
- New stacking contexts can form via `transform`, `opacity < 1`, `filter`, `position: fixed`, and `z-index` on flex/grid children.
- Establish a scale (e.g., 10 for dropdowns, 20 for modals) to avoid arbitrary large numbers.

## Real-World Scenario

- A customer noticed toast notifications hiding behind the header. By documenting z-index layers (header 50, toast 60, modal 100), the team prevents future conflicts and keeps overlays visible.

## Examples

```css
.modal {
  position: fixed;
  z-index: 100;
}

.toast {
  position: fixed;
  z-index: 60;
}
```

## Follow-up

- [ ] Build a modal overlay ensuring it appears above sticky headers and other UI layers.
- [ ] Document common stacking contexts in your project to prevent z-index battles.
- [ ] Inspect stacking contexts in dev tools when debugging hidden elements.
---
title: Z-Index & Stacking Order
status: draft
last_reviewed: 09-11-2025
---

