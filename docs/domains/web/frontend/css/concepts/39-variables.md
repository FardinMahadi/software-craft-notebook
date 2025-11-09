---
title: CSS Custom Properties
status: draft
last_reviewed: 09-11-2025
---

# CSS Custom Properties

## Why It Matters

- Custom properties (CSS variables) store reusable values and make theming easier.
- Variables inherit, so updating them in one place cascades through components.

## Core Ideas

```css
:root {
  --spacing-4: 1rem;
  --color-accent: hsl(198deg 93% 60%);
}

.cta {
  padding: var(--spacing-4);
  background: var(--color-accent);
}
```

- Define variables on `:root` for global scope; override within components for variations.
- Use `var(--name, fallback)` to provide defaults.
- Toggle themes by redefining variables (e.g., in `[data-theme="dark"]`).

## Real-World Scenario

- A design system stores brand colors and spacing in `:root`. Switching to dark mode updates only the variable values, so all components adjust instantly.

## Follow-up

- [ ] Create a theme switcher that toggles color variables.
- [ ] Use spacing variables to maintain consistent rhythm across components.
- [ ] Update variables via JavaScript with `element.style.setProperty('--color-accent', '#1d4ed8');`.
