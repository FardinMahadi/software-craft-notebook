---
title: JavaScript Language Basics
status: draft
last_reviewed: 09-11-2025
---

# JavaScript Language Basics

## Execution Model & Strict Mode

- JavaScript runs in a single-threaded event loop; understand call stack vs task/microtask queues for async behavior.
- Always enable strict mode (`"use strict"` or bundler defaults) to catch silent errors (e.g., implicit globals).

## Declarations & Scope

- Prefer `const` for immutability and `let` for reassignable bindings; avoid `var`.
- Block scope controls variable lifetime inside `{}`; closures capture lexical scope for functions.
- Hoisting moves declarations to the top of scope, but with `let`/`const` you must respect the temporal dead zone before initialization.

## Types & Comparisons

- Primitive types: string, number, bigint, boolean, null, undefined, symbol. Objects include arrays, functions, dates, maps, sets.
- Use `===` strictly; avoid `==` coercion. Convert explicitly (`Number()`, `Boolean()`) when needed.
- Falsy values: `false`, `0`, `""`, `null`, `undefined`, `NaN`. Guard conditions should account for legitimate values like `0`.

## Strings & Template Literals

- Template literals `` `Hello ${name}` `` support interpolation and multi-line strings.
- Tagged templates allow preprocessing (e.g., styled-components); understand signature `tag(strings, ...values)`.

## Destructuring & Spread

- Destructure arrays/objects for readability (`const { props } = obj`).
- Spread (`...`) clones/merges arrays, objects; rest collects remaining elements/function arguments.
- Default values in destructuring avoid `undefined` type errors.

## Control Flow & Short-Circuiting

- Use `if/else`, `switch`, ternary (`condition ? a : b`), and logical operators (`&&`, `||`, `??`) for conditional logic.
- Nullish coalescing (`??`) preserves valid falsy values like `0`, unlike `||`.

## Practice Prompts

- Rewrite a snippet using `var` declarations to utilize `let`/`const` and explain the differences in scope.
- Use destructuring to extract nested values from a React props object, including defaults.
- Implement a guard function using `??` to provide default config values without overriding valid falsy settings.
