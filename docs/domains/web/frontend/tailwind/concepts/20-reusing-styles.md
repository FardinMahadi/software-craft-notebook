---
title: Reusing Styles
status: draft
last_reviewed: 09-11-2025
---

# Reusing Styles

## Why It Matters

- Tailwind promotes composition, but larger apps benefit from reusable patterns.

## Core Ideas

- Use `@apply` inside `@layer components` to bundle repeated utilities (keep usage limited to avoid bloating compiled CSS).
- Build framework components that encapsulate utility stacks; helper libraries like `clsx` or `cva` manage conditional classes.
- Author plugins or semantic utilities when tokens repeat across the product.

## Real-World Scenario

- A design system exposes `Button` and `Badge` components that wrap Tailwind utilities, while shared variants come from a `cva` helper to keep prop-driven styling consistent.

## Follow-up

- [ ] Refactor a repeated button utility stack into `@apply` and compare compiled output size.
- [ ] Build a variants helper using `class-variance-authority` for prop-driven styling.
- [ ] Document reuse patterns (apply, components, plugins) for the team.
