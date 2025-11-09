---
title: Testing & Maintenance
status: draft
last_reviewed: 09-11-2025
---

# Testing & Maintenance

## Why It Matters

- Keeping Tailwind projects healthy requires linting, visual regression tests, and mindful upgrades.

## Core Ideas

- Use Prettier + Tailwind plugin to sort class names; add ESLint rules for unknown classes.
- Employ visual regression tooling (Chromatic, Playwright, Loki) across themes and breakpoints.
- Track Tailwind releases; `npx @tailwindcss/upgrade` can assist major upgrades.

## Real-World Scenario

- A component library added Prettier sorting and Playwright screenshots for hero variants. During a Tailwind upgrade, the upgrade tool flagged breaking changes, and visual tests caught a spacing regression.

## Follow-up

- [ ] Add Prettier Tailwind sorting to the project and run it against a large component file.
- [ ] Create visual regression tests for a component with multiple variants.
- [ ] Monitor Tailwind release notes and schedule upgrade windows.
