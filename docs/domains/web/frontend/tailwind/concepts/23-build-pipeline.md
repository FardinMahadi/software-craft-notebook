---
title: Build Pipeline & CLI
status: draft
last_reviewed: 09-11-2025
---

# Build Pipeline & CLI

## Why It Matters

- Tailwind’s CLI and PostCSS integrations build and purge utilities for production-ready CSS.

## Core Ideas

- CLI: `npx tailwindcss -i ./src/styles.css -o ./dist/tailwind.css --minify --watch` for dev/prod workflows.
- PostCSS: include `tailwindcss` and `autoprefixer` in `postcss.config.js`; works with Vite, Next.js, Remix, Astro, etc.
- Production builds rely on accurate `content` paths and `NODE_ENV=production` to purge unused classes.

## Real-World Scenario

- A team integrated Tailwind into an Astro project. Running the CLI in watch mode during dev and minified builds for production kept CSS under 40KB gzip.

## Follow-up

- [ ] Run the CLI build, analyze output size, and verify only used utilities remain.
- [ ] Integrate Tailwind into an existing PostCSS pipeline and confirm hot reload works.
- [ ] Document build scripts (dev, prod) so teammates can reproduce builds reliably.
