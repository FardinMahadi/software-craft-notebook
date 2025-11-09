# HTML Favicons

## Why It Matters

- Favicons appear in browser tabs, bookmarks, and pinned shortcuts—tiny assets that reinforce brand identity.
- Multiple icon sizes keep graphics crisp across devices, including retina displays and mobile homescreens.
- Proper links prevent 404s or default globe icons that look unpolished.

## Core Ideas

- Provide a legacy `.ico` file plus modern PNG or SVG variants at different sizes (`16x16`, `32x32`, `48x48`).
- Use `<link rel="icon" href="/favicon-32x32.png" sizes="32x32" type="image/png">` and similar tags in `<head>`.
- Add `rel="apple-touch-icon"` for iOS tiles and `rel="manifest"` to connect the Web App Manifest.
- Store icons in predictable paths (site root or `/assets/`) so browsers find them automatically.

## Real-World Scenario

- A startup launches a new product and wants consistent branding in investor demos. After aligning assets, they generate favicon sizes, wire them into the `<head>`, and confirm mobile devices show polished icons when the app is saved to the home screen.

## Examples

```html
<link rel="icon" href="/favicon.ico" />
<link
  rel="icon"
  href="/favicon-32x32.png"
  sizes="32x32"
  type="image/png"
/>
<link
  rel="apple-touch-icon"
  href="/apple-touch-icon.png"
  sizes="180x180"
/>
<link rel="manifest" href="/site.webmanifest" />
```

## Follow-up

- [ ] Generate a favicon set using a tool like RealFaviconGenerator and integrate the markup.
- [ ] Inspect network requests to ensure all icon files return 200 status codes.
- [ ] Test pinned tabs or homescreen shortcuts on multiple devices to verify clarity.
---
title: HTML Favicon
status: draft
last_reviewed: 09-11-2025
---

