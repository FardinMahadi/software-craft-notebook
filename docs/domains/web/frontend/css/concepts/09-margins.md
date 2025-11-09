# CSS Margins

## Why It Matters

- Margins create breathing room outside an element, separating it from neighbors.
- Consistent spacing systems make layouts feel intentional and aligned.

## Core Ideas

- Shorthand syntax: `margin: 1rem;` applies to all sides, `margin: 1rem 2rem;` sets vertical then horizontal, `margin: top right bottom left`.
- Auto margins center block elements with a defined width (`margin: 0 auto;`) or via logical properties (`margin-inline: auto;`).
- Vertical margins can collapse between adjacent elements; prevent collapse with padding, borders, or `overflow: auto` on containers.

## Real-World Scenario

- A marketing site establishes an 8px spacing scale. Designers apply margin utilities to keep consistent gaps between sections; when they notice unexpected collapse between headings, they adjust the container padding instead of sprinkling extra rules.

## Examples

```css
.content {
  max-width: 60ch;
  margin: 0 auto;
}

h2 {
  margin: 2rem 0 1rem;
}

.card-stack > * + * {
  margin-top: 1.5rem;
}
```

## Follow-up

- [ ] Build a vertical rhythm scale and apply consistent margins between headings and paragraphs.
- [ ] Demonstrate margin collapse by nesting sections, then resolve it using padding or overflow.
- [ ] Document spacing tokens or utilities (e.g., `.mt-4`) to keep spacing consistent across components.
---
title: CSS Margins
status: draft
last_reviewed: 09-11-2025
---

