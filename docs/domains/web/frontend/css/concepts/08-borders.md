# CSS Borders

## Why It Matters

- Borders frame elements, signal interactivity, and help build visual hierarchy.
- Thoughtful border choices keep interfaces clean without relying solely on shadows.

## Core Ideas

- Control width, style (`solid`, `dashed`, `double`, `none`), and color individually or with shorthand (`border: 1px solid #e2e8f0;`).
- Use `border-radius` for rounded corners and `border-top/right/bottom/left` for per-side adjustments.
- `border-image` and gradients create decorative effects; `outline` emphasizes focus without affecting layout.

## Real-World Scenario

- A dashboard uses subtle 1px borders to separate cards. During dark mode work, designers adjust just the custom properties driving border color, preserving hierarchy with minimal code changes.

## Examples

```css
.card {
  border: 1px solid rgb(226 232 240);
  border-radius: 1rem;
  box-shadow: 0 10px 30px rgb(15 23 42 / 0.05);
}

.pill {
  border: 2px dashed var(--color-primary);
  border-radius: 999px;
}
```

## Follow-up

- [ ] Design cards with different border radii to explore visual hierarchy.
- [ ] Combine `border` and `box-shadow` for elevated components.
- [ ] Experiment with `border-image` or gradient borders for feature callouts.
---
title: CSS Borders
status: draft
last_reviewed: 09-11-2025
---

