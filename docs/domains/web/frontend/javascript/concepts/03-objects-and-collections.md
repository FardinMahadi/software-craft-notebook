---
title: Objects, Collections & Immutability
status: draft
last_reviewed: 09-11-2025
---

# Objects, Collections & Immutability

## Object Manipulation

- Use property shorthand (`{ name, age }`) and computed keys (`{ [id]: value }`).
- Clone objects with spread (`{ ...user, active: true }`) or structuredClone for deep copies.
- Use `Object.assign` cautiously; avoid mutating source objects.

## Array Operations

- Immutable transformations: `map`, `filter`, `reduce`, `slice`, `concat`.
- Spread to append/prepend: `[...list, newItem]`, `[newItem, ...list]`.
- Prefer `find`/`some`/`every` for search, `flatMap` for nested arrays.

## Maps, Sets & Weak Collections

- `Map` maintains insertion order, supports non-string keys; ideal for caching.
- `Set` ensures uniqueness and supports fast membership checks.
- Weak variants (`WeakMap`, `WeakSet`) allow garbage collection; useful for metadata tied to objects.

## Destructuring Patterns

- Extract nested properties: `const { profile: { email } = {} } = user`.
- Rename while destructuring: `const { id: userId } = user`.
- Combine with defaults for optional properties.

## Immutability in React

- Never mutate state directly; create new references to trigger re-renders.
- Nested updates: `setState(prev => ({ ...prev, settings: { ...prev.settings, theme } }))`.
- Use libraries (`immer`) when updates become complex, but understand plain JS first.

## Practice Prompts

- Given an array of products, produce derived arrays (available only, sorted by price) without mutating the original list.
- Convert an object keyed by IDs into an array of values and vice versa using `reduce`.
- Implement a lookup cache using `Map` with JSON responses keyed by request URL.
