---
title: Installation & Tooling
status: draft
last_reviewed: 09-11-2025
---

# Installation & Tooling

Tailwind installs through npm and integrates with build tools to process directives and purge unused classes.

## Install Steps

```bash
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
```

- Generates `tailwind.config.js` and `postcss.config.js`.
- Use `npx tailwindcss init --full` to scaffold a verbose config for reference.

## Entry Stylesheet

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

- Place directives in a CSS file imported by your bundler (Vite, Next, Remix).

## Scripts

- Add `tailwindcss -i ./src/input.css -o ./dist/output.css --watch` for vanilla setups.
- When using frameworks, rely on their dev servers; ensure Tailwind’s content paths match.

## Real-World Scenario

- A team integrates Tailwind into a Vite project. Running `npx tailwindcss init -p` seeds the config, and updating `content: ['./index.html', './src/**/*.{js,ts,jsx,tsx}']` ensures unused classes purge correctly in production.

## Follow-up

- [ ] Spin up a minimal Vite project and confirm Tailwind builds utilities.
- [ ] Configure VS Code IntelliSense (`tailwindcss` extension) for class hints and previews.
- [ ] Double-check `content` paths so purge tooling catches your templates.

## Practice

- Spin up a minimal Vite project and confirm Tailwind builds utilities.
- Configure VS Code IntelliSense (`tailwindcss` extension) for class hints and previews.
