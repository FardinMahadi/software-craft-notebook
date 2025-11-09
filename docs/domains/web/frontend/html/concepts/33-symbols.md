# HTML Symbols

## Why It Matters

- Symbols provide quick visual cues for status, currency, math, or navigation without custom images.
- Properly annotated symbols improve accessibility and maintain consistent styling.
- Relying on Unicode keeps bundles light compared to image sprites.

## Core Ideas

- Use Unicode characters directly (✓, ★, →) or via entities (`&hearts;`, `&#x2665;`).
- Verify that your font stack supports chosen symbols; fallback fonts can change appearance.
- Provide accessible labels: hide the symbol from screen readers and supply text with `.sr-only`, or include descriptive text alongside.
- Consider SVG or icon fonts when you need stylistic control or complex shapes.

## Real-World Scenario

- A SaaS dashboard adds a legend explaining project status. Each row uses a Unicode symbol with accompanying text and screen-reader labels, ensuring colorblind users and assistive tech understand the meaning.

## Examples

```html
<p>
  <span aria-hidden="true" class="status status-success">✓</span>
  <span class="sr-only">Completed</span>
  Export finished successfully.
</p>

<p>
  <span aria-hidden="true">★</span>
  <span>Marked as favorite</span>
</p>
```

## Follow-up

- [ ] Build a status legend using symbols and associated labels.
- [ ] Test pages on multiple devices and browsers to confirm symbols render correctly.
- [ ] Evaluate when to switch from Unicode symbols to SVGs for design consistency.
---
title: HTML Symbols
status: draft
last_reviewed: 09-11-2025
---

