---
title: Framework Integration
status: draft
last_reviewed: 09-11-2025
---

# Framework Integration

## Why It Matters

- Tailwind plugs into modern frameworks with minimal configuration.

## Core Ideas

- React/Vite: scaffold with `npm create vite@latest` and follow the Tailwind Vite guide; import styles in `main.jsx`.
- Next.js/Remix: use official templates (`npx create-next-app --tailwind`) and ensure `content` globs include `app/**` or `pages/**`.
- Laravel/Rails: use framework starters (`php artisan breeze:install`, `rails tailwindcss:install`) to configure PostCSS/autoprefixer.

## Real-World Scenario

- A team migrated UI to Next.js and used the Tailwind template. After adding `app/**` paths to `content`, server-rendered pages purged correctly, and hot reload worked out of the box.

## Follow-up

- [ ] Integrate Tailwind into a React/Vite app and confirm fast refresh keeps class edits.
- [ ] Evaluate SSR frameworks (Next, Remix) to ensure purge settings include server-rendered paths.
- [ ] Document framework-specific setup steps for the team.

---
**Notes**
- Confirm Tailwind guide updates for Remix/Laravel/Rails integrations; some scaffolds change commands between versions.
- Double-check `app` directory support in Next.js documentation when using the latest release.
