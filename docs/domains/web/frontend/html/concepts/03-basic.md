---
title: HTML Basics
status: draft
last_reviewed: 09-11-2025
---

# HTML Basic

## Why It Matters

- Every HTML page shares the same core skeleton; mastering it prevents broken layouts.
- Clear heading and paragraph structure improves readability and screen-reader navigation.
- Simple elements help you focus on content before layering in style or behavior.

## Core Ideas

- Begin with the boilerplate: `<!DOCTYPE html>`, `<html>`, `<head>`, and `<body>`.
- Use headings (`<h1>`–`<h6>`) to describe hierarchy; the main topic gets a single `<h1>`.
- Paragraphs (`<p>`) represent blocks of text; use `<br />` sparingly for line breaks and `<hr />` to separate sections.
- Comments (`<!-- ... -->`) document decisions without affecting the output.

## Real-World Scenario

- A nonprofit needs a simple FAQ page for an upcoming event. With headings for each question and paragraphs for answers, volunteers keep information tidy. Later, designers add styling, but the content structure already works well for screen readers and search engines.

## Examples

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <title>Basic Example</title>
  </head>
  <body>
    <h1>Frequently Asked Questions</h1>
    <h2>What time does the event start?</h2>
    <p>The doors open at 6:00 PM, and the keynote begins at 7:00 PM.</p>
    <hr />
    <h2>Where is the venue?</h2>
    <p>
      The event takes place at the Riverside Community Center.<br />
      Parking is available on-site.
    </p>
    <!-- Reminder: Add a link to the parking map once it is finalized -->
  </body>
</html>
```

## Follow-up

- [ ] Build your own page with a title, headings, and paragraphs describing a topic you know.
- [ ] Add comments to note future improvements before sharing the file.
- [ ] Validate the page with the W3C Markup Validator to confirm the structure is sound.
