---
title: Content Scanning
status: draft
last_reviewed: 09-11-2025
---

# Content Scanning

## Why It Matters

- Tailwind removes unused utilities based on the files you list. Accurate scanning keeps bundles lean.

## Core Ideas

- Configure `content` with every file that renders markup: `.html`, `.jsx`, `.tsx`, `.vue`, `.mdx`, Rails views, etc.
- Safelist dynamic class names (e.g., status badges) when generating them programmatically.
- Tailwind 3 runs in JIT mode; `--watch` recompiles utilities as files change.

## Real-World Scenario

- A team updated their templates to use `.mdx` but forgot to add the extension to `content`. Production builds stripped required classes, breaking docs styling until the glob patterns were fixed.

## Follow-up

- [ ] Audit `content` globs to ensure they cover all template locations.
- [ ] Add safelist entries for dynamic classes produced from data.
- [ ] Trigger a build, inspect output size, and remove unnecessary directories from scanning.

---

**Notes**

- Confirm Tailwind version (>=3.4) for examples that rely on latest features.
- Review official docs for `color-mix` and viewport unit variants (svh/lvh/dvh) to ensure browser support guidance stays accurate.
