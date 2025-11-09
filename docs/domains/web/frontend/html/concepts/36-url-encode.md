# URL Encoding

## Why It Matters

- URLs accept only a limited set of safe characters; encoding prevents broken links and injection issues.
- User-generated data often includes spaces, symbols, or unicode that must be encoded before adding to a query string.

## Core Ideas

- Percent-encoding converts characters to `%` + hex code (`:` → `%3A`, `/` → `%2F`); spaces become `%20` (or `+` in query strings).
- Use built-in helpers: `encodeURIComponent()` for parameter values, `encodeURI()` for entire URLs.
- Decode data when reading query parameters (`decodeURIComponent`) and avoid double encoding.
- Always encode before sending data across network boundaries (URLs, APIs) and validate on receipt.

## Real-World Scenario

- A search feature lets users filter by topic names that include spaces and slashes (`React/Next Steps`). Encoding the value before constructing the link prevents 404 errors and ensures server handlers parse the correct string.

## Examples

```html
<a href="https://example.com/search?q=layout%20patterns">
  Search for layout patterns
</a>

<script>
  const term = "React/Next Steps";
  const url = `https://example.com/search?q=${encodeURIComponent(term)}`;
  console.log(url);
</script>
```

## Follow-up

- [ ] Construct a query string with special characters and verify encoding using `encodeURIComponent`.
- [ ] Parse encoded URLs in the browser console to confirm decoding behavior (`decodeURIComponent`).
- [ ] Review server-side routing to ensure incoming parameters are decoded and validated.

---

title: URL Encoding
status: draft
last_reviewed: 09-11-2025

---
