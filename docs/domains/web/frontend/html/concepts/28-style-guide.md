# HTML Style Guide & Conventions

## Why It Matters

- Consistent formatting makes markup easier to read, review, and debug.
- Shared conventions reduce merge conflicts and onboarding time for new contributors.
- Automated linting prevents subtle accessibility or style regressions.

## Core Ideas

- Use lowercase tag names and kebab-case identifiers (`hero-banner`, `primary-nav`).
- Agree on indentation (two spaces or project standard) to reveal hierarchy.
- Order attributes predictably: `id`, `class`, `name`, `data-*`, then other attributes; wrap values in double quotes.
- Keep line length reasonable (~120 characters); break long attribute lists onto new lines.
- Document non-obvious decisions with concise comments and remove temporary TODOs before shipping.
- Integrate formatters (Prettier) and validators (HTMLHint, ESLint plugins) into the toolchain.

## Real-World Scenario

- A distributed team collaborates on a design system. With a documented HTML style guide and automated formatter, pull requests focus on component behavior instead of whitespace or naming nitpicks, speeding up reviews.

## Examples

```html
<section id="hero-banner" class="hero">
  <h1>Build accessible interfaces faster</h1>
  <p>Track modules, labs, and reflections in one workspace.</p>
  <a class="cta-button" href="/signup">Get started</a>
</section>

<!-- TODO: Replace placeholder copy before launch -->
```

## Follow-up

- [ ] Run a formatter on a messy HTML file and compare before/after readability.
- [ ] Document style conventions (naming, indentation, attribute order) in your project README.
- [ ] Add HTML linting/formatting to your pre-commit or CI workflow.
---
title: HTML Style Guide & Conventions
status: draft
last_reviewed: 09-11-2025
---

