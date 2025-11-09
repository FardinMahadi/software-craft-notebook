---
title: CSS Selectors
status: draft
last_reviewed: 09-11-2025
---

# CSS Selectors

## Why It Matters

- Selectors decide which elements receive styles; precise targeting keeps stylesheets efficient.
- Mastery prevents overusing classes and reduces specificity battles later.

## Core Ideas

- Type (`p`), class (`.card`), ID (`#hero`), and universal (`*`) selectors cover most cases.
- Combine selectors to control scope: group (`h1, h2`), descendant (`.card p`), child (`.card > p`), and sibling (`.card + .card`, `.card ~ .card`).
- Attribute selectors (`input[type="email"]`) style elements based on attribute values.
- Specificity increases with IDs and inline styles—prefer classes and structured selectors for flexibility.

## Real-World Scenario

- A design system introduces card components with consistent headings and button styles. By chaining selectors (`.card > h2`, `.card .cta-button`), the team updates the look everywhere without touching markup, and other modules stay unaffected.

## Examples

```css
/* Basic selectors */
h1 {
  font-size: clamp(2rem, 3vw, 3rem);
}
.card {
  border-radius: 1rem;
  padding: 1.5rem;
}

/* Attribute selector */
input[type='email'] {
  border-color: #2563eb;
}
```

## Follow-up

- [ ] Create a card component with nested selectors for headings and paragraphs.
- [ ] Use attribute selectors to highlight required form fields.
- [ ] Inspect the computed specificity of your selectors using browser dev tools.
