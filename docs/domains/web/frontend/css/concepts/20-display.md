# Display & Visibility

## Why It Matters

- `display` determines how elements participate in layout, from block flow to flexible containers.
- Visibility properties manage how elements appear without always removing them from the document flow.

## Core Ideas

- Common `display` values: `block`, `inline`, `inline-block`, `flex`, `grid`, `none`.
- `display: none;` removes the element from layout and accessibility tree (unless managed separately).
- `visibility: hidden;` hides an element but preserves space; `opacity: 0;` keeps it visible to screen readers but transparent.
- `display: contents;` flattens wrappers while keeping semantics—use with caution and test accessibility.
- `display: inline-flex;` creates flexible inline containers.

## Real-World Scenario

- A product card grid switches from two columns to one column on small screens. Using `display: grid` with responsive breakpoints keeps the markup clean while ensuring cards stack gracefully.

## Examples

```css
.card-grid {
  display: grid;
  gap: 1.5rem;
  grid-template-columns: repeat(auto-fit, minmax(16rem, 1fr));
}

.pill {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
}
```

## Follow-up

- [ ] Toggle between display values to observe layout changes.
- [ ] Build a component that switches between `flex` and `grid` at different breakpoints.
- [ ] Audit places where `display: none;` is used and confirm accessibility implications.
---
title: Display & Visibility
status: draft
last_reviewed: 09-11-2025
---

