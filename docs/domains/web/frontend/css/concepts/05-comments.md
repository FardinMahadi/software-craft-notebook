# CSS Comments

## Why It Matters

- Comments capture intent, making large stylesheets easier to navigate.
- Marking sections or TODOs speeds up collaboration during reviews.
- Commenting out declarations helps experiment safely without deleting code.

## Core Ideas

- Syntax: wrap text between `/*` and `*/`; comments can span multiple lines but cannot nest.
- Use comments to outline sections (base, layout, components) or document tricky decisions.
- Remove outdated comments to avoid confusion and keep stylesheets clean.

## Real-World Scenario

- A design systems team tags breakpoint overrides with comments, so engineers know why certain `@media` rules exist. During refactors, they quickly confirm whether the change is still required.

## Examples

```css
/* Base styles */
body {
  color: #1f2937;
}

/* TODO: Remove once dark mode launches */
.header {
  background-color: #0f172a;
}
```

## Follow-up

- [ ] Add comments to a stylesheet to mark sections (base, layout, utilities).
- [ ] Comment out a declaration to compare visual differences, then re-enable it.
- [ ] Review your codebase and delete obsolete comments or replace them with documentation.
---
title: CSS Comments
status: draft
last_reviewed: 09-11-2025
---

