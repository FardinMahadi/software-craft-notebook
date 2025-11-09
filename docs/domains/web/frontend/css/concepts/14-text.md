# CSS Text Styling

## Why It Matters

- Thoughtful text styling improves readability and communicates hierarchy.
- Small adjustments to spacing or decoration can transform the tone of a page.

## Core Ideas

- Key properties: `color`, `text-align`, `text-decoration`, `text-transform`, `text-indent`, `letter-spacing`, `word-spacing`, `line-height`.
- Use text shadows sparingly to enhance contrast (`text-shadow: 0 2px 4px rgb(15 23 42 / 0.25);`).
- Truncate overflowing text with `white-space: nowrap; overflow: hidden; text-overflow: ellipsis;`.
- Build typographic scales to keep font sizes and spacing consistent.

## Real-World Scenario

- A documentation site updates line height and letter spacing for body text. Readers report less eye strain on long articles, and the support team sees fewer “hard to read” complaints.

## Examples

```css
.heading-xl {
  font-size: clamp(2rem, 5vw, 3.5rem);
  line-height: 1.1;
}

.body-copy {
  line-height: 1.7;
  letter-spacing: 0.01em;
}

.truncate {
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}
```

## Follow-up

- [ ] Create a typographic scale for headings and body copy.
- [ ] Experiment with line height and letter spacing to improve readability on long-form text.
- [ ] Review text overflow cases (cards, tables) and decide when to show ellipsis vs. wrapping.
---
title: CSS Text Styling
status: draft
last_reviewed: 09-11-2025
---

