---
title: HTML Styles
status: draft
last_reviewed: 09-11-2025
---

# HTML Styles

## Why It Matters

- Inline styles are the quickest way to tweak appearance without editing external CSS.
- They help when experimenting, working in email templates, or applying conditional styles via scripts.
- Knowing their limitations encourages a clean transition to reusable stylesheets.

## Core Ideas

- Syntax: `style="property: value; property2: value2;"`.
- Inline styles have high specificity—they override class or external stylesheet rules.
- Useful properties include `color`, `background-color`, `font-family`, `font-size`, `text-align`, `margin`, and `padding`.
- Overusing inline styles leads to duplication; move repeated patterns into CSS classes.

## Real-World Scenario

- A marketing team updates a one-off promo email. Because many email clients strip external CSS, they apply inline styles for colors and typography. The campaign ships quickly, and once the promotion ends, developers incorporate lessons into reusable templates.

## Examples

```html
<body style="background-color: #f8fafc;">
  <h1 style="color: #0f172a; font-size: 2rem;">
    Study Dashboard
  </h1>
  <p style="font-family: 'Inter', sans-serif; margin-top: 0.5rem;">
    Track modules, labs, and reflections in one place.
  </p>
</body>
```

## Follow-up

- [ ] Add inline styles to a simple page, then refactor them into a separate stylesheet.
- [ ] Inspect elements in dev tools to see inline styles at the top of the cascade.
- [ ] Experiment with JavaScript: use `element.style.color = 'tomato'` to update an element dynamically.
