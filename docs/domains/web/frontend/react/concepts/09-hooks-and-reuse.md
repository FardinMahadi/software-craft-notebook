---
title: Hooks & Reusing Logic
status: draft
last_reviewed: 09-11-2025
---

# Hooks & Reusing Logic

This guide covers core React hooks, performance hooks, `useSyncExternalStore`, and patterns for custom hooks.

## Hook Rules Recap

- Call hooks only at the top level of function components or other hooks.
- Never call hooks inside loops/conditions; branch within the hook body after invocation.
- Prefix custom hooks with `use` so lint rules can enforce proper usage.

## Core Hooks (State, Context, Effects, Refs)

- **`useState`** – local component memory. Accepts an initial value or initializer callback. Prefer functional updates when referencing prior state:

  ```jsx
  const [count, setCount] = useState(
    () => Number(localStorage.getItem("count")) || 0
  );
  const increment = () => setCount((prev) => prev + 1);
  ```

- **`useReducer`** – centralize transitions when state changes depend on multiple events or complex logic:

  ```jsx
  type Action = { type: "add", task: Task } | { type: "remove", id: string };
  const [state, dispatch] = useReducer(reducer, initialState);
  ```

- **`useContext`** – consume nearest provider. Wrap in a helper hook to guarantee provider usage:

  ```jsx
  const ThemeContext =
    (createContext < ThemeContextValue) | (undefined > undefined);
  const useTheme = () => {
    const ctx = useContext(ThemeContext);
    if (!ctx) throw new Error("useTheme must be used within ThemeProvider");
    return ctx;
  };
  ```

- **`useEffect`** – synchronize with external systems after render. Always include dependencies and clean up subscriptions:

  ```jsx
  useEffect(() => {
    const subscription = dataSource.subscribe(setData);
    return () => subscription.unsubscribe();
  }, [dataSource]);
  ```

- **`useLayoutEffect`** – runs synchronously after DOM mutations but before paint. Use for measurements or imperative layout adjustments; keep work minimal to avoid blocking paint.

- **`useInsertionEffect`** – inject critical styles before layout (mainly for CSS-in-JS libraries).

- **`useRef`** – persistent mutable container; `.current` updates do not trigger renders. Ideal for DOM nodes, timers, or storing previous values.

- **`useImperativeHandle`** – expose a custom imperative API when using `forwardRef`:

  ```jsx
  useImperativeHandle(ref, () => ({ focus: () => inputRef.current?.focus() }));
  ```

- **`useId`** – generate stable, unique IDs across server/client renders for accessibility attributes (`aria-labelledby`, etc.).

## Performance Hooks

- **`useMemo`** – memoize derived values to avoid recalculating heavy computations unless dependencies change:

  ```jsx
  const filtered = useMemo(
    () => items.filter(applyFilters),
    [items, applyFilters]
  );
  ```

- **`useCallback`** – memoize function references. Helpful when passing callbacks to memoized children or effect dependencies:

  ```jsx
  const handleSelect = useCallback((id: string) => setSelected(id), []);
  ```

- **`useTransition`** – mark non-urgent updates (e.g., filtering large lists) so urgent UI updates remain responsive:

  ```jsx
  const [isPending, startTransition] = useTransition();
  const onSearch = (value: string) => startTransition(() => setQuery(value));
  ```

- **`useDeferredValue`** – create a deferred version of state or props to throttle expensive rendering:

  ```jsx
  const deferredQuery = useDeferredValue(query);
  const results = useMemo(() => search(deferredQuery), [deferredQuery]);
  ```

## External Store Integration

- **`useSyncExternalStore`**:
  - Bridges React state with external mutable stores; ensures consistency with concurrent rendering.
  - Signature: `const snapshot = useSyncExternalStore(subscribe, getSnapshot, getServerSnapshot?);`
  - Implement `subscribe` to register listeners, `getSnapshot` to read current value.
  - Use for Redux, Zustand, or custom event emitter interop.

## Custom Hook Patterns

- Encapsulate reusable logic (state, effects, subscriptions) without returning JSX.
- Return consistent shapes (tuple `[value, setter]` or named object).
- Compose hooks internally; keep UI concerns separate.

```jsx
function useLocalStorage<T>(key: string, initialValue: T) {
  const [value, setValue] = useState<T>(() => {
    const stored = window.localStorage.getItem(key);
    return stored ? JSON.parse(stored) : initialValue;
  });

  useEffect(() => {
    window.localStorage.setItem(key, JSON.stringify(value));
  }, [key, value]);

  return [value, setValue] as const;
}
```

## Sharing Behavior vs UI

- Keep hooks UI-agnostic; components render UI using data/handlers returned by hooks.
- Pair hooks with context providers (`useAuth`, `useTheme`) to encapsulate domain state.
- Return memoized values to prevent unnecessary re-renders down the tree.

## Testing Hooks

- Use React Testing Library’s `renderHook` (or `@testing-library/react-hooks`) to render hooks in isolation.
- Mock external dependencies (storage, network, timers) to avoid flakiness.
- Assert cleanup behavior by unmounting hooks and verifying listeners/subscriptions are removed.

## Practice Prompts

- Refactor duplicated effect logic into a `useDocumentTitle` hook and integrate it into multiple components.
- Implement a `useUndoRedo` hook managing history stacks for a form and add tests covering add/undo/redo flows.
- Build a hook that subscribes to an external store using `useSyncExternalStore`, then document how to mock the store during testing.
