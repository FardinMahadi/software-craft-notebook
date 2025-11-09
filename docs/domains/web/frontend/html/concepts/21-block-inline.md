# Block vs Inline Elements

## Why It Matters

- Knowing default display behavior helps you control layout and spacing confidently.
- Choosing the right element reduces CSS overrides and improves semantic clarity.
- Understanding inline vs block is foundational before moving to flexbox or grid.

## Core Ideas

- **Block elements** start on a new line, take full width by default, and accept width/height/margins. Examples: `<div>`, `<section>`, `<article>`, `<header>`, `<main>`, `<footer>`, `<p>`, `<ul>`, `<li>`.
- **Inline elements** flow within text, ignore width/height settings, and respect horizontal padding. Examples: `<span>`, `<a>`, `<strong>`, `<em>`, `<code>`, `<img>`.
- **Inline-block** combines inline flow with the ability to set width/height—useful for pills, badges, or nav items.
- CSS `display` can change an element’s default behavior (`display: inline-block`, `display: block`), but start with semantic defaults.

## Real-World Scenario

- A marketing site uses inline links within paragraphs but needs a row of evenly sized CTA buttons. Converting anchors to `display: inline-block` keeps them on one line while allowing consistent padding and width. Later, the team upgrades to flexbox knowing the basics already.

## Examples

```html
<p>
  Stay informed with our <a href="/newsletter">weekly newsletter</a>.
</p>

<a class="cta" href="/signup">Get Started</a>

<style>
  .cta {
    display: inline-block;
    padding: 0.75rem 1.5rem;
    background: #2563eb;
    color: white;
    border-radius: 999px;
    text-decoration: none;
  }
</style>
```

| Property             | Block             | Inline              | Inline-block  |
| -------------------- | ----------------- | ------------------- | ------------- |
| Starts new line      | Yes               | No                  | No            |
| Width default        | 100% of container | Content width       | Content width |
| Accepts width/height | Yes               | No (height ignored) | Yes           |

## Follow-up

- [ ] Convert inline text to block-level cards using `display: block` and inspect spacing.
- [ ] Experiment with `display: inline-block` to create pill-shaped navigation items without breaking the line.
- [ ] Note which elements in your project rely on manual display overrides and decide if a semantic alternative fits better.
---
title: Block vs Inline Elements
status: draft
last_reviewed: 09-11-2025
---

