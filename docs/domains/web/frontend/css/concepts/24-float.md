# Float & Clear

## Why It Matters

- Floats let text wrap around images and remain in legacy codebases.
- Understanding floats helps when maintaining older layouts or emails.

## Core Ideas

- `float: left/right;` removes an element from normal flow and aligns it to a side; inline content wraps around it.
- Use `clear: both;` on subsequent blocks or a clearfix (`.clearfix::after`) to prevent container collapse.
- Modern layouts favor flexbox/grid; use floats only when needed for wrap effects or legacy support.

## Real-World Scenario

- A blog post wraps author headshots within text. Using floats keeps the reading flow natural while allowing the rest of the layout to rely on flexbox.

## Examples

```css
.article img.figure {
  float: right;
  margin: 0 0 1rem 1.5rem;
}

.clearfix::after {
  content: "";
  display: table;
  clear: both;
}
```

## Follow-up

- [ ] Float an image within an article and ensure subsequent sections clear the float.
- [ ] Refactor a float-based layout into flexbox to compare maintainability.
- [ ] Audit legacy stylesheets and note where floats can be simplified.

---

title: Float & Clear
status: draft
last_reviewed: 09-11-2025

---
