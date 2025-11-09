---
title: Selector Combinators
status: draft
last_reviewed: 09-11-2025
---

# Selector Combinators

## Why It Matters

- Combinators let you target elements based on their relationship without sprinkling extra classes everywhere.
- They keep styles focused and reduce duplication when designing nested components.

## Core Ideas

- **Descendant** (`.card p`) selects any matching descendant inside `.card`.
- **Child** (`.card > p`) targets only direct children, avoiding deeper nesting.
- **Adjacent sibling** (`.card + .card`) styles the immediate sibling that follows.
- **General sibling** (`.card ~ .card`) affects all matching siblings that come after.
- Keep selectors shallow and readable to avoid brittle cascades.

## Real-World Scenario

- A pricing page adds vertical spacing between consecutive `.plan` cards using `.plan + .plan { margin-top: 2rem; }` so teams don’t wrap each pair in an extra container.

## Examples

```css
.card > h3 {
  margin-bottom: 0.5rem;
}

.card + .card {
  margin-top: 1.5rem;
}

.alert ~ .alert {
  border-top: 1px solid rgb(226 232 240);
}
```

## Follow-up

- [ ] Style the first paragraph inside each `section` differently using a child combinator.
- [ ] Add top margins only when two `.card` components are adjacent.
- [ ] Review long selectors and simplify any overly deep combinators.

