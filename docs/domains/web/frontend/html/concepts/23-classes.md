---
title: HTML Classes
status: draft
last_reviewed: 09-11-2025
---

# HTML Classes

## Why It Matters

- Classes create reusable styling and scripting hooks across multiple elements.
- Consistent naming keeps CSS manageable and reduces duplication.
- JavaScript relies on class names to toggle states (e.g., open/closed menus).

## Core Ideas

- Declare classes in the `class` attribute: `<div class="card lead-story">`.
- Elements can have multiple classes separated by spaces; order doesn’t change specificity.
- CSS targets classes with `.class-name`, while JavaScript uses `querySelector('.class-name')`.
- Adopt a naming convention (kebab-case, BEM, utility classes) to communicate intent.

## Real-World Scenario

- A content team reuses a “call-to-action” pattern across pages. By sharing a `.cta-button` class, designers tweak style once and see updates everywhere. Developers toggle `.is-loading` on the same button to show a spinner during API calls.

## Examples

```html
<a class="cta-button is-loading" href="/signup">
  Join now
</a>

<style>
  .cta-button {
    display: inline-block;
    padding: 0.75rem 1.5rem;
    background: #2563eb;
    color: white;
    border-radius: 0.75rem;
    text-decoration: none;
  }

  .cta-button.is-loading {
    opacity: 0.7;
    pointer-events: none;
  }
</style>

<script>
  const button = document.querySelector('.cta-button');
  button.classList.remove('is-loading');
</script>
```

## Follow-up

- [ ] Audit a page and align class names to your chosen convention.
- [ ] Reuse a single class across multiple components to confirm styles stay DRY.
- [ ] Use `classList` methods (`add`, `remove`, `toggle`) to manage state transitions in JavaScript.
