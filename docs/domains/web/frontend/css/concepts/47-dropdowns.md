---
title: Dropdown Menus
status: draft
last_reviewed: 09-11-2025
---

# Dropdown Menus

## Why It Matters

- Dropdowns reveal secondary navigation or actions without crowding the UI.

## Core Ideas

- Use a positioned container (`position: relative`) and absolute submenu.
- Toggle visibility via `:focus-within`, `:hover`, or a JavaScript class while keeping focus states clear.
- Provide accessible buttons (`aria-expanded`, `aria-controls`) and respect reduced-motion when animating.

## Real-World Scenario

- A product dashboard shows quick filters in a dropdown. Keyboard users open it with a button, arrow key through options, and close it with Escape, all guided by visible focus rings.

## Examples

```css
.dropdown {
  position: relative;
}

.dropdown-menu {
  position: absolute;
  inset-inline-start: 0;
  top: 100%;
  min-width: 12rem;
  padding: 0.5rem;
  border-radius: 0.75rem;
  background: white;
  box-shadow: 0 16px 32px rgb(15 23 42 / 0.15);
  visibility: hidden;
  opacity: 0;
  transform: translateY(0.5rem);
  transition: opacity 150ms ease, transform 150ms ease;
}

.dropdown:focus-within .dropdown-menu,
.dropdown:hover .dropdown-menu {
  visibility: visible;
  opacity: 1;
  transform: translateY(0);
}
```

## Follow-up

- [ ] Implement a dropdown that opens on hover for desktop and focus for keyboard users.
- [ ] Add CSS transitions for smooth reveal/hide while respecting reduced-motion preferences.
- [ ] Ensure focus trapping and Escape key behavior if you enhance with JavaScript.
