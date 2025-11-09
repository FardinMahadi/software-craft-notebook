---
title: HTML Colors
status: draft
last_reviewed: 09-11-2025
---

# HTML Colors

## Why It Matters

- Color choices impact branding, readability, and accessibility.
- Understanding color formats lets you adjust shades precisely and consistently.
- Accessible contrast ensures all users can read and interact with content.

## Core Ideas

- Named colors (`tomato`, `royalblue`) are quick but limited.
- HEX (`#RRGGBB`) is compact; shorthand (`#369`) expands to `#336699`.
- RGB (`rgb(255, 99, 71)`) and HSL (`hsl(9, 100%, 64%)`) expose channels for fine-tuning.
- RGBA/HSLA add transparency (`rgba(255, 99, 71, 0.5)`).
- Aim for 4.5:1 contrast for body text (3:1 for large/bold text) and avoid relying on color alone for state changes.

## Real-World Scenario

- A SaaS dashboard team receives a new brand palette. They convert the primary color to HEX for CSS variables, use HSL to create lighter button hovers, and check contrast ratios to ensure KPI cards remain legible in bright offices. Design feedback cycles shrink because everyone speaks the same color language.

## Examples

```html
<p style="color: #2563eb; background-color: rgba(37, 99, 235, 0.12);">
  Accent text with a matching transparent background for callouts.
</p>
<button style="background-color: hsl(220, 85%, 56%); color: white;">
  View Report
</button>
```

## Follow-up

- [ ] Convert one brand color across HEX, RGB, and HSL to learn each format.
- [ ] Use a contrast checker (e.g., WebAIM) to validate text/background combinations.
- [ ] Add focus styles that use both color and another cue (underline, outline) for clarity.
