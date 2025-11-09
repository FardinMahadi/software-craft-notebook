---
title: Responsive Variants
status: draft
last_reviewed: 09-11-2025
---

# Responsive Variants

## Why It Matters

- Tailwind’s breakpoint prefixes make responsive design declarative and mobile-first.

## Core Ideas

- Default screens: `sm` (640px), `md` (768px), `lg` (1024px), `xl` (1280px), `2xl` (1536px); apply with `md:flex`, `lg:grid-cols-3`.
- Base utilities target all sizes; prefixed variants layer on top (`flex flex-col md:flex-row`).
- Extend `theme.screens` for custom breakpoints or raw queries (e.g., `"tall": { raw: "(min-height: 700px)" }`).
- Add `print` or `motion-safe` screens for specialized contexts.

## Real-World Scenario

- A feature list stacks vertically on mobile and switches to a three-column grid at `lg:` with only class changes—no custom media queries needed.

## Follow-up

- [ ] Refactor a responsive layout to use Tailwind breakpoints instead of custom media queries.
- [ ] Add a `print` screen to tailor print-friendly styles.
- [ ] Document custom screens so teammates apply consistent breakpoints.
