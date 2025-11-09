# Pseudo-Classes

## Why It Matters

- Pseudo-classes let you style elements based on state (hovered, focused, first child, etc.) without extra markup.
- They power interactive feedback, alternating layouts, and form validation cues.

## Core Ideas

- Interaction states: `:hover`, `:focus`, `:focus-visible`, `:active`; combine with transitions for smooth feedback.
- Structural selectors: `:first-child`, `:last-child`, `:nth-child(odd)`, `:nth-of-type(2n)` for alternating styles.
- Form states: `:required`, `:valid`, `:invalid`, `:disabled` to reflect validation and availability.
- Pseudo-classes chain easily (`button.primary:hover:enabled`) for precise behavior.

## Real-World Scenario

- A signup form highlights invalid fields using `input:invalid` and provides clear focus outlines via `:focus-visible`, helping users correct mistakes quickly.

## Examples

```css
button:hover,
button:focus-visible {
  background-color: #1d4ed8;
  transition: background-color 150ms ease;
}

tbody tr:nth-child(even) {
  background: rgb(226 232 240 / 0.5);
}

input:invalid {
  border-color: #f87171;
}
```

## Follow-up

- [ ] Add hover and focus-visible states to buttons with accessible contrast.
- [ ] Use `:nth-child` to create zebra stripes without extra classes.
- [ ] Style form inputs based on `:invalid` and `:valid` to surface validation feedback.
---
title: Pseudo-Classes
status: draft
last_reviewed: 09-11-2025
---

