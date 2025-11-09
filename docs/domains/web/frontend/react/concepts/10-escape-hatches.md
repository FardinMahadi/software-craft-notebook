---
title: Escape Hatches
status: draft
last_reviewed: 09-11-2025
---

# Escape Hatches

Escape hatches let you interact with the DOM or browser APIs when declarative patterns aren’t enough. Use them deliberately.

## Refs for Mutable Values

- `useRef` returns a mutable `.current` object that survives re-renders without triggering updates.
- Ideal for storing DOM nodes (`ref` attribute) or other mutable data (timers, previous values).

```jsx
const inputRef = useRef(null);

function focusInput() {
  inputRef.current?.focus();
}

return <input ref={inputRef} />;
```

## Manipulating the DOM

- Access DOM nodes through refs; avoid direct DOM manipulation during render.
- Imperative operations should live in event handlers or effects.

## Effects for Synchronization

- `useEffect` runs after commit to synchronize with external systems (network requests, subscriptions).
- Clean up side effects by returning a cleanup function from the effect.

```jsx
useEffect(() => {
  const id = setInterval(() => {
    tick();
  }, 1000);
  return () => clearInterval(id);
}, [tick]);
```

## Minimizing Effects

- Effects are often overused; derive data during render when possible.
- Prefer event handlers or state updates over effects for reacting to user input.
- Think of effects as synchronizing with systems outside React (DOM APIs, storage, network).

## Effect Lifecycles

- Dependencies array dictates when effects re-run; include all reactive values.
- Separate concerns into multiple effects instead of writing monolithic effect blocks.
- Use `useLayoutEffect` only when you need to measure DOM layout before paint.

## Removing Dependencies

- Extract logic into functions declared inside the effect or mark them as dependencies.
- Use refs to store mutable values that should not trigger re-renders.
- Memoize callbacks (`useCallback`) or values (`useMemo`) when necessary for stable references.

## Custom Hooks

- Encapsulate reusable effect-driven logic into custom hooks (functions starting with `use`).
- Custom hooks can manage subscriptions, event listeners, or derived state.

## Practice Prompts

- Implement a timer component using refs and effects, ensuring cleanup on unmount.
- Audit existing components for unnecessary effects and refactor them into pure render logic or event handlers.
- Build a custom hook (e.g., `useLocalStorage`) that synchronizes state with browser storage, handling cleanup and dependency management.
