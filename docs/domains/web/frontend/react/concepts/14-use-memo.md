---
title: useMemo Deep Dive
status: draft
last_reviewed: 09-11-2025
---

# `useMemo` Deep Dive

## Purpose

- Memoize derived values or computations to avoid recalculating expensive logic on every render.
- Ensure referential equality for dependency arrays (e.g., context values, memoized components).

## Basic Syntax

```jsx
const memoizedValue = useMemo(() => computeExpensiveValue(a, b), [a, b]);
```

- React re-computes the function only when dependencies change.
- Return value is cached between renders.

## When to Use

- Filtering/sorting large lists.
- Computing derived data structures (maps, tree transforms).
- Memoizing configuration objects passed as props/context values to avoid re-renders.
- Avoid using `useMemo` for simple calculations; premature optimization adds complexity.

## Example: Filtered List

```jsx
const filteredProducts = useMemo(() => {
  const lower = search.toLowerCase();
  return products.filter((product) =>
    product.name.toLowerCase().includes(lower)
  );
}, [products, search]);
```

## Memoizing Context Values

```jsx
const AuthContext =
  (createContext < AuthContextValue) | (undefined > undefined);

function AuthProvider({ children }: PropsWithChildren) {
  const [user, setUser] = (useState < User) | (null > null);

  const value = useMemo(
    () => ({ user, login: setUser, logout: () => setUser(null) }),
    [user]
  );

  return <AuthContext.Provider value={value}>{children}</AuthContext.Provider>;
}
```

- Without `useMemo`, provider re-renders cause consumers to re-render even if the value shape hasn't changed.

## Dependency Arrays

- Include all values referenced inside the memo callback.
- If ESLint warns about missing dependencies, heed it—memoization relies on correct dependencies.
- For functions defined inline, prefer `useCallback` or define outside to avoid constant changes.

## Pitfalls

- `useMemo` does not guarantee performance improvement—measure before optimizing.
- Memoized value recalculates if dependencies are unstable (e.g., new object instances). Ensure dependencies are stable or memoized themselves.
- Avoid storing side effects or asynchronous logic inside `useMemo`; keep it pure.

## Testing

- Write tests covering scenarios where dependencies change or remain the same; ensure results update appropriately.
- In performance-sensitive components, profile with React DevTools before/after applying memoization.

## Practice Prompts

- Memoize a derived chart data structure used in a visualization component and measure render times before/after.
- Refactor a context provider to memoize its value and document the effect on consumer re-renders.
- Implement a `useFilteredList` hook that accepts items and filters, memoizes the results, and unit tests dependency behavior.
