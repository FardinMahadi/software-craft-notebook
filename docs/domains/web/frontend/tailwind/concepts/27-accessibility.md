---
title: Accessibility with Tailwind
status: draft
last_reviewed: 09-11-2025
---

# Accessibility with Tailwind

## Why It Matters

- Tailwind utilities support inclusive interfaces when paired with semantic markup.

## Core Ideas

- Maintain visible focus outlines (`focus-visible:outline`, `focus-visible:ring`).
- Use ARIA/data variants to reflect state changes (`aria-pressed:bg-indigo-600`, `data-[state=open]:bg-slate-800`).
- Provide screen-reader helpers (`sr-only`, `not-sr-only`) and ensure color contrast meets guidelines.
- Use `motion-safe:` / `motion-reduce:` to respect user animation preferences.

## Real-World Scenario

- An alert component uses `role="alert"`, `aria-live`, and Tailwind variants to differentiate success/warning/error while keeping text accessible.

## Follow-up

- [ ] Audit components to confirm focus management works across inputs.
- [ ] Build an accessible alert using `role` attributes and variant-driven styles.
- [ ] Review color contrast and motion preferences during design reviews.
