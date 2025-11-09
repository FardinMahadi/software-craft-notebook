# CSS Transitions

## Why It Matters

- Transitions add polish by animating property changes smoothly.
- Subtle motion improves perceived responsiveness and guides attention.

## Core Ideas

- Define transitions with `transition: property duration timing-function delay;`
- Common timing functions: `ease`, `linear`, `ease-in`, `ease-out`, or custom `cubic-bezier()`.
- Animate performant properties (`opacity`, `transform`) to avoid jank.
- Respect `prefers-reduced-motion` to disable or simplify motion for sensitive users.

## Real-World Scenario

- A primary button uses `transform` and `opacity` transitions for hover and focus, creating a gentle lift effect while remaining accessible to reduced-motion users.

## Examples

```css
.button {
  transition: background 200ms ease, transform 200ms ease;
}

.button:hover,
.button:focus-visible {
  background: #1d4ed8;
  transform: translateY(-2px);
}

@media (prefers-reduced-motion: reduce) {
  .button {
    transition: none;
  }
}
```

## Follow-up

- [ ] Add hover transitions to buttons and cards; audit performance in dev tools.
- [ ] Create a reduced-motion media query to disable intensive animations.
- [ ] Experiment with custom cubic-bezier curves to fine-tune motion.
---
title: CSS Transitions
status: draft
last_reviewed: 09-11-2025
---

