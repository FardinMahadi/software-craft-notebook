# Inheritance & Cascade

## Why It Matters

- Stylesheets resolve conflicts through inheritance and the cascade.
- Understanding the order prevents unexpected overrides and simplifies refactors.

## Core Ideas

- Some properties inherit (color, font); others don’t (margin, border). Control behavior with `inherit`, `initial`, `revert`, or `unset`.
- Cascade precedence: origin (user agent, user, author) → importance (`!important`) → specificity → source order.
- `@layer` groups styles (reset, base, components, utilities) to manage precedence explicitly.
- Keep selectors shallow and class-based to avoid specificity wars.

## Real-World Scenario

- A product page used multiple `!important` overrides. Introducing cascade layers for reset, base, components, and utilities eliminated conflicts and made future changes predictable.

## Examples

```css
@layer reset, base, components, utilities;

@layer reset {
  *, *::before, *::after {
    box-sizing: border-box;
  }
}

@layer base {
  body {
    color: #0f172a;
    font-family: system-ui, sans-serif;
  }
}
```

## Follow-up

- [ ] Inspect a component in dev tools to trace inherited values.
- [ ] Use `@layer` to define reset, base, and utilities, verifying override order.
- [ ] Remove unnecessary `!important` declarations by restructuring specificity.
---
title: Inheritance & Cascade
status: draft
last_reviewed: 09-11-2025
---

