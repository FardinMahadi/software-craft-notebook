---
title: CSS Optimization & Performance
status: draft
last_reviewed: 09-11-2025
---

# CSS Optimization & Performance

## Why It Matters

- Lean stylesheets load faster and keep interfaces snappy.
- Clear organization reduces regressions during future changes.

## Core Ideas

- Split critical CSS for inline delivery; defer or async-load the rest.
- Purge unused selectors in production builds, then minify and compress assets.
- Animate performant properties (transform, opacity) to avoid layout thrashing.
- Adopt a modular architecture (ITCSS, BEM, utility-first) to keep specificity low and predictable.

## Real-World Scenario

- A marketing site trimmed 40% of its CSS bundle by purging unused utility classes and shipping only above-the-fold styles inline. Lighthouse scores jumped, and subsequent refactors became simpler because selectors stayed tidy.

## Follow-up

- [ ] Audit CSS bundle size and identify unused selectors.
- [ ] Enable Lighthouse or performance profiler to measure style recalculation cost.
- [ ] Review architecture decisions and keep specificity low for easier overrides.
