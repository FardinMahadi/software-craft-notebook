---
title: useCallback Deep Dive
status: draft
last_reviewed: 09-11-2025
---

# `useCallback` Deep Dive

## Purpose

- Memoize function references so they remain stable between renders.
- Prevent unnecessary re-renders of memoized children (`React.memo`) or repeated effect subscriptions.
- Stabilize callbacks used in dependency arrays.

## Basic Syntax

```jsx
const memoizedHandler = useCallback((value: string) => {
  setState(value);
}, []);
```

- React returns the same function reference as long as dependencies are unchanged.
- Equivalent to `useMemo(() => handler, deps)` but reads more clearly for functions.

## When to Use

- Passing callbacks to child components that rely on referential equality (memoized).
- Registering event listeners or subscriptions inside effects.
- Avoiding re-runs of `useEffect` when callbacks appear in dependency arrays.

## Example: Memoized Child Handler

```jsx
const handleSelect = useCallback(
  (id: string) => setSelectedId((prev) => (prev === id ? null : id)),
  []
);

return <List items={items} onSelect={handleSelect} />;
```

- Without `useCallback`, each render creates a new function and memoized children re-render unnecessarily.

## Stable Dependencies

- Include every value used inside the callback.
- If the callback depends on state/props, add them to dependencies or leverage functional updates to avoid stale closures.

```jsx
const increment = useCallback(() => setCount((prev) => prev + 1), []);
```

- Functional update removes `count` from dependencies by referencing previous state.

## Interaction with `useMemo`

- Wrap complex objects in `useMemo` and functions in `useCallback` to maintain stable dependencies.
- Memoized callbacks can be used inside `useMemo` to compose memoized values.

## Performance Considerations

- `useCallback` introduces overhead; only apply when child memoization or effect dependencies require stable references.
- Do not wrap every function by default—profile first.

## Testing & Debugging

- Snapshot tests or debug logs can verify whether child components avoid re-rendering when `useCallback` is applied.
- Use React DevTools “Highlight Updates” to observe changes before/after memoization.

## Practice Prompts

- Memoize event handlers in a form with many inputs to prevent re-render storms and confirm with profiling.
- Build a toggle list component using `React.memo` + `useCallback` and show how removing `useCallback` affects renders.
- Create a custom hook `useStableCallback` that wraps callbacks with logging to debug dependency issues, then test it.
