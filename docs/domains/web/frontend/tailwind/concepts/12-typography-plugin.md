---
title: Typography Plugin
status: draft
last_reviewed: 09-11-2025
---

# Typography Plugin

## Why It Matters

- The official `@tailwindcss/typography` plugin (aka `prose`) styles long-form content with minimal effort.

## Core Ideas

- Install via `npm install -D @tailwindcss/typography` and add to `plugins` in `tailwind.config.js`.
- Wrap rich text in `prose` classes (`prose`, `prose-slate`, `prose-lg`, `prose-invert`).
- Customize defaults by extending `theme.typography` for headings, links, etc.

## Real-World Scenario

- Documentation pages use `prose` for articles. When the brand palette shifts, updating `--tw-prose-body` and heading styles keeps markdown content on-brand without touching HTML.

## Examples

```js
// tailwind.config.js
plugins: [require('@tailwindcss/typography')],

typography: ({ theme }) => ({
  DEFAULT: {
    css: {
      '--tw-prose-body': theme('colors.slate.200'),
    },
  },
}),
```

## Follow-up

- [ ] Apply the typography plugin to documentation and tweak heading sizes.
- [ ] Combine `prose` with utilities like `prose-headings:font-semibold` for finer control.
- [ ] Audit dark mode variants using `prose-invert` to maintain readability.
