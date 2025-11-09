# Flexbox Fundamentals

## Why It Matters

- Flexbox shines for one-dimensional layouts, distributing space along a row or column.
- It simplifies alignment, spacing, and reordering compared to floats.

## Core Ideas

- Flex container properties: `display: flex`, `flex-direction`, `justify-content` (main-axis alignment), `align-items` (cross-axis), `gap`.
- Flex item properties: `flex-grow`, `flex-shrink`, `flex-basis`, shorthand `flex: 1 1 12rem;`, plus `align-self`.
- Flexbox wraps and reflows gracefully with `flex-wrap` and `align-content`.

## Real-World Scenario

- A responsive toolbar spaces navigation links and actions evenly. On small screens, `flex-wrap: wrap` stacks items while `justify-content: space-between` keeps controls reachable.

## Examples

```css
.toolbar {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 1rem;
  flex-wrap: wrap;
}

.card-list {
  display: flex;
  gap: 1.5rem;
}

.card-list > * {
  flex: 1 1 16rem;
}
```

## Follow-up

- [ ] Build a responsive navigation bar that wraps on smaller screens.
- [ ] Use flex properties to create equal-height cards without fixed heights.
- [ ] Experiment with `align-self` to adjust individual items inside a flex container.
---
title: Flexbox Fundamentals
status: draft
last_reviewed: 09-11-2025
---

