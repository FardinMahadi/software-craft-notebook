# HTML Links

## Why It Matters

- Anchor tags connect pages, sections, downloads, and contact actions.
- Descriptive link text improves accessibility and SEO.
- Safe link attributes prevent security issues when opening new tabs.

## Core Ideas

- Use `<a href="...">` with absolute URLs, relative paths, or fragment identifiers (`#faq`).
- Make link text meaningful (“View pricing”) instead of generic (“Click here”).
- Wrap block-level content inside anchors for clickable cards in HTML5.
- When using `target="_blank"`, add `rel="noopener noreferrer"` to block tab hijacking.
- The `download` attribute prompts file saves; `mailto:` and `tel:` handle email or phone links.

## Real-World Scenario

- A documentation site includes a “Jump to API Reference” link near the top. Clear anchor text and fragment IDs let developers skip quickly, while external links open in new tabs without exposing the main window to third-party scripts.

## Examples

```html
<a
  href="https://www.example.com/docs"
  target="_blank"
  rel="noopener noreferrer"
>
  Read the documentation
</a>

<a href="#faq">Skip to FAQ</a>

<a href="/files/product-brief.pdf" download>Download the product brief</a>
```

## Follow-up

- [ ] Build a table of contents using fragment links and test with keyboard navigation.
- [ ] Audit external links to confirm `rel` accompanies `target="_blank"`.
- [ ] Experiment with `mailto:` and `tel:` schemes, ensuring fallback contact methods exist.
---
title: HTML Links
status: draft
last_reviewed: 09-11-2025
---

