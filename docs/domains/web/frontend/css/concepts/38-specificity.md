# Specificity & `!important`

## Why It Matters

- Specificity decides which rules win when multiple selectors target the same element.
- Managing specificity keeps styles predictable and maintainable.

## Core Ideas

- Specificity weights: inline styles (1000), IDs (100), classes/attributes/pseudo-classes (10), type selectors/pseudo-elements (1), universal/combinators (0).
- Favor low-specificity selectors (single classes) to keep overrides simple.
- Use utility classes or cascade layers instead of chaining IDs or `!important`.
- `!important` should be sparse—reserved for utilities or third-party overrides and difficult to supersede.

## Real-World Scenario

- A component library standardized on class-based selectors and reserved `!important` for `.hidden` utilities. Developers now avoid accidental overrides and rarely reach for specificity hacks.

## Examples

```css
/* Low specificity utility */
.text-muted {
  color: #64748b;
}

/* Specific component override */
.card .card-title {
  margin-bottom: 0.5rem;
}
```

## Follow-up

- [ ] Analyze conflicting styles and calculate specificity to understand outcomes.
- [ ] Refactor high-specificity selectors into class-based ones to simplify overrides.
- [ ] Audit `!important` usage and document intentional cases.
---
title: Specificity & !important
status: draft
last_reviewed: 09-11-2025
---

# Specificity & `!important`

Specificity rankings determine which rule wins when multiple selectors target the same element.

## Specificity Weights

- Inline styles: 1000
- IDs: 100
- Classes, attributes, pseudo-classes: 10
- Type selectors, pseudo-elements: 1
- Universal selector, combinators: 0

## Strategies

- Favor low-specificity selectors (single classes) for predictable overrides.
- Use utility classes or cascade layers to manage precedence.

## `!important`

- Overrides normal cascade order; use sparingly for utilities or third-party overrides.
- Hard to supersede—requires another `!important` with equal or higher specificity.

## Practice

- Analyze conflicting styles and calculate specificity to understand outcomes.
- Refactor high-specificity selectors into class-based ones to simplify overrides.
