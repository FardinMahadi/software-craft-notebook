---
title: Lists & Navigation
status: draft
last_reviewed: 09-11-2025
---

## Why It Matters

- Lists organise content into scannable chunks and power navigation menus or step-by-step guides.
- Semantic lists help assistive tech announce structure properly.
- Using the right list type avoids accessibility retrofits later.

## Core Ideas

- Choose list type by meaning: ordered (`<ol>`), unordered (`<ul>`), or description (`<dl>` with `<dt>/<dd>`).
- Navigation menus belong inside `<nav>` and typically use `<ul>` + `<li>` regardless of horizontal or vertical layout.
- `type` and `start` attributes adjust numbering when the order conveys meaning.
- Breadcrumbs benefit from `aria-label="Breadcrumb"` and `aria-current="page"` on the active link.

## Real-World Scenario

- A SaaS dashboard features a vertical navigation menu and a step-by-step onboarding checklist. By structuring both as lists, the design team styles them flexibly, and screen-reader users hear “list of 5 items” before navigating—speeding onboarding.

## Examples

```html
<nav aria-label="Main">
  <ul class="nav">
    <li><a href="/overview" aria-current="page">Overview</a></li>
    <li><a href="/docs">Docs</a></li>
    <li><a href="/pricing">Pricing</a></li>
  </ul>
</nav>

<ol class="setup-steps">
  <li>Create your workspace</li>
  <li>Invite teammates</li>
  <li>Upload your first project</li>
</ol>
```

## Follow-up

- [ ] Convert a navigation bar into semantic `<nav>` + `<ul>/<li>` markup and style with CSS.
- [ ] Build a description list for glossary terms and ensure screen readers announce definitions correctly.
- [ ] Document an accessible pattern for multi-level navigation, including keyboard interactions.
