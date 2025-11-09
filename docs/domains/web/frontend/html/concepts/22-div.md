---
title: Using `<div>` Containers
status: draft
last_reviewed: 09-11-2025
---

# `<div>` Containers

## Why It Matters

- `<div>` provides a flexible container when no semantic element fits.
- Proper use keeps markup organized while leaving room for CSS layout hooks.
- Overusing `<div>` without context leads to “div soup,” making maintenance difficult.

## Core Ideas

- `<div>` is block-level and carries no semantic meaning—pair it with `class` or `id` to describe purpose.
- Reach for semantic tags (`<section>`, `<article>`, `<nav>`) first; fall back to `<div>` when content doesn’t match a specific element.
- Group related elements (e.g., card bodies, grid columns) to apply shared styles or JavaScript behavior.

## Real-World Scenario

- A dashboard displays multiple info cards. Designers wrap each card in `<div class="card">` so they can apply shadows and padding uniformly, while still using semantic elements (`<h2>`, `<p>`, `<ul>`) inside for content structure.

## Examples

```html
<div class="card">
  <h2>Daily Highlights</h2>
  <p>Summaries from the latest study session.</p>
</div>

<div class="layout-grid">
  <div class="column">
    <h3>Modules</h3>
    <!-- content -->
  </div>
  <div class="column">
    <h3>Labs</h3>
  </div>
</div>
```

## Follow-up

- [ ] Refactor a page to replace unnecessary `<div>` usage with semantic elements.
- [ ] Create a responsive grid by wrapping items in `<div>` containers and applying flex or grid utility classes.
- [ ] Document naming conventions for container classes (`card`, `section`, etc.) to keep styling consistent.
