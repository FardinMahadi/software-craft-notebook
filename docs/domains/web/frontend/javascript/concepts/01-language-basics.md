---
title: JavaScript Language Basics
status: draft
last_reviewed: 09-11-2025
---

# JavaScript Language Basics

## Why It Matters

- Mastering modern syntax and scope rules prevents subtle bugs and lays the foundation for advanced topics.

## Core Ideas

- Execution model: single-threaded event loop with call stack plus task/microtask queues; enable strict mode to catch silent errors.
- Declarations & scope: favor `const`/`let`, avoid `var`; understand block scope, closures, hoisting, and the temporal dead zone.
- Types & comparisons: learn primitive vs object types, prefer `===`, know falsy values, convert explicitly.
- Strings & templates: use template literals for interpolation/multi-line text; tagged templates preprocess input when needed.
- Destructuring & spread: break apart arrays/objects, use rest/spread for cloning/merging, provide defaults.
- Control flow: combine `if`, `switch`, ternary, logical operators; distinguish `||` vs `??` for default values.

## Real-World Scenario

- Refactoring a legacy script from `var` to `const`/`let` eliminated race conditions caused by hoisting and clarified which values could change. Adding "use strict" surfaced undeclared globals during tests.

## Follow-up

- [ ] Rewrite a snippet using `var` declarations to `let`/`const` and explain scope differences.
- [ ] Use destructuring to extract nested props with defaults in a React component.
- [ ] Implement a guard function using `??` to provide default config values without overriding valid falsy settings.

---

**Notes**

- Confirm ES2023/ES2024 features (e.g., `structuredClone`, `findLast`) availability when referencing runtime targets.
- Link MDN event loop article for future deep dives if needed.
