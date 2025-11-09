---
title: Positioning & Z-Index
status: draft
last_reviewed: 09-11-2025
---

# Positioning & Z-Index

## Why It Matters

- Positioning utilities handle sticky headers, tooltips, and overlays without custom CSS.

## Core Ideas

- Position classes: `relative`, `absolute`, `fixed`, `sticky`.
- Inset helpers: `inset-0`, `inset-x-4`, `top-1/2`, with negative offsets like `-top-6` and transforms (`-translate-y-1/2`).
- Z-index scale: `z-0` through `z-50`; extend `zIndex` for custom stacks.

## Real-World Scenario

- A sticky sidebar uses `sticky top-16` to stay visible while content scrolls. Tooltips rely on `absolute` positioning and `z-40` to layer above cards.

## Follow-up

- [ ] Create a sticky header and confirm it stays above scrolling content.
- [ ] Layer tooltips or modals using positioning and z-index utilities.
- [ ] Document z-index conventions so overlays remain predictable.
