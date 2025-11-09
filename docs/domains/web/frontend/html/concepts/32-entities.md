# HTML Entities & Symbols

## Why It Matters

- Entities allow you to display reserved characters (`<`, `>`, `&`) without breaking markup.
- They provide consistent ways to include typographic symbols, math notation, currency, and emoji.
- Understanding entities helps when working with legacy content or limited text encodings.

## Core Ideas

- Named entities are easier to read (`&copy;`), while numeric or hex codes cover symbols without names (`&#169;`, `&#x1F680;`).
- UTF-8 files can often include literal characters, but entities ensure reliability across editors and servers.
- Use entities for characters that might be misinterpreted by HTML parsers or when pasting from rich text.

## Real-World Scenario

- A legal page requires ©, ™, and smart quotes throughout. By using entities, the content team avoids copy/paste glitches and ensures the characters render correctly in email templates and PDFs generated from the same HTML.

## Examples

| Character | Entity Name | Numeric Code |
| --------- | ----------- | ------------ |
| <         | `&lt;`      | `&#60;`      |
| >         | `&gt;`      | `&#62;`      |
| &         | `&amp;`     | `&#38;`      |
| ©         | `&copy;`    | `&#169;`     |
| €         | `&euro;`    | `&#8364;`    |
| —         | `&mdash;`   | `&#8212;`    |
| 🚀        | —           | `&#x1F680;`  |

```html
<p>Render braces: &lt;div&gt;Content&lt;/div&gt;</p>
<p>&copy; 2025 Study Lab · All rights reserved.</p>
```

## Follow-up

- [ ] Replace raw `<` or `&` characters in documentation with entities to prevent parsing errors.
- [ ] Create a quick reference sheet for symbols frequently used in your project.
- [ ] Verify that your build pipeline preserves UTF-8 so literal emoji or symbols stay intact.
---
title: HTML Entities & Symbols
status: draft
last_reviewed: 09-11-2025
---

