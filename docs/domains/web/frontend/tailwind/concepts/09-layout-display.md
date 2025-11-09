---
title: Layout & Display Utilities
status: draft
last_reviewed: 09-11-2025
---

# Layout & Display Utilities

## Why It Matters

- Tailwind’s display and alignment utilities build layouts quickly without custom CSS.

## Core Ideas

- Display modes: `block`, `inline`, `inline-block`, `flex`, `inline-flex`, `grid`, `inline-grid`, `hidden`.
- Alignment helpers: `justify-between`, `items-center`, `place-items-center`, plus `content-*` and `self-*` variants.
- Overflow utilities: `overflow-hidden`, `overflow-x-auto`, scroll snap (`snap-x`, `snap-mandatory`, `snap-center`).
- Use `flow-root` or flex/grid instead of clearfix hacks.

## Real-World Scenario

- A dashboard header combines `flex`, `items-center`, and `justify-between` to align brand, search, and profile actions without writing new CSS.

## Follow-up

- [ ] Assemble a card layout using display and alignment utilities only.
- [ ] Replace legacy clearfix solutions with `flex`, `grid`, or `flow-root` utilities.
- [ ] Build a horizontal scroller using overflow and scroll-snap utilities.

---
**Notes**
- Confirm Tailwind version for scrollbar/scroll-snap utilities (`snap-*`) and new viewport units before using in production.
- Review official docs on negative translate classes to ensure cross-browser behavior for transforms.
