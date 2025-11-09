# Responsive Design Strategies

## Why It Matters

- Users access content on phones, tablets, desktops, and TVs.
- Responsive design ensures layouts adapt gracefully without maintaining separate codebases.

## Core Ideas

- Start mobile-first: build a stacked layout, then enhance with media queries as space grows.
- Choose breakpoints based on content (e.g., when cards feel cramped), not device names.
- Use fluid units (`%`, `vw`, `clamp()`) and custom properties to scale typography and spacing.
- Experiment with container queries (`@container`) to adapt components by their parent size (provide fallbacks for unsupported browsers).

## Real-World Scenario

- A marketing landing page begins as a single column. At 48rem the features become a two-column grid, and at 64rem a sidebar appears for testimonials—all from one codebase.

## Examples

```css
.hero {
  padding: clamp(2rem, 6vw, 4rem);
}

@media (min-width: 48rem) {
  .feature-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(16rem, 1fr));
    gap: 1.5rem;
  }
}

@container card (min-width: 30rem) {
  .card-horizontal {
    display: grid;
    grid-template-columns: 12rem 1fr;
    gap: 1rem;
  }
}
```

## Follow-up

- [ ] Build a responsive layout that shifts from stacked to two-column at 48rem and adds a sidebar at 64rem.
- [ ] Audit responsive behavior using device emulators and real hardware.
- [ ] Explore container queries with fallbacks for browsers that lack support.
---
title: Responsive Design Strategies
status: draft
last_reviewed: 09-11-2025
---

