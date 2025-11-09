---
title: Theme Extension
status: draft
last_reviewed: 09-11-2025
---

# Theme Extension

## Why It Matters

- Extending Tailwind tokens keeps design systems consistent without rewriting core scales.

## Core Ideas

- Use `theme.extend` to add colors, spacing, fonts, and more while preserving defaults.
- Align naming with product design tokens (`surface-muted`, `brand-accent`).
- Mirror CSS custom properties when mixing Tailwind with plain CSS.

## Real-World Scenario

- Marketing defined brand shades outside Tailwind’s defaults. Extending `colors.brand` let developers use `bg-brand` utilities across the app without custom CSS.

## Examples

```js
theme: {
  extend: {
    colors: {
      surface: {
        DEFAULT: '#0F172A',
        muted: '#1E293B',
      },
    },
    spacing: {
      18: '4.5rem',
    },
    fontFamily: {
      display: ['"Inter var"', 'system-ui', 'sans-serif'],
    },
  },
},
```

## Follow-up

- [ ] Document a color palette in `theme.extend.colors` and test generated utilities.
- [ ] Create spacing scales that match design guidelines and apply them across components.
- [ ] Review extended tokens regularly to avoid unused or inconsistent values.
