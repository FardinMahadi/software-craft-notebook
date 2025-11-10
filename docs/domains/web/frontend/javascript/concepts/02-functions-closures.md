---
title: Functions, Scope & Closures
status: draft
last_reviewed: 09-11-2025
---

# Functions, Scope & Closures

## Why It Matters

- Functions and closures power reusable logic, state management, and asynchronous APIs in JavaScript.

## Core Ideas

- Function forms: declarations (hoisted), expressions, arrow functions (lexical `this`, no own `arguments`), default parameters.
- `this` binding: arrow functions inherit lexical scope; regular functions depend on call site (`call/apply/bind`, method, constructor).
- Closures capture outer variables to maintain private state (e.g., counters, memoization).
- Higher-order functions accept/return functions (`map`, `filter`, custom hooks, curried helpers).
- Rest/spread parameters simplify variable arguments and forwarding (`function sum(...nums)`, `fn(...args)`).

## Real-World Scenario

- A React hook memoizes API responses using a closure-based cache. Converting event handlers to arrow functions ensured `this` referenced component scope without manual binding.

## Follow-up

- [ ] Build a `memoize` helper using closures to cache expensive computations.
- [ ] Convert a class method relying on `this` to an arrow function and explain the binding change.
- [ ] Create a higher-order event handler that logs analytics before invoking the original callback.
