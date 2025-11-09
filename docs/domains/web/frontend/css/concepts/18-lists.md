# Styling Lists

## Why It Matters

- Lists power navigation menus, feature checklists, and ordered instructions.
- Clear styling keeps items readable while preserving semantic structure.

## Core Ideas

- Control markers with `list-style-type` (`disc`, `decimal`, etc.) and remove them when necessary (`list-style: none;`)—but replace with alternative cues.
- `list-style-position: outside` (default) or `inside` affects marker alignment with text.
- Custom markers via pseudo-elements (`li::before`) allow icons or emojis; remember to add spacing and color.
- Use `display: flex` or `grid` to transform lists into nav bars or columns while keeping accessible markup.

## Real-World Scenario

- A features list gets lost in a landing page. By replacing default bullets with checkmarks and spacing items with flexbox, marketing highlights benefits while screen readers still announce the list structure.

## Examples

```css
ul.features {
  list-style: none;
  padding: 0;
}

ul.features li::before {
  content: '✔';
  color: #16a34a;
  margin-right: 0.5rem;
}

.nav {
  display: flex;
  gap: 1.5rem;
}
```

## Follow-up

- [ ] Build a breadcrumb trail using ordered lists and pseudo-elements.
- [ ] Create responsive nav lists that collapse into vertical stacks on smaller screens.
- [ ] Test list modifications with screen readers to ensure marker changes remain understandable.
---
title: Styling Lists
status: draft
last_reviewed: 09-11-2025
---

