# Responsive HTML

## Why It Matters

- Visitors use phones, tablets, laptops, and big displays; responsive layouts keep experiences consistent.
- Proper viewport settings and flexible containers prevent zooming or horizontal scroll.
- Responsive assets protect performance by serving the right size at the right time.

## Core Ideas

- Include `<meta name="viewport" content="width=device-width, initial-scale=1">` in `<head>` to match the device width.
- Build fluid layouts with percentages, flexbox, or grid; reserve fixed widths for small elements like icons.
- Use media queries (`@media`) or container queries to adjust layout, typography, and spacing at breakpoints.
- Serve responsive images (`srcset`, `sizes`, `<picture>`) and lazy-load noncritical embeds.

## Real-World Scenario

- A blog launches with readers on both phones and desktops. With a responsive grid, the sidebar moves below the article on small screens, while images load lightweight mobile variants. Engagement improves because content stays readable without pinching or waiting on large downloads.

## Examples

```html
<head>
  <meta name="viewport" content="width=device-width, initial-scale=1" />
</head>

<main class="layout">
  <article>...</article>
  <aside>...</aside>
</main>

<style>
  .layout {
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
  }

  @media (min-width: 48rem) {
    .layout {
      flex-direction: row;
      align-items: flex-start;
    }
    .layout > article {
      flex: 2;
    }
    .layout > aside {
      flex: 1;
    }
  }
</style>
```

## Follow-up

- [ ] Build a layout that stacks on small screens and becomes multi-column on tablets/desktops.
- [ ] Test responsiveness in browser device emulators and, if possible, real hardware.
- [ ] Configure responsive image sources and verify the correct asset loads at different viewport widths.
---
title: Responsive HTML
status: draft
last_reviewed: 09-11-2025
---

