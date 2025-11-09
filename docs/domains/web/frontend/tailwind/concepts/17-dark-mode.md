---
title: Dark Mode Strategies
status: draft
last_reviewed: 09-11-2025
---

# Dark Mode Strategies

## Why It Matters

- Tailwind supports class-based or media-query dark modes, letting you adapt themes quickly.

## Core Ideas

- `darkMode: 'class'` (default) toggles a `.dark` class on `<html>` or `<body>`; `darkMode: 'media'` follows `prefers-color-scheme`.
- Prefix utilities with `dark:` (`bg-slate-100 dark:bg-slate-900`, `dark:prose-invert`).
- Toggle via JS (`document.documentElement.classList.toggle('dark')`) and persist in local storage.

## Real-World Scenario

- A dashboard needs user-controlled themes. Toggling the `.dark` class on `<html>` flips colors defined in `theme.extend.colors`, keeping both modes in sync.

## Follow-up

- [ ] Convert an existing page to support dark mode variants.
- [ ] Ensure light/dark palettes meet contrast guidelines using design tokens.
- [ ] Document where the `.dark` class is applied (html vs body) so team members stay consistent.

---
**Notes**
- Confirm Tailwind version for `darkMode` defaults and `prose-invert` support before using in production.
- Review official docs for token naming updates when extending color palettes for dark mode.
