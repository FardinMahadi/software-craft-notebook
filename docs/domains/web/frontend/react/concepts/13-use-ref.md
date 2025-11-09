---
title: useRef Deep Dive
status: draft
last_reviewed: 09-11-2025
---

# `useRef` Deep Dive

## Purpose

- Hold mutable values that persist for the lifetime of the component without triggering re-renders.
- Access DOM nodes or imperative APIs exposed by child components.
- Store previous state/prop values for comparison.

## Basic Usage

```jsx
function FocusInput() {
  const inputRef = useRef < HTMLInputElement > null;

  const handleClick = () => {
    inputRef.current?.focus();
  };

  return (
    <>
      <input ref={inputRef} />
      <button onClick={handleClick}>Focus</button>
    </>
  );
}
```

- Initial value is assigned to `.current`; subsequent renders reuse the same object.
- Updating `.current` does **not** cause a re-render—this is intentional.

## Storing Mutable State

```jsx
function Stopwatch() {
  const intervalId = (useRef < number) | (null > null);
  const startTime = useRef < number > 0;

  const start = () => {
    startTime.current = Date.now();
    intervalId.current = window.setInterval(
      () => setElapsed(Date.now() - startTime.current),
      50
    );
  };

  const stop = () => {
    if (intervalId.current) {
      clearInterval(intervalId.current);
      intervalId.current = null;
    }
  };
}
```

- Ideal for timers, animation frames, external subscriptions.
- Remember to clean up inside effects if refs reference external resources.

## Tracking Previous Values

```jsx
function usePrevious<T>(value: T) {
  const previous = useRef<T>();
  useEffect(() => {
    previous.current = value;
  }, [value]);
  return previous.current;
}
```

- Helpful for comparing props/state between renders (e.g., implementing `componentDidUpdate` behavior).

## Refs with Controlled Components

- Use refs sparingly when state-driven rendering suffices.
- Prefer controlled component patterns for form state, but refs are useful for focusing, selection, or interacting with third-party widgets.

## Imperative Handles

- Combine with `forwardRef` to expose custom APIs (see `useImperativeHandle` section in hooks overview).

## Testing Tips

- Access ref-exposed functions via testing-library queries + `fireEvent`.
- Mock DOM APIs (e.g., `focus`) when running in JSDOM.

## Practice Prompts

- Build a carousel component that uses refs to scroll to specific items on button clicks.
- Implement a custom `useScrollPosition` hook that stores the latest scroll position in a ref to avoid re-renders.
- Create a reusable `usePrevious` hook and write tests verifying it returns the previous value after updates.
