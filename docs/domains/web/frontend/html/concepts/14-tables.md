---
title: Data Tables
status: draft
last_reviewed: 09-11-2025
---

## Why It Matters

- Tables communicate structured data effectively when marked up semantically.
- Proper headers and captions keep information accessible to screen readers.
- Responsive strategies prevent data loss on small screens.

## Core Ideas

- Add a concise `<caption>` describing the table’s purpose.
- Use `<thead>`, `<tbody>`, `<tfoot>` for logical grouping and `<th scope="col|row">` to identify headers.
- For complex headers, link cells with `id` on `<th>` and `headers` on `<td>`.
- Provide horizontal scrolling or card layouts on small screens; avoid tables for non-data layouts.

## Real-World Scenario

- The analytics team shares monthly performance metrics. A well-structured table with row/column headers lets executives scan trends quickly, while screen-reader users hear each value with its context. On mobile, the table scrolls horizontally so nothing is truncated.

## Examples

```html
<div class="table-wrapper">
  <table>
    <caption>Monthly Active Users</caption>
    <thead>
      <tr>
        <th scope="col">Month</th>
        <th scope="col">Active</th>
        <th scope="col">Churn</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <th scope="row">January</th>
        <td>1,245</td>
        <td>4.2%</td>
      </tr>
      <tr>
        <th scope="row">February</th>
        <td>1,310</td>
        <td>3.9%</td>
      </tr>
    </tbody>
  </table>
</div>
```

## Follow-up

- [ ] Add a caption and scopes to an existing data table, then test with a screen reader.
- [ ] Implement a responsive wrapper that allows horizontal scrolling on narrow screens.
- [ ] Document which tables need interactive features (sorting, pagination) for future enhancement.
