---
title: Objects, Collections & Immutability
status: draft
last_reviewed: 09-11-2025
---

# Objects, Collections & Immutability

## Why It Matters

- Working with data structures safely prevents bugs, especially in stateful UI frameworks.

## Core Ideas

- Object manipulation: property shorthand, computed keys, spread cloning, `structuredClone` for deep copies, avoid mutating sources.
- Arrays: use immutable helpers (`map`, `filter`, `reduce`, `slice`, `concat`), employ spread to append/prepend, leverage `find/some/every/flatMap` for queries.
- Maps & Sets: `Map` for ordered key/value with non-string keys, `Set` for uniqueness, weak collections for metadata tied to object lifecycle.
- Destructuring: extract/rename nested properties with defaults to avoid `undefined` errors.
- Immutability in React: never mutate state; create new references, use nested spreads or `immer` when updates get complex.

## Real-World Scenario

- A React app managed user preferences. Switching to immutable updates prevented stale renders and made undo/redo features straightforward.

## Follow-up

- [ ] Produce derived arrays (e.g., filter available products, sort by price) without mutating the original list.
- [ ] Convert an object keyed by IDs into an array and back using `reduce`.
- [ ] Implement a request cache using `Map` keyed by URL for JSON responses.
