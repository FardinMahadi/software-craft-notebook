---
title: HTML Formatting
status: draft
last_reviewed: 09-11-2025
---

# HTML Formatting Elements

## Why It Matters

- Semantic inline elements convey meaning beyond visual styling.
- Screen readers pick up emphasis, edits, and highlights when you use proper tags.
- Formatting elements avoid brittle CSS hacks for basic text variations.

## Core Ideas

- `<strong>` indicates importance; `<em>` signals stress emphasis.
- `<b>` and `<i>` are purely visual—use them when no semantic alternative fits.
- `<mark>` highlights text, `<small>` adds side notes, `<sub>`/`<sup>` handle formulas and references.
- `<del>` and `<ins>` document changes in release notes or contracts.

## Real-World Scenario

- A product manager drafts changelog entries highlighting features and deprecations. Using `<strong>` for “important update,” `<mark>` for rollout dates, and `<del>`/`<ins>` for API changes keeps communication clear to both readers and assistive technologies—reducing onboarding friction for customer success teams.

## Examples

```html
<p>
  Always <strong>validate</strong> forms and provide
  <em>meaningful</em> feedback for users.
</p>
<p>
  The <b>Beta+</b> program is closed, but the <i>waitlist</i> remains open.
</p>
<p>
  Track <del>deprecated</del> <ins>replacement</ins> APIs in the changelog.
  <small>Rollout finishes by Q3.</small>
</p>
<p>
  Water is H<sub>2</sub>O and E = mc<sup>2</sup>.
</p>
```

## Follow-up

- [ ] Rewrite a paragraph using semantic formatting instead of inline CSS.
- [ ] Review a changelog or blog post and swap purely visual `<b>/<i>` for semantic alternatives where appropriate.
- [ ] Test the page with a screen reader to confirm emphasis is announced as intended.
