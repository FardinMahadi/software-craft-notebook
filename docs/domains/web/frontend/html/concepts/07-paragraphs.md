---
title: HTML Paragraphs
status: draft
last_reviewed: 09-11-2025
---

# HTML Paragraphs

## Why It Matters

- Paragraphs keep text readable and responsive without manual spacing tricks.
- Correct whitespace handling prevents unexpected breaks when content changes.
- Understanding line breaks and preformatted blocks makes addresses or code samples display correctly.

## Core Ideas

- Wrap text blocks in `<p>`; browsers handle spacing between paragraphs automatically.
- HTML collapses consecutive spaces and line breaks—formatting is presentation, not structure.
- Use `<br>` for intentional line breaks within a paragraph (addresses, poetry); rely on CSS for spacing elsewhere.
- `<pre>` preserves whitespace verbatim, ideal for code or fixed-format text.
- `<hr>` provides a thematic break between sections.

## Real-World Scenario

- A support team publishes knowledge-base articles with troubleshooting steps and command snippets. Using paragraphs for explanations, `<br>` for addresses, and `<pre>` around terminal commands keeps the article easy to scan and copy, reducing customer confusion.

## Examples

```html
<section>
  <h2>Event Location</h2>
  <p>
    Community Hall<br />
    123 Market Street<br />
    Springfield, USA
  </p>

  <h2>Setup Script</h2>
  <pre><code>npm install
npm run dev
</code></pre>
  <hr />
  <p>Contact us if you need wheelchair access or parking information.</p>
</section>
```

## Follow-up

- [ ] Rewrite a block of text from a document into paragraphs and intentional line breaks.
- [ ] Inspect default margins in dev tools, then adjust them with CSS to understand the handoff.
- [ ] Use `<pre>` with `<code>` to display a multi-line snippet and compare with a normal paragraph.
