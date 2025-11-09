---
title: Arbitrary Values & Modifiers
status: draft
last_reviewed: 09-11-2025
---

# Arbitrary Values & Modifiers

## Why It Matters

- Arbitrary values and modifiers handle edge cases beyond the Tailwind theme.

## Core Ideas

- Arbitrary values: `class="[property:value]"` or `utility-[value]` (e.g., `bg-[radial-gradient(circle,_var(--tw-gradient-stops))]`, `p-[3.75rem]`).
- Modifiers: `!` for important (`!mt-0`), state modifiers (`checked:bg-indigo-600`, `placeholder:text-slate-400`), directional variants (`rtl:space-x-reverse`).
- Document custom values so teammates know why they exist.

## Real-World Scenario

- A marketing hero needs a custom gradient start point. Using `bg-[radial-gradient(...)]` solves it without writing manual CSS, and the decision is noted for future designers.

## Follow-up

- [ ] Implement a gradient or spacing value outside Tailwind’s presets using arbitrary values.
- [ ] Use important modifiers sparingly to override third-party styles.
- [ ] Review arbitrary usage quarterly to consolidate into theme tokens where possible.
