---
title: CSS Accessibility Considerations
status: draft
last_reviewed: 09-11-2025
---

# CSS Accessibility Considerations

## Why It Matters

- CSS can support or hinder accessibility; thoughtful styling keeps interfaces inclusive.

## Core Ideas

- Provide clear focus outlines with `:focus-visible`; never remove them without a strong alternative.
- Honor `prefers-reduced-motion` to limit animations for sensitive users.
- Maintain sufficient color contrast and avoid relying on color alone to convey meaning.
- Use visually hidden utilities (`.sr-only`) instead of `display: none` when content still needs to be announced by screen readers.

## Real-World Scenario

- A signup flow failed accessibility reviews because focus outlines were removed and error states used color only. Restoring outlines, adding icons/text, and respecting reduced-motion preferences brought the experience up to AA compliance.

## Examples

```css
:focus-visible {
  outline: 3px solid #22d3ee;
  outline-offset: 4px;
}

@media (prefers-reduced-motion: reduce) {
  * {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
  }
}
```

## Follow-up

- [ ] Audit styles with accessibility tools (axe, Lighthouse) to catch color and focus issues.
- [ ] Create reduced-motion alternatives and test with OS settings.
- [ ] Document focus styles and visually hidden utilities so contributors follow the same patterns.
