---
title: Configuration Structure
status: draft
last_reviewed: 09-11-2025
---

# Configuration Structure

`tailwind.config.js` controls scanning, theming, plugins, and future-proof options.

## Key Sections

- `content`: glob patterns to scan for class usage.
- `theme`: default tokens and `extend` for custom values.
- `plugins`: official or community extensions.
- `future` / `experimental`: opt into upcoming features.

## Example

```js
module.exports = {
  content: ["./index.html", "./src/**/*.{js,ts,jsx,tsx}"],
  theme: {
    extend: {
      colors: {
        brand: {
          DEFAULT: "#2563EB",
          dark: "#1D4ED8",
        },
      },
    },
  },
  plugins: [],
};
```

## Real-World Scenario

- A project adds `./src/**/*.mdx` to `content` so documentation pages purge correctly. They extend theme colors under `brand` to map marketing tokens, keeping design language consistent across components.

## Follow-up

- [ ] Audit content globs to ensure they cover pages, layouts, component directories, and MDX files if used.
- [ ] Use `npx tailwindcss init --full` to explore defaults, then cherry-pick tokens to extend.
- [ ] Document plugin choices and why they’re included (forms, typography, aspect-ratio, etc.).

## Practice

- Audit content globs to ensure they cover pages, layouts, and component directories.
- Use `npx tailwindcss init --full` to explore defaults, then cherry-pick tokens to extend.
