# Head & Metadata

## Why It Matters

- The `<head>` element communicates essential metadata to browsers, search engines, and social platforms.
- Solid defaults improve rendering, discoverability, and link previews.
- Managing head content centrally prevents regressions when new pages launch.

## Core Ideas

- Always include `<meta charset="utf-8">` and `<meta name="viewport" content="width=device-width, initial-scale=1">`.
- Provide descriptive `<title>` and `<meta name="description">` for SEO and tab clarity.
- Add favicons and touch icons (`<link rel="icon">`, `<link rel="apple-touch-icon">`) in multiple sizes.
- Configure Open Graph (`og:title`, `og:description`, `og:image`) and Twitter Card tags for share previews.
- Link canonical URLs to avoid duplicate content penalties.
- Preload critical assets (fonts, hero images) cautiously to balance performance.

## Real-World Scenario

- A marketing team schedules a product launch. By preparing the `<head>` metadata—favicon set, OG image, accurate description—they ensure social previews look polished and search snippets update quickly when the page goes live.

## Examples

```html
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Product Dashboard</title>
  <meta
    name="description"
    content="Monitor product metrics with real-time insights."
  />
  <link rel="canonical" href="https://example.com/dashboard" />
  <meta property="og:title" content="Product Dashboard" />
  <meta
    property="og:description"
    content="Monitor product metrics in real time."
  />
  <meta property="og:image" content="https://example.com/og-dashboard.png" />
  <meta name="twitter:card" content="summary_large_image" />
  <link rel="icon" href="/favicon.ico" sizes="any" />
</head>
```

## Follow-up

- [ ] Automate common metadata via templates or layout components.
- [ ] Maintain a checklist for share images, canonical URLs, and analytics tags per page.
- [ ] Audit existing pages to confirm metadata accuracy and remove stale tags.
---
title: Head & Metadata
status: draft
last_reviewed: 09-11-2025
---

