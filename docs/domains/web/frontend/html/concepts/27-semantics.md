# Semantic Structure

## Why It Matters

- Semantic elements convey meaning, improving accessibility, SEO, and maintainability.
- Assistive technologies rely on landmarks and headings to navigate content quickly.
- Semantic markup reduces the need for custom ARIA roles or JavaScript fixes later.

## Core Ideas

- Start with `<!DOCTYPE html>` and set `<html lang="">` for localization hints.
- Use landmarks (`<header>`, `<nav>`, `<main>`, `<aside>`, `<footer>`) so screen readers can skip efficiently.
- Choose descriptive containers (`<section>`, `<article>`, `<figure>`, `<time>`, `<blockquote>`) instead of stacking `<div>`s.
- Include essential metadata: `<title>`, `<meta charset>`, viewport, descriptions, and social cards.
- Let native semantics handle roles and interactions; add ARIA only when no native element fits.

## Real-World Scenario

- A company redesigns their marketing site. By mapping each component to semantic tags, the SEO score improves and audits find fewer accessibility issues. Future contributors understand where to place new sections without guessing class names.

## Examples

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>Semantic Skeleton</title>
  </head>
  <body>
    <header>
      <nav aria-label="Primary">
        <a href="/">Logo</a>
        <ul>
          <li><a href="/features">Features</a></li>
          <li><a href="/pricing">Pricing</a></li>
        </ul>
      </nav>
    </header>
    <main>
      <article>
        <header><h1>Feature Spotlight</h1></header>
        <p>Explain why this feature matters.</p>
      </article>
    </main>
    <footer>&copy; 2025 Acme Inc.</footer>
  </body>
</html>
```

## Follow-up

- [ ] Run an accessibility audit (Lighthouse, axe) to detect missing landmarks or headings.
- [ ] Document landmark expectations for shared layouts in your style guide.
- [ ] Add semantic tags to existing components and remove redundant ARIA roles where native elements suffice.
---
title: Semantic Structure
status: draft
last_reviewed: 09-11-2025
---

