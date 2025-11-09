---
title: Flexbox & Grid Utilities
status: draft
last_reviewed: 09-11-2025
---

# Flexbox & Grid Utilities

## Why It Matters

- Tailwind makes flexbox and grid layouts declarative, speeding up responsive design.

## Core Ideas

- Flex direction/wrap: `flex-row`, `flex-col`, `flex-wrap` with responsive variants (`md:flex-row`).
- Flex sizing: `flex-1`, `flex-auto`, `flex-none`; alignment: `justify-between`, `items-end`, `self-center`.
- Grid columns/rows: `grid-cols-1`, `md:grid-cols-3`, `grid-cols-[repeat(auto-fit,minmax(16rem,1fr))]`, gaps (`gap-4`), spans (`col-span-2`).

## Real-World Scenario

- A dashboard stacks cards vertically on mobile (`flex-col`) and switches to a grid (`md:grid-cols-3`) on larger screens with a single class change.

## Follow-up

- [ ] Build a responsive dashboard switching from stacked flexboxes to multi-column grids.
- [ ] Experiment with grid auto-flow and span utilities to create masonry-like layouts.
- [ ] Document preferred patterns (flex vs grid) to keep team usage consistent.
