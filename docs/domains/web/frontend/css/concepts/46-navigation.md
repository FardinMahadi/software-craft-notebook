---
title: Navigation Patterns
status: draft
last_reviewed: 09-11-2025
---

# Navigation Patterns

## Why It Matters

- Navigation bars guide users through products; styling affects clarity and accessibility.

## Core Ideas

- Flexbox handles horizontal layouts with spacing (`gap`, `justify-content`); switch to column on small screens.
- Keep focus styles visible; add subtle hover indicators (underlines, background fills).
- Manage responsive states with classes that toggle `display`, `max-height`, or transforms.

## Real-World Scenario

- A SaaS app uses flexbox for a desktop nav and collapses to a hamburger menu on mobile. Focus outlines remain visible so keyboard users can navigate the menu.

## Examples

```css
.nav {
  display: flex;
  gap: 1.5rem;
  align-items: center;
}

.nav a {
  padding: 0.5rem 0;
  position: relative;
}

.nav a::after {
  content: '';
  position: absolute;
  inset-inline: 0;
  bottom: -0.25rem;
  height: 2px;
  background: currentColor;
  transform: scaleX(0);
  transition: transform 200ms ease;
}

.nav a:hover::after,
.nav a:focus-visible::after,
.nav a[aria-current='page']::after {
  transform: scaleX(1);
}
```

## Follow-up

- [ ] Build a responsive navigation bar that swaps to a hamburger menu on narrow screens.
- [ ] Ensure focus management and `aria-expanded` states update correctly when toggling menus.
- [ ] Document navigation variants (horizontal, vertical, dropdown) for reuse.
