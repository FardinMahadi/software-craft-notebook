---
title: Adding Interactivity
status: draft
last_reviewed: 09-11-2025
---

# Adding Interactivity

Focus on events, state lifecycles, and updates using `useState`.

## Responding to Events

- Use camelCase handler props (`onClick`, `onChange`) and pass function references.
- Define handlers inside components to access props/state, or hoist them when reusability is required.

```jsx
function Button({ onClick, children }) {
  return <button onClick={onClick}>{children}</button>;
}
```

## State as Component Memory

- Initialize state with `useState(initialValue)`; initial value is used only on the first render.
- State updates schedule re-renders; React batches multiple updates during the same event.

```jsx
const [count, setCount] = useState(0);
setCount(count + 1);
setCount(count + 1); // still results in +1 due to stale closure
```

- Prefer updater functions when new state derives from previous state:

```jsx
setCount((prev) => prev + 1);
setCount((prev) => prev + 1); // increments twice
```

## Render & Commit Cycle

- Render phase: React calls components to produce JSX.
- Commit phase: React mutates the DOM and runs layout/browser work.
- Avoid side effects during render; use events or effects for DOM mutations.

## State as Snapshot

- State values are snapshots for the render in which they were read.
- Refs or closures capture state values at the time of definition; ensure you use up-to-date values via setters or refs.

## Queueing Updates

- Multiple state updates in a single event are processed sequentially.
- React may delay re-renders for performance; rely on the updater form to avoid stale values.

## Updating Objects & Arrays

- State must be immutable; create new objects or arrays when updating.

```jsx
setUser((prev) => ({ ...prev, name: newName }));
setTodos((prev) =>
  prev.map((todo) => (todo.id === id ? { ...todo, done: !todo.done } : todo))
);
```

## Practice Prompts

- Build a form that tracks input values with state and resets fields on submit.
- Experiment with multiple `setCount` calls using value vs updater forms to observe batching.
- Create a todo list with add, toggle, and delete actions, ensuring state updates remain immutable.
