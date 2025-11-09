---
title: State & Interaction Variants
status: draft
last_reviewed: 09-11-2025
---

# State & Interaction Variants

## Why It Matters

- Tailwind variants style interactive states, ARIA attributes, and media conditions directly in markup.

## Core Ideas

- Pseudo-class variants: `hover:`, `focus:`, `focus-visible:`, `active:`, `disabled:`, `visited:`.
- Group/peer variants: `group-hover:`, `group-focus:`, `peer-checked:` enable child/sibling reactions.
- ARIA/data variants: `aria-expanded:`, `aria-selected:`, `data-[state=open]:bg-slate-800`.
- Media variants: `motion-safe:`, `motion-reduce:`, `portrait:`, `dark:`.

## Real-World Scenario

- An accordion uses `peer` on a hidden checkbox to toggle answer visibility with `peer-checked:max-h-40` while respecting `motion-reduce` for transitions.

## Follow-up

- [ ] Implement a collapsible panel using `peer` to toggle child states.
- [ ] Use `group` to change child styles when a parent card is hovered or focused.
- [ ] Audit ARIA variants to ensure interactive components remain accessible.
