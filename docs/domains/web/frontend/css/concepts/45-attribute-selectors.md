---
title: Attribute Selectors
status: draft
last_reviewed: 09-11-2025
---

# Attribute Selectors

## Why It Matters

- Attribute selectors style elements based on attribute presence or value patterns, reducing the need for extra classes.

## Core Ideas

- Variants: presence `[attr]`, exact `[attr="value"]`, word `[attr~="value"]`, prefix `[attr|="value"]`, starts `[attr^="value"]`, ends `[attr$="value"]`, contains `[attr*="value"]`.
- Combine with pseudo-classes (e.g., `[aria-invalid="true"]:focus`) for rich state styling.

## Real-World Scenario

- External links receive an icon using `a[target="_blank"]::after`, helping users recognize they’re leaving the site without touching HTML.

## Examples

```css
a[target="_blank"]::after {
  content: '↗';
  margin-left: 0.25rem;
}

input[type^="tel"] {
  font-variant-numeric: tabular-nums;
}
```

## Follow-up

- [ ] Highlight external links using attribute selectors instead of additional classes.
- [ ] Style validation states by targeting `input[aria-invalid="true"]`.
- [ ] Audit markup for reusable attribute patterns (data attributes, ARIA states) that simplify styling.
