---
title: Tailwind Directives
status: draft
last_reviewed: 09-11-2025
---

# Tailwind Directives

Tailwind injects prebuilt styles through CSS directives compiled at build time.

## Core Directives

- `@tailwind base;` – resets and base typography.
- `@tailwind components;` – component classes like `container`.
- `@tailwind utilities;` – the utility class set.

## Layering Custom CSS

```css
@tailwind base;
@tailwind components;
@tailwind utilities;

@layer components {
  .badge {
    @apply inline-flex items-center gap-2 rounded-full px-3 py-1 text-sm;
  }
}
```

- Use `@layer` to inject custom rules into Tailwind’s ordering.

## Real-World Scenario

- A team creates shared component classes for badges and alerts inside `@layer components`, ensuring custom styles merge with Tailwind utilities without specificity issues.

## Follow-up

- [ ] Add a component layer snippet and verify it respects cascade ordering.
- [ ] Inspect compiled CSS to understand how directives expand into full styles.
- [ ] Document any custom layers so teammates know where to add overrides.

## Practice

- Add a component layer snippet and verify it respects cascade ordering.
- Inspect compiled CSS to understand how directives expand into full styles.
