---
title: Forms Plugin
status: draft
last_reviewed: 09-11-2025
---

# Forms Plugin

## Why It Matters

- `@tailwindcss/forms` normalizes form controls and provides sensible defaults.

## Core Ideas

- Install with `npm install -D @tailwindcss/forms` and add to `plugins` in `tailwind.config.js`.
- Base classes (`form-input`, `form-textarea`, `form-select`, `form-checkbox`, `form-radio`) align padding, borders, and focus outlines.
- Customize via `@layer components` or theme tokens (colors, shadows) to match brand.

## Real-World Scenario

- A registration form looked inconsistent across browsers. Enabling the forms plugin and tweaking focus colors delivered a consistent, accessible experience.

## Follow-up

- [ ] Style a form using the plugin and add custom focus ring utilities.
- [ ] Compare native browser UI vs. plugin styling across platforms.
- [ ] Document overrides so designers know how forms are themed.
