---
title: Performance & Bundle Size
status: draft
last_reviewed: 09-11-2025
---

# Performance & Bundle Size

## Why It Matters

- Accurate purging and disciplined utility usage keep Tailwind bundles lean.

## Core Ideas

- Ensure `content` globs include all template paths; safelist only necessary classes.
- Extract repeated utility stacks to helpers or components to avoid duplication.
- Run CLI builds (`npx tailwindcss -i input.css -o output.css --minify`) and monitor size; include CSS reports in CI.

## Real-World Scenario

- After auditing safelists and content globs, a SaaS app cut CSS output from 120KB to 45KB gzip, improving largest contentful paint.

## Follow-up

- [ ] Introduce a bundle size gate in CI and fail builds that exceed thresholds.
- [ ] Compare before/after CSS size when removing unused safelist patterns.
- [ ] Review utility usage quarterly to consolidate tokens and avoid arbitrary values.
