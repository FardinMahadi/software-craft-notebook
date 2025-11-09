---
title: Spacing & Sizing
status: draft
last_reviewed: 09-11-2025
---

# Spacing & Sizing

## Why It Matters

- Tailwind’s spacing scale keeps padding, margins, and dimensions consistent across components.

## Core Ideas

- Margin utilities: `m-4`, `mx-auto`, `mt-6`; padding: `p-4`, `px-6`, `py-8`; gaps: `gap-4`, `space-y-4`.
- Sizing utilities: `w-64`, `w-full`, `h-screen`, plus min/max helpers (`min-w-[12rem]`, `max-h-96`).
- Aspect ratio utilities (`aspect-square`, `aspect-video`) maintain consistent media sizing.
- Arbitrary values (`mt-[3.75rem]`, `max-w-[72ch]`) solve edge cases—document them for consistency.

## Real-World Scenario

- A marketing layout spec defines exact spacing. By mapping values to Tailwind’s scale, the team avoids custom CSS and keeps future updates simple.

## Follow-up

- [ ] Recreate a layout spec using only spacing-scale utilities.
- [ ] Identify where arbitrary values are necessary and log them for future reuse.
- [ ] Review spacing usage periodically to keep designs aligned with the theme scale.
