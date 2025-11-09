# CSS Positioning

## Why It Matters

- Positioning lets you fine-tune where elements appear relative to siblings, containers, or the viewport.
- Tooltips, sticky headers, and modals all rely on these positioning modes.

## Core Ideas

- `static` (default) participates in normal flow.
- `relative` offsets from the original position and creates a containing block for absolutely positioned children.
- `absolute` removes the element from flow and positions it relative to the nearest positioned ancestor.
- `fixed` anchors to the viewport and ignores scrolling.
- `sticky` behaves as relative until a scroll threshold, then sticks like fixed.
- `z-index` controls stacking order; properties like `transform` also create stacking contexts.

## Real-World Scenario

- A documentation site wants a table of contents that stays visible while readers scroll. Using `position: sticky; top: 4rem;` keeps the sidebar accessible without resorting to complex scripts.

## Examples

```css
.toc {
  position: sticky;
  top: 4rem;
}

.tooltip {
  position: absolute;
  top: 100%;
  left: 50%;
  transform: translateX(-50%);
  z-index: 10;
}
```

## Follow-up

- [ ] Implement a sticky sidebar that activates after scrolling past the header.
- [ ] Create a tooltip positioned absolutely within a relatively positioned container.
- [ ] Audit z-index values across your project to avoid stacking conflicts.
---
title: CSS Positioning
status: draft
last_reviewed: 09-11-2025
---

