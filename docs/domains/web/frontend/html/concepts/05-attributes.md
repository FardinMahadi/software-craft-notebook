---
title: HTML Attributes
status: draft
last_reviewed: 09-11-2025
---

# HTML Attributes

## Why It Matters

- Attributes add meaning and behavior to elements without changing structure.
- Consistent attribute usage makes styling, scripting, and accessibility easier.
- Clean attribute choices prevent bugs caused by typos or mismatched values.

## Core Ideas

- Attributes live in the opening tag: `<element attribute="value">`.
- Global attributes (`id`, `class`, `lang`, `data-*`) can appear on most elements; element-specific ones (`href`, `src`, `alt`) only work where defined.
- Boolean attributes (`disabled`, `checked`, `required`) are true when present—no value needed.
- Custom `data-*` attributes safely store extra info for JavaScript via `element.dataset`.

## Real-World Scenario

- A news site personalizes the homepage by tagging sections with `data-topic="finance"` or `data-topic="sports"`. The front end filters which sections to highlight for each reader, while CSS uses shared classes for styling. Clear attribute conventions keep designers, developers, and content editors aligned.

## Examples

```html
<a id="cta-signup" class="button primary" href="/signup" data-track="hero-cta">
  Join the newsletter
</a>

<input type="checkbox" id="subscribe" name="subscribe" checked />
<label for="subscribe">Email me about product updates</label>
```

## Follow-up

- [ ] Audit an existing page and list which global attributes appear most often.
- [ ] Add a `data-*` attribute to an element and read it via `element.dataset` in the console.
- [ ] Validate your markup to catch misspelled or invalid attribute names.
