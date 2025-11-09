# Styling Links

## Why It Matters

- Clear link states guide users and support keyboard navigation.
- Consistent styling builds trust and prevents missed calls to action.

## Core Ideas

- Follow LVFHA order (`:link`, `:visited`, `:focus`, `:hover`, `:active`) to avoid specificity surprises.
- Maintain visible focus styles (use `:focus-visible`) and differentiate hovered/active states.
- Underlines are the clearest affordance; only remove them if you provide an equally obvious cue.
- Distinguish visited links subtly so users track where they’ve been.

## Real-World Scenario

- A knowledge base receives feedback that links are hard to spot. By reinforcing underlines, tweaking hover colors, and adding focus outlines, the team reduces support tickets from keyboard and screen reader users.

## Examples

```css
a {
  color: #2563eb;
  text-decoration: underline;
  text-decoration-thickness: 0.1em;
}

a:hover,
a:focus-visible {
  color: #1d4ed8;
  text-decoration-style: wavy;
}
```

## Follow-up

- [ ] Create a link style guide documenting colors, hover effects, and focus outlines.
- [ ] Implement `:focus-visible` to differentiate keyboard vs pointer focus handling.
- [ ] Review visited link styling to ensure it remains accessible and on-brand.
---
title: Styling Links
status: draft
last_reviewed: 09-11-2025
---

