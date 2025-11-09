---
title: CSS Syntax
status: draft
last_reviewed: 09-11-2025
---

# CSS Syntax

## Why It Matters

- Clean syntax keeps stylesheets predictable and easier to debug.
- Consistent structure lets teams share rules without unexpected side effects.
- Browsers ignore invalid declarations, so catching typos early saves time.

## Core Ideas

- A rule consists of a selector and a declaration block wrapped in braces.
- Declarations use `property: value;` pairs; end each with a semicolon.
- Values can be strings (`"Inter", sans-serif`), numbers (`16px`, `1.5rem`), or keywords (`none`, `auto`).
- Comments use `/* ... */` and can span multiple lines (avoid nesting).

## Real-World Scenario

- A design system team standardizes corporate intranet styling. Marketing drops a seasonal banner into the stylesheet; because everyone follows the same syntax conventions, nothing else breaks and reviewers can scan changes quickly.

## Examples

```css
/* Rule structure */
.cta-button {
  background-color: #2563eb;
  color: white;
  padding: 0.75rem 1.5rem;
}

/* Comments explain intent */
/* TODO: Replace brand color after rebrand */
```

## Follow-up

- [ ] Write a rule targeting `p` elements and set font size, line height, and color.
- [ ] Introduce an invalid property to observe how the browser ignores only that declaration.
- [ ] Configure your editor or formatter (Prettier) to enforce consistent spacing and semicolons.
