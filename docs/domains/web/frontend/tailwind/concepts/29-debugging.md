---
title: Debugging Tailwind
status: draft
last_reviewed: 09-11-2025
---

# Debugging Tailwind

## Why It Matters

- Tailwind’s utility approach is straightforward, but misconfigurations can hide styles or bloat CSS.

## Core Ideas

- Common issues: misspelled utilities, missing `content` paths, conflicting class order.
- Use dev tools to inspect compiled classes; Tailwind utilities map directly to CSS rules.
- Employ helpers (`tailwind-merge`, `clsx`) to resolve class order conflicts.
- Add temporary debug utilities (`border border-red-500`) or custom variants to highlight breakpoints.

## Real-World Scenario

- A missing `content` glob caused button hover states to disappear in production. Inspecting compiled CSS revealed purge removed the classes, leading to a quick fix.

## Follow-up

- [ ] Diagnose a missing style by verifying the class exists in the compiled CSS.
- [ ] Configure `tailwind-merge` to avoid duplicate spacing utilities.
- [ ] Create debug utilities or variants to surface layout boundaries during development.
