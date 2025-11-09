---
title: HTML Comments
status: draft
last_reviewed: 09-11-2025
---

# HTML Comments

## Why It Matters

- Comments capture intent, making future maintenance easier.
- Temporary notes help collaborators understand unfinished sections without changing layout.
- Careful use prevents shipping sensitive information to end users.

## Core Ideas

- Syntax: `<!-- comment text -->`; browsers ignore comments but they remain in the HTML source.
- Keep comments concise and purposeful—describe why, not what.
- Avoid leaving secrets, credentials, or internal chatter in comments; anyone can view page source.
- Prefer progressive enhancement over conditional comments for old browsers.

## Real-World Scenario

- A product team coordinates a homepage refresh. Designers add `<!-- TODO: replace hero image after photoshoot -->`, and engineers see it during code review. Once assets arrive, the comment disappears, and no one wastes time searching Slack threads to remember the next step.

## Examples

```html
<!-- Hero Section: update CTA copy before Q4 launch -->
<section class="hero">
  <h1>Build faster with reusable components</h1>
  <p>Ship UI updates in days, not weeks.</p>
</section>

<!-- Temporary: remove this banner after 2025-12-31 -->
<aside class="sale-banner">Holiday sale ends soon!</aside>
```

## Follow-up

- [ ] Annotate major sections of a template with comments explaining their purpose.
- [ ] Run a search to ensure no debug comments or secrets make it to production.
- [ ] Replace outdated comments with documentation links or delete them once work is complete.
