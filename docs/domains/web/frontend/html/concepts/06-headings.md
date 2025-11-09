---
title: HTML Headings
status: draft
last_reviewed: 09-11-2025
---

# HTML Headings

## Why It Matters

- Headings describe document structure, helping readers and search engines scan content quickly.
- Accessible outlines let screen-reader users jump to the section they need.
- Consistent heading levels reduce styling hacks and keep CSS simpler.

## Core Ideas

- Use `<h1>` once per page for the main topic; nested sections use `<h2>`–`<h6>` in order.
- Choose heading levels based on meaning, not default size—override appearance with CSS classes instead.
- Tools like HeadingsMap (browser extension) show the outline to catch skipped levels.

## Real-World Scenario

- A documentation team publishes installation guides for multiple platforms. When each page follows a strict heading hierarchy (`<h1>` product name, `<h2>` platform, `<h3>` step groups), users can rely on the sidebar TOC and screen readers announce a predictable outline—reducing support tickets.

## Examples

```html
<h1>Documentation Playbook</h1>
<h2>Purpose</h2>
<p>Explains why the playbook exists and who benefits from it.</p>
<h2>Audience</h2>
<h3>Contributors</h3>
<p>How to submit updates.</p>
<h3>Reviewers</h3>
<p>Checklist to approve new guides.</p>
```

## Follow-up

- [ ] Outline a multi-section article using headings only, then fill in paragraphs.
- [ ] Audit an existing page with HeadingsMap or dev tools to ensure levels aren’t skipped.
- [ ] Refactor a page that misused `<h3>` for visual size by replacing it with `<p>` plus CSS.
