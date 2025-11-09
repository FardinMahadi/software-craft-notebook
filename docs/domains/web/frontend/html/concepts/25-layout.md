# HTML Page Layout

## Why It Matters

- Semantic sections help users and assistive tech navigate large pages quickly.
- Clear layout structure makes CSS and JavaScript easier to maintain.
- Consistent landmarks support SEO and enable skip-link shortcuts.

## Core Ideas

- Use structural elements for meaning: `<header>`, `<nav>`, `<main>` (once per page), `<section>`, `<article>`, `<aside>`, `<footer>`.
- Nest sections logically and maintain heading hierarchy to reflect the outline.
- Pair semantic structure with CSS layout systems (Flexbox, Grid) for responsive designs.
- Use `<div>` internally only when no semantic element fits.

## Real-World Scenario

- A learning platform builds a dashboard with global navigation, main content, and a resources sidebar. Semantic landmarks let screen-reader users jump straight to “Main” or “Quick Links,” while designers manipulate layout with CSS grid without altering HTML structure.

## Examples

```html
<header>
  <h1>Learning Dashboard</h1>
  <nav aria-label="Primary">
    <a href="#modules">Modules</a>
    <a href="#notes">Notes</a>
  </nav>
</header>
<main id="modules">
  <section>
    <h2>Current Focus</h2>
    <p>HTML fundamentals and layout drills.</p>
  </section>
</main>
<aside aria-label="Quick links">
  <h2>Quick Links</h2>
  <ul>
    <li><a href="/resources">Resources</a></li>
    <li><a href="/schedule">Schedule</a></li>
  </ul>
</aside>
<footer>&copy; 2025 Study Lab</footer>
```

## Follow-up

- [ ] Sketch a page wireframe, map each area to semantic elements, then implement the structure in HTML.
- [ ] Apply Flexbox or Grid to achieve responsive columns while keeping landmarks intact.
- [ ] Add skip links (`<a href="#main">Skip to main content</a>`) and verify they work with keyboard navigation.
---
title: HTML Page Layout
status: draft
last_reviewed: 09-11-2025
---

