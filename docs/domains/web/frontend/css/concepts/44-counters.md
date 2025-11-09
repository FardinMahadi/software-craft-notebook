---
title: CSS Counters
status: draft
last_reviewed: 09-11-2025
---

# CSS Counters

## Why It Matters

- Counters automatically number headings, sections, or list items, removing manual updates.

## Core Ideas

- Initialize counters with `counter-reset`; increment with `counter-increment` and display via `content: counter(name)`.
- Nest counters for hierarchical numbering.
- Combine with pseudo-elements to keep HTML clean.

## Real-World Scenario

- Documentation headings use counters to generate “Section 1.2” labels automatically. Writers reorder content freely without fixing numbering by hand.

## Examples

```css
body {
  counter-reset: section;
}

h2::before {
  counter-increment: section;
  content: 'Section ' counter(section) '. ';
}
```

## Follow-up

- [ ] Number documentation sections using counters to avoid manual renumbering.
- [ ] Build a task list that prepends incremental IDs to each item.
- [ ] Try nested counters for subheadings (e.g., section + subsection).
