# Styling Tables

## Why It Matters

- Tables organize data; styling improves readability and interaction.
- Responsive patterns ensure tables stay usable on smaller screens.

## Core Ideas

- Start with `border-collapse: collapse;` and generous padding for `th`/`td`.
- Use zebra striping (`tr:nth-child(even)`) for row separation and sticky headers for long lists.
- Wrap tables in scroll containers or transform rows into cards for mobile layouts.

## Real-World Scenario

- A SaaS dashboard lists customer activity. By adding subtle striping, sticky headers, and a mobile-friendly card layout, the data stays readable on any device without duplicating markup.

## Examples

```css
table {
  border-collapse: collapse;
  width: 100%;
}

th,
td {
  padding: 0.75rem;
  text-align: left;
}

tbody tr:nth-child(even) {
  background: rgb(226 232 240 / 0.5);
}
```

## Follow-up

- [ ] Create a pricing table with sticky header rows and zebra striping.
- [ ] Implement a responsive table that stacks data on mobile breakpoints.
- [ ] Test the table with screen readers to ensure header associations remain intact.
---
title: Styling Tables
status: draft
last_reviewed: 09-11-2025
---

