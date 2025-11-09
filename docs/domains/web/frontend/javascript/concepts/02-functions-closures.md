---
title: Functions, Scope & Closures
status: draft
last_reviewed: 09-11-2025
---

# Functions, Scope & Closures

## Function Forms

- Declarations: `function greet() {}` hoisted within scope.
- Expressions: `const greet = function() {};` useful for conditional definitions.
- Arrow functions: concise syntax, lexically bind `this`, and do not have their own `arguments`.
- Use default parameters (`function fetchData(url, options = {})`) to simplify call sites.

## `this` Binding

- In arrow functions, `this` equals surrounding lexical scope; ideal for callbacks that need outer context.
- In regular functions, `this` depends on call site: method invocation, `call/apply/bind`, or constructor with `new`.
- Avoid using `this` in modules where closures or explicit parameters make data flow clearer.

## Closures & State

- Closures capture variables from enclosing scopes, enabling private state patterns:

```js
function createCounter() {
  let count = 0;
  return () => ++count;
}
const increment = createCounter();
increment(); // 1
```

- In React, closures affect state updates; ensure functions reference current values (preferred functional `setState`).

## Higher-Order Functions

- Functions can accept other functions (callbacks) or return new functions; enables composition.
- Common patterns: `map`, `filter`, `reduce`, custom hooks returning handler functions.
- Curry functions to prefill arguments: `const withLogger = (fn) => (...args) => { console.log(args); return fn(...args); };`

## Parameter & Rest Handling

- Rest parameters (`function sum(...nums)`) gather variable arguments.
- Spread arguments when forwarding (`fn(...args)`), especially when wrapping callbacks.
- Validate argument types defensively in shared utilities.

## Practice Prompts

- Build a `memoize` helper using closures to cache heavy computation results.
- Convert a class method relying on `this` to an arrow function and explain the binding change.
- Create a higher-order event handler passing configuration (`handleClick = withAnalytics('like', logEvent)`).
