# Applying CSS

## Why It Matters

- Knowing how to attach CSS helps you choose the right strategy for maintainability and performance.
- Separating concerns keeps markup clean while still allowing quick overrides when needed.

## Core Ideas

- **External stylesheets** (`<link rel="stylesheet">`) are preferred for caching, reuse, and separation of concerns.
- **Internal style blocks** (`<style>`) work for prototypes or page-specific overrides.
- **Inline styles** (`style=""`) carry the highest specificity; reserve them for dynamic or one-off adjustments (emails, script output).
- Order matters: later declarations override earlier ones when specificity ties.

## Real-World Scenario

- A product team migrates from inline styles to a shared stylesheet so branding changes roll out across marketing and app pages. Inline styles remain only for dynamically generated email templates.

## Examples

```html
<!-- External -->
<link rel="stylesheet" href="/css/app.css" />

<!-- Internal -->
<style>
  body {
    background: #f8fafc;
  }
</style>

<!-- Inline -->
<button style="background: #0f172a; color: white;">Save</button>
```

## Follow-up

- [ ] Refactor a page with inline styles into an external stylesheet.
- [ ] Use browser dev tools to inspect which source (inline, internal, external) is winning in the cascade.
- [ ] Document when your team should use inline styles (e.g., transactional emails) to avoid accidental sprawl.
---
title: Applying CSS
status: draft
last_reviewed: 09-11-2025
---

