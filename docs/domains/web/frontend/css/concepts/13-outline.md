# CSS Outline

## Why It Matters

- Outlines highlight elements without affecting layout, ideal for focus styles and debugging.
- Clear focus indicators improve keyboard accessibility.

## Core Ideas

- Outline sits outside the border and doesn’t take up space.
- Control width, style, color, and offset (`outline-width`, `outline-style`, `outline-color`, `outline-offset`).
- Use `:focus-visible` or `:focus` to apply outlines for keyboard users while avoiding noisy styles on mouse click.

## Real-World Scenario

- A sign-up form fails accessibility reviews because focus states rely on subtle color shifts. Adding a distinct outline with offset makes the focused field obvious, helping users tab through the form confidently.

## Examples

```css
button:focus-visible {
  outline: 3px solid #22d3ee;
  outline-offset: 4px;
}

.debug *:focus {
  outline: 1px dashed tomato;
}
```

## Follow-up

- [ ] Design accessible focus indicators using outline and offset.
- [ ] Use outlines temporarily during debugging to visualize element boundaries.
- [ ] Document your app’s focus styles so all components stay consistent.
---
title: CSS Outline
status: draft
last_reviewed: 09-11-2025
---

