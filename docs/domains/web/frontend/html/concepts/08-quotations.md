---
title: HTML Quotations
status: draft
last_reviewed: 09-11-2025
---

# HTML Quotations and Citations

## Why It Matters

- Proper quotation markup preserves attribution and improves readability.
- Screen readers and search engines understand when text is quoted or referenced.
- Abbreviations with definitions help newcomers grasp jargon without breaking flow.

## Core Ideas

- Use `<blockquote>` for multi-line quotes; include the `cite` attribute to store the source URL.
- `<q>` handles short inline quotes and adds quotation marks automatically.
- `<cite>` references titles of works (books, podcasts, articles).
- `<abbr title="Full phrase">` reveals definitions on hover and to assistive tech.

## Real-World Scenario

- A company blog publishes customer success stories. Marketing quotes customers inside `<blockquote>` with links to interviews, references the product name using `<cite>`, and adds `<abbr>` for industry terms. Readers trust the content more, and legal reviews finish faster because sources are explicit.

## Examples

```html
<p>
  The report notes that <abbr title="User Experience">UX</abbr> teams thrive when
  they share a common design vocabulary.
</p>
<blockquote cite="https://example.com/design-systems">
  <p>“Design systems scale not only UI but decision-making.”</p>
</blockquote>
<p>
  The insight first appeared in <cite>Design Systems Handbook</cite>, published in 2023.
</p>
```

## Follow-up

- [ ] Tag long quotes in your notes with `<blockquote>` and add a `cite` URL.
- [ ] Replace inline quotation marks with `<q>` to let the browser manage punctuation.
- [ ] Create a glossary using `<abbr>` so readers can hover to learn unfamiliar terms.
