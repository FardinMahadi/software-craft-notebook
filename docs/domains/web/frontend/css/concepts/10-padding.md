# CSS Padding

## Why It Matters

- Padding controls the breathing room inside components, improving readability and click targets.
- Consistent inner spacing aligns with your spacing scale and supports responsive layouts.

## Core Ideas

- Shorthand syntax mirrors margins: `padding: 1rem;` for all sides, `padding: vertical horizontal;`, `padding: top right bottom left`.
- Logical properties (`padding-block`, `padding-inline`) adapt to different writing directions, aiding internationalization.
- Backgrounds extend through padding, so combine with border radius for pills or badges.

## Real-World Scenario

- A call-to-action button feels cramped on mobile. Increasing padding and using logical properties ensures comfortable touch targets whether the layout is LTR or RTL.

## Examples

```css
.cta {
  padding: 0.75rem 1.5rem;
  border-radius: 999px;
  background: var(--color-primary);
  color: white;
}

article {
  padding-inline: clamp(1rem, 5vw, 2.5rem);
  padding-block: 2rem;
}
```

## Follow-up

- [ ] Create callout boxes with generous padding and compare readability.
- [ ] Replace traditional padding with logical properties to support RTL layouts.
- [ ] Audit button components to ensure padding meets minimum touch target guidelines (44px).
---
title: CSS Padding
status: draft
last_reviewed: 09-11-2025
---

