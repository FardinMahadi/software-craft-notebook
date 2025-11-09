# Pseudo-Elements

## Why It Matters

- Pseudo-elements add decorative or helper content without modifying HTML.
- They keep templates clean while enabling rich visual treatments.

## Core Ideas

- `::before` and `::after` insert generated content before/after element content.
- `::first-line`, `::first-letter` style typography accents.
- `::selection` customizes highlighted text color.
- Generated content still requires `content` property (even empty string) to render.

## Real-World Scenario

- A feature list uses `::before` to create checkmark bullets, keeping the HTML simple while improving visual hierarchy.

## Examples

```css
.badge::before {
  content: '';
  display: inline-block;
  width: 0.75rem;
  height: 0.75rem;
  border-radius: 9999px;
  background: #22c55e;
  margin-right: 0.5rem;
}

blockquote::before {
  content: '“';
  font-size: 3rem;
  color: rgb(99 102 241 / 0.4);
}
```

## Follow-up

- [ ] Create custom list markers using `::before`.
- [ ] Design quote blocks with decorative quotation marks using `::before` and `::after`.
- [ ] Experiment with `::selection` to match brand highlight colors.
---
title: Pseudo-Elements
status: draft
last_reviewed: 09-11-2025
---

