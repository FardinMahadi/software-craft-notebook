# HTML vs XHTML

## Why It Matters

- HTML5 is the modern standard, but XHTML rules still appear in legacy systems and influence strict coding styles.
- Understanding the differences helps when migrating old sites or integrating with XML-based tooling.

## Core Ideas

- HTML5 syntax is flexible: tag/attribute names are case-insensitive, void elements (`<br>`, `<img>`) don’t require self-closing slashes, and browsers repair many errors.
- XHTML is XML-based: tags must be lowercase, properly closed (`<br />`), attribute values quoted, and boolean attributes explicit (`disabled="disabled"`).
- XHTML documents often use the `application/xhtml+xml` MIME type, causing browsers to enforce strict XML parsing (any error breaks rendering).
- Most modern projects serve HTML5 for simplicity and broad tooling support; XHTML surfaces mainly in legacy enterprise stacks or XML pipelines.

## Real-World Scenario

- An enterprise CMS still outputs XHTML for integration with an XML transformer. While the engineering team modernizes templates to HTML5, they maintain backward compatibility by ensuring well-formed markup and testing how browsers behave under both doctypes.

## Examples

```html
<!-- HTML5 -->
<input type="checkbox" checked />

<!-- XHTML -->
<input type="checkbox" checked="checked" />
```

## Follow-up

- [ ] Convert an HTML5 snippet to XHTML-compliant markup and validate with an XML parser.
- [ ] Review legacy pages that declare XHTML to plan migration to HTML5.
- [ ] Decide whether strict linting rules (self-closing tags, lowercase attributes) still add value in your current projects.

---

title: HTML vs XHTML
status: draft
last_reviewed: 09-11-2025

---
