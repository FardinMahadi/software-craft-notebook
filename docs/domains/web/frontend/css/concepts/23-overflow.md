# CSS Overflow

## Why It Matters

- Overflow decides what happens when content exceeds its container.
- Managing overflow keeps layouts tidy and enables scroll-based experiences.

## Core Ideas

- Common values: `visible` (default), `hidden`, `scroll`, `auto`.
- Control axes separately with `overflow-x` and `overflow-y`; `overflow: clip` strictly hides overflow without scrollbars.
- Scroll snap (`scroll-snap-type`) pairs with `overflow: auto` for carousels or timelines.
- Remember that hidden overflow can cut off focus outlines or tooltips—plan accordingly.

## Real-World Scenario

- A feature comparison table overflows on mobile. Wrapping it in a container with `overflow-x: auto` keeps the table intact while signaling users to scroll.

## Examples

```css
.table-wrapper {
  overflow-x: auto;
  -webkit-overflow-scrolling: touch;
}

.carousel {
  display: grid;
  grid-auto-flow: column;
  overflow-x: auto;
  scroll-snap-type: x mandatory;
}

.carousel > * {
  scroll-snap-align: center;
}
```

## Follow-up

- [ ] Create a horizontally scrollable table with `overflow-x: auto`.
- [ ] Implement scroll snapping for a testimonials carousel.
- [ ] Verify focus outlines remain visible when overflow is hidden.
---
title: CSS Overflow
status: draft
last_reviewed: 09-11-2025
---

